# Gameye

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Gameye is a managed game server orchestration platform for multiplayer game studios, founded in 2017 in Rotterdam (Gameye B.V.). It runs dedicated, containerized game servers across bare metal, cloud, and edge providers behind a single REST API — the Session API. Studios call POST /session with a region and a Docker image; Gameye selects the best available location, starts a container in about half a second, and returns the host IP and mapped ports players connect to. Capacity-based pricing carries no egress fees, and the platform is matchmaker-agnostic (Pragma Engine, Nakama, PlayFab, FlexMatch). Gameye has orchestrated 120M+ sessions with a 99.99% uptime SLA and serves studios including Torn Banner Studios (Chivalry 2) and Remedy Entertainment.

**Areas:** Company · Game Server Hosting · Game Server Orchestration · Multiplayer · Containers · Infrastructure · Gaming · Edge Computing · DevOps

## Gameye on APIs.io

Everything profiled for Gameye is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/gameye/](https://apis.io/providers/gameye/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [Gameye Artifacts API](https://apis.io/apis/gameye/gameye-artifacts-api/) — The Artifacts API from Gameye — 1 operation(s) for artifacts.
- [Gameye Available Location API](https://apis.io/apis/gameye/gameye-available-location-api/) — The Available Location API from Gameye — 1 operation(s) for available location.
- [Gameye Logs API](https://apis.io/apis/gameye/gameye-logs-api/) — The Logs API from Gameye — 1 operation(s) for logs.
- [Gameye Session API](https://apis.io/apis/gameye/gameye-session-api/) — The Session API from Gameye — 4 operation(s) for session.
- [Gameye Tag API](https://apis.io/apis/gameye/gameye-tag-api/) — The Tag API from Gameye — 1 operation(s) for tag.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (3)

Multi-step workflows that chain operations into a business task.

- [Allocate a Gameye session and get its connection address](https://apis.io/arazzos/gameye/gameye-allocate-session/)
- [Manage the player roster on a Gameye session](https://apis.io/arazzos/gameye/gameye-player-lifecycle/)
- [Stream logs, stop a Gameye session, and download an artifact](https://apis.io/arazzos/gameye/gameye-session-teardown/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [gameye](https://apis.io/servers/gameye/gameye/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Gameye Agentic Access](https://apis.io/agentic-access/gameye/gameye-agentic-access/)

#### Collections (5)

Postman and Open Collection request collections.

- [Gameye Session Artifacts API](https://apis.io/collections/gameye/open-gameye-artifacts-api/)
- [Gameye Session Artifacts Available Location API](https://apis.io/collections/gameye/open-gameye-available-location-api/)
- [Gameye Session Artifacts Logs API](https://apis.io/collections/gameye/open-gameye-logs-api/)
- [Gameye Artifacts Session API](https://apis.io/collections/gameye/open-gameye-session-api/)
- [Gameye Session Artifacts Tag API](https://apis.io/collections/gameye/open-gameye-tag-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Gameye Session Overlay](https://apis.io/overlays/gameye/gameye-session-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Gameye Authentication](https://apis.io/security/gameye/gameye-authentication/)
- [Gameye Domain Security](https://apis.io/security/gameye/gameye-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://gameye.com)
- [Documentation](https://gameye.com/docs/api-v2/)
- [Getting started](https://gameye.com/docs/getting-started/)
- [API reference](https://gameye.com/docs/api-v2/)
- [Pricing](https://gameye.com/pricing/)
- [Sign up](https://trial.gameye.com/)
- [Support](https://gameye.com/docs/support/getting-support/)
- [Changelog](https://gameye.com/docs/changelogs/)
- [Blog](https://gameye.com/blog/)
- [Terms of service](https://gameye.com/terms/)
- [Privacy policy](https://gameye.com/privacy/)
- [GitHub](https://github.com/Gameye)
- [Status](https://gameye.com/status/)

## API Evangelist rating

**Kin Score 51.4** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 45.5 |
| Contract governance | 4.5 |
| Operational transparency | 39.5 |
| Developer ergonomics | 73.2 |
| Access clarity | 44.7 |

**Agent readiness 28.3** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/gameye/](https://apis.io/providers/gameye/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Gameye: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/gameye/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
