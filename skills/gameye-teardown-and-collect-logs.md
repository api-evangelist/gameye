---
name: Tear down a session and collect its logs and artifacts
description: Stream a game server's logs, stop the session, and download crash dumps or other artifacts from the terminated container.
api: openapi/gameye-session-openapi.yml
operations: [stream-logs, session-stop, artifacts]
---

# Tear down a session and collect diagnostics

End a match cleanly and retrieve everything you need for debugging.

## Auth
`Authorization: Bearer <token>` with `logs:read`, `session:stop`, and
`artifact:read` scopes.

## Steps
1. **Stream logs (optional)** — call `stream-logs` (`GET /logs?id=<session>`), set
   `follow=true` to keep the stream open or omit it to pull everything written so far.
2. **Stop the session** — call `session-stop` (`DELETE /session/{id}`). Gameye sends
   `SIGTERM` to the container and returns `204`. A second stop returns `409`.
3. **Download artifacts** — call `artifacts` (`GET /artifacts?session=<id>&path=<abs>`)
   with an absolute Unix path (e.g. `/home/user/game/crashdump.log`). You get a
   `.tar.gz`; keep it under 100 MB.

## Rules
- Artifacts are only downloadable **after** the session is terminated, and only while
  the container still lives on its host — pull them promptly.
- Quote the error `identifier` trace field when contacting support.
