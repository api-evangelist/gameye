---
name: Allocate a game session and get a connection address
description: Pick an available region for a Docker image, start a containerized game session, and return the host IP and mapped ports players connect to.
api: openapi/gameye-session-openapi.yml
operations: [get-available-locations, session-run, describe-session]
---

# Allocate a game session and connect players

Use the Gameye Session API to spin up a dedicated game server on demand.

## Auth
Every call needs `Authorization: Bearer <token>`. The token must carry the
`regions:read`, `session:start`, and `session:read` permission scopes. Use the
sandbox base URL `https://api.sandbox-gameye.gameye.net` while testing.

## Steps
1. **Find a region** — call `get-available-locations` (`GET /available-location/{image}`)
   with your image name. It returns candidate locations plus pingable IPv4s so you
   can measure latency. Do not cache the list; it changes.
2. **Start the session** — call `session-run` (`POST /session`) with a body containing
   `location`, `image`, and (recommended) a caller-supplied UUIDv4 `id`. Optionally set
   `env`, `args`, `labels`, `version` (image tag), `ttl` (e.g. `1h`), and `restart`.
   On success you get `201` with `host` and `ports[]`.
3. **Confirm / re-fetch** — call `describe-session` (`GET /session/{id}`) to read live
   `status`, `host`, `port`, and joined `players` if you need them again later.

## Rules
- Supply a unique `id` per session; re-using one returns `409 CONFLICT` (this is the
  natural-key idempotency contract — reuse it to avoid double-allocating).
- `420 CAPACITY_UNAVAILABLE` means retry after 2-5 seconds or pick another region.
- A configured warm pool ignores `env`/`args`/`labels` and serves a pre-warmed container.
- Set `ttl` so abandoned sessions self-terminate.
