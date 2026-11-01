# Toolhouse

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

Toolhouse is a Backend-as-a-Service platform for building, deploying, and managing "AI workers"
(Toolhouse's current product noun, used interchangeably with "AI agents"). The homepage frames the value
proposition as "Turn your AI chats into affordable and reliable AI workers that do work while you're
busy," and the docs define a worker as "a system that carries out a task with three components: a trigger,
a process that may include specialized skills, and tools or systems it can connect to." Builders describe
a task in plain language in the Agent Editor and ship a worker to production; developers can do the same
programmatically via SDKs. Every worker is automatically wired into Toolhouse's pre-integrated
capabilities, including web and social media search, scraping, Toolhouse RAG, persistent memory, the
Virtual Computer code-execution sandbox, image generation/editing and vision, document parsing, file
download, and MCP Discovery for connecting to thousands of MCP servers at runtime. The platform exposes
a Workers API (agents.toolhouse.ai) for invoking deployed workers over REST with text and NDJSON
streaming and stateful conversation continuity (X-Toolhouse-Run-ID), a Platform API for full worker and
run lifecycle management, scheduling (10-minute minimum cadence), metrics, monetization, and integrations,
plus no-code workflow integration through Zapier and Toolhouse n8n Nodes. Toolhouse runs on a broad model
substrate including OpenAI, Anthropic, Together AI, Groq, and NVIDIA model offerings. The current public
pricing surface is Business ($500/mo, 25,000 credits, 50 workers), Business Max ($1,200/mo, 80,000
credits, 500 workers), and custom Enterprise — all plans include "free unlimited tokens" and a 14-day
free trial. Toolhouse reports 7,000+ teams on the platform and 40+ integrations and is backed by
NextGenerationEU funding.

**Areas:** Agent Infrastructure · AI Agents · AI Workers · Backend-as-a-Service · MCP · MCP Discovery · RAG · Tools · Workers API

## Toolhouse on APIs.io

Everything profiled for Toolhouse is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/toolhouse/](https://apis.io/providers/toolhouse/)** — or go straight to one of the APIs or properties below.

### APIs (8)

- [Toolhouse Workers API](https://apis.io/apis/toolhouse/workers-api/) — The Toolhouse Workers API (historically the "Agents API") enables HTTP execution of any deployed Toolhouse worker. Workers defined via the Agent Editor or…
- [Toolhouse Agent Runs API](https://apis.io/apis/toolhouse/toolhouse-agent-runs-api/) — The Agent Runs API from Toolhouse — 4 operation(s) for agent runs.
- [Toolhouse API Keys API](https://apis.io/apis/toolhouse/toolhouse-api-keys-api/) — The API Keys API from Toolhouse — 3 operation(s) for api keys.
- [Toolhouse Backoffice API](https://apis.io/apis/toolhouse/toolhouse-backoffice-api/) — The Backoffice API from Toolhouse — 15 operation(s) for backoffice.
- [Toolhouse Logs API](https://apis.io/apis/toolhouse/toolhouse-logs-api/) — The Logs API from Toolhouse — 2 operation(s) for logs.
- [Toolhouse Metrics API](https://apis.io/apis/toolhouse/toolhouse-metrics-api/) — The Metrics API from Toolhouse — 4 operation(s) for metrics.
- [Toolhouse SDK API](https://apis.io/apis/toolhouse/toolhouse-sdk-api-api/) — The SDK API API from Toolhouse — 20 operation(s) for sdk api.
- [Toolhouse User API](https://apis.io/apis/toolhouse/toolhouse-user-api-api/) — The User API API from Toolhouse — 58 operation(s) for user api.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [MCP Server](https://apis.io/servers/toolhouse/mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Toolhouse Agentic Access](https://apis.io/agentic-access/toolhouse/toolhouse-agentic-access/)

#### JSON Schema (1)

The data models the API reads and writes.

- [Toolhouse Agent](https://apis.io/schemas/toolhouse/toolhouse-agent/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Toolhouse Agent Structure](https://apis.io/json-structure/toolhouse/toolhouse-agent-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Toolhouse Context](https://apis.io/jsonld/toolhouse/toolhouse-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Toolhouse Vocabulary](https://apis.io/vocabularies/toolhouse/toolhouse-vocabulary/)

#### Examples (2)

Example requests and responses.

- [Toolhouse List Agents Example](https://apis.io/examples/toolhouse/toolhouse-list-agents-example/)
- [Toolhouse Upsert Agent Example](https://apis.io/examples/toolhouse/toolhouse-upsert-agent-example/)

#### Collections (14)

Postman and Open Collection request collections.

- [Toolhouse Agent Runs API](https://apis.io/collections/toolhouse/open-toolhouse-agent-runs-api/)
- [Toolhouse Agent Runs API Keys API](https://apis.io/collections/toolhouse/open-toolhouse-api-keys-api/)
- [Toolhouse Agent Runs Backoffice API](https://apis.io/collections/toolhouse/open-toolhouse-backoffice-api/)
- [Toolhouse Agent Runs Logs API](https://apis.io/collections/toolhouse/open-toolhouse-logs-api/)
- [Toolhouse Agent Runs Metrics API](https://apis.io/collections/toolhouse/open-toolhouse-metrics-api/)
- [Toolhouse Agent Runs SDK API API](https://apis.io/collections/toolhouse/open-toolhouse-sdk-api-api/)
- [Toolhouse Agent Runs User API API](https://apis.io/collections/toolhouse/open-toolhouse-user-api-api/)
- [Toolhouse Agent Runs API](https://apis.io/collections/toolhouse/postman-toolhouse-agent-runs-api/)
- [Toolhouse Agent Runs API Keys API](https://apis.io/collections/toolhouse/postman-toolhouse-api-keys-api/)
- [Toolhouse Agent Runs Backoffice API](https://apis.io/collections/toolhouse/postman-toolhouse-backoffice-api/)
- [Toolhouse Agent Runs Logs API](https://apis.io/collections/toolhouse/postman-toolhouse-logs-api/)
- [Toolhouse Agent Runs Metrics API](https://apis.io/collections/toolhouse/postman-toolhouse-metrics-api/)
- [Toolhouse Agent Runs SDK API API](https://apis.io/collections/toolhouse/postman-toolhouse-sdk-api-api/)
- [Toolhouse Agent Runs User API API](https://apis.io/collections/toolhouse/postman-toolhouse-user-api-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Toolhouse — jsonschema rules](https://apis.io/rules/toolhouse/toolhouse-jsonschema-spectral-rules/)
- [Toolhouse API Rules](https://apis.io/rules/toolhouse/toolhouse-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Toolhouse Authentication](https://apis.io/security/toolhouse/toolhouse-authentication/)
- [Toolhouse Domain Security](https://apis.io/security/toolhouse/toolhouse-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Toolhouse Plans Pricing](https://apis.io/plans/toolhouse/toolhouse-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Toolhouse Rate Limits](https://apis.io/rate-limits/toolhouse/toolhouse-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Toolhouse Finops](https://apis.io/finops/toolhouse/toolhouse-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://toolhouse.ai/)
- [Documentation](https://docs.toolhouse.ai/toolhouse)
- [Pricing](https://toolhouse.ai/pricing)
- [Support](https://help.toolhouse.ai/)
- [Changelog](https://toolhouse.ai/blog/toolhouse-changelog-august-2025)
- [Blog](https://toolhouse.ai/blog)
- [Terms of service](https://toolhouse.ai/tos)
- [Privacy policy](https://toolhouse.ai/privacy)
- [GitHub](https://github.com/toolhouseai)
- [Status](https://toolhouse.betteruptime.com/)

## API Evangelist rating

**Kin Score 50.3** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 71.7 |
| Contract quality | 51.7 |
| Contract governance | 27.3 |
| Operational transparency | 44.7 |
| Developer ergonomics | 46.4 |
| Access clarity | 44.7 |

**Agent readiness 27.3** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/toolhouse/](https://apis.io/providers/toolhouse/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Toolhouse: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/toolhouse/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
