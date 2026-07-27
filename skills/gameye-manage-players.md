---
name: Track players joining and leaving a session
description: Register and remove player IDs on a running Gameye session and read the current joined-player count for backfill decisions.
api: openapi/gameye-session-openapi.yml
operations: [join-session, leave-session, describe-session]
---

# Track players on a session

Keep Gameye's view of a session's roster in sync with your matchmaker.

## Auth
`Authorization: Bearer <token>`. Reads need `session:read`.

## Steps
1. **Join** — call `join-session` (`PUT /session/player/join`) with `session` (the id)
   and a `players[]` array of player IDs. The response returns the new total `count`
   and the `players[]` now in the session.
2. **Leave** — call `leave-session` (`DELETE /session/player/leave`) with the `players[]`
   to remove. The response returns the updated `count`.
3. **Inspect** — call `describe-session` (`GET /session/{id}`); `players.joined` and
   `players.joinedCount` reflect the live roster.

## Rules
- Player tracking drives backfill: combine `session-list` filters `location` +
  `playerCount[lt]` to find under-filled sessions in a region.
- A `404` on join/leave means the session no longer exists (terminated or expired).
- `422 INVALID_REQUEST` means malformed body — check `violations[]` in the error.
