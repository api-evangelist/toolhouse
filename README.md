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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Toolhouse is a Backend-as-a-Service platform for building, deploying, and managing "AI workers" (Toolhouse's current product noun, used interchangeably with "AI agents"). The homepage frames the value proposition as "Turn your AI chats into affordable and reliable AI workers that do work while you're busy," and the docs define a worker as "a system that carries out a task with three components: a trigger, a process that may include specialized skills, and tools or systems it can connect to." Builders describe a task in plain language and ship a worker to production; developers can invoke any worker over HTTP via the Workers API at `agents.toolhouse.ai`. Every worker is wired into pre-integrated capabilities including Toolhouse RAG, web and social media search, scraping, the Virtual Computer (Python sandbox), image generation/editing, vision, document parsing, file download, memory, and MCP Discovery.

**Website:** [https://toolhouse.ai](https://toolhouse.ai)
**Documentation:** [https://docs.toolhouse.ai/toolhouse](https://docs.toolhouse.ai/toolhouse)
**GitHub Org:** [https://github.com/toolhouseai](https://github.com/toolhouseai)
**Pricing:** Business $500/mo (25k credits) · Business Max $1,200/mo (80k credits) · Enterprise custom · all plans include free unlimited tokens.

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

Agent Infrastructure, AI Agents, AI Workers, Backend as a Service, MCP, MCP Discovery, RAG, Tools, Workers API

## APIs

### Toolhouse Platform API

Management and orchestration capabilities for AI workers and connected tools. Endpoints cover user profile and billing, API key lifecycle, worker definition and deployment, agent-run management with paginated listing and per-run logs (including MCP server logs), Agent Studio chat sessions, agent file management, agent subscriptions and monetization, transfer, scheduled execution via cron (10-minute minimum), MCP server and MCP registry configuration, integrations and auth connections, OAuth callback handling, Stripe webhook and session handling, and an agent-runs metrics surface for usage, volume, and per-agent summary reporting. Authentication is HTTPBearer with per-user API keys.

**Human URL:** [https://docs.toolhouse.ai/toolhouse](https://docs.toolhouse.ai/toolhouse)

**Tags:** Agent Runs, AI Agents, AI Workers, Agent Studio, API Keys, Billing, Credits, Integrations, Management, Metrics, Monetization, Schedules, SDK

**Properties:**
- [Documentation](https://docs.toolhouse.ai/toolhouse)
- [OpenAPI](openapi/toolhouse-openapi-original.yml)
- [SpectralRules](rules/toolhouse-rules.yml)
- [Naftiko Capabilities](capabilities/)

### Toolhouse Workers API

HTTP execution surface for any deployed worker at `https://agents.toolhouse.ai`. `POST /{agent_id}` starts a new task, `PUT /{agent_id}/{run_id}` continues an existing conversation, and `GET /{agent_id}/{run_id}` retrieves the full history. NDJSON variants under `/ndjson/` stream the worker's output plus out-of-band tool-call and debug signals. Conversation continuity is keyed by the `X-Toolhouse-Run-ID` response header. Attachments are supported via URL (30-second download timeout) or base64-encoded direct upload (10 MB max per attachment). Public workers require no authentication; private workers use HTTPBearer with a Toolhouse API key.

**Human URL:** [https://docs.toolhouse.ai/toolhouse/developers/workers-api](https://docs.toolhouse.ai/toolhouse/developers/workers-api)

**Base URL:** `https://agents.toolhouse.ai`

**Tags:** AI Agents, AI Workers, Attachments, Conversations, Execution, Statefulness, Streaming

## SDKs & Integrations

| Name | URL |
|---|---|
| Python SDK (v1.3.1) | [toolhouseai/toolhouse-sdk-python](https://github.com/toolhouseai/toolhouse-sdk-python) |
| TypeScript SDK | [toolhouseai/toolhouse-sdk-typescript](https://github.com/toolhouseai/toolhouse-sdk-typescript) |
| Client (JavaScript) | [toolhouseai/client](https://github.com/toolhouseai/client) |
| MCP Server | [toolhouseai/toolhouse-mcp](https://github.com/toolhouseai/toolhouse-mcp) |
| MCP Distributed | [toolhouseai/mcp-distributed](https://github.com/toolhouseai/mcp-distributed) |
| n8n Nodes | [toolhouseai/n8n-nodes-toolhouse](https://github.com/toolhouseai/n8n-nodes-toolhouse) |
| Examples | [toolhouseai/toolhouse-examples](https://github.com/toolhouseai/toolhouse-examples) |
| Fastlane Demo | [toolhouseai/fastlane-demo](https://github.com/toolhouseai/fastlane-demo) |
| Toolhouse Assessment | [toolhouseai/toolhouse-assessment](https://github.com/toolhouseai/toolhouse-assessment) |
| Teleprompter | [toolhouseai/toolhouse-teleprompter](https://github.com/toolhouseai/toolhouse-teleprompter) |
| Agentic Labs | [toolhouseai/toolhouse-agenticlabs](https://github.com/toolhouseai/toolhouse-agenticlabs) |

## Artifacts

### OpenAPI Specifications

| File | Description |
|---|---|
| [openapi/toolhouse-openapi-original.yml](openapi/toolhouse-openapi-original.yml) | Toolhouse Platform API — OpenAPI 3.1 (60+ endpoints) |

### Spectral Rules

| File | Description |
|---|---|
| [rules/toolhouse-rules.yml](rules/toolhouse-rules.yml) | Spectral ruleset enforcing Toolhouse API conventions |

### Naftiko Capabilities

| File | Description |
|---|---|
| [capabilities/toolhouse-user-api.yaml](capabilities/toolhouse-user-api.yaml) | User API capability (78 operations) |
| [capabilities/toolhouse-sdk-api.yaml](capabilities/toolhouse-sdk-api.yaml) | Toolhouse SDK API capability (`/v1/` surface) |
| [capabilities/toolhouse-agent-runs.yaml](capabilities/toolhouse-agent-runs.yaml) | Agent runs capability |
| [capabilities/toolhouse-api-keys.yaml](capabilities/toolhouse-api-keys.yaml) | API key lifecycle capability |
| [capabilities/toolhouse-backoffice.yaml](capabilities/toolhouse-backoffice.yaml) | Backoffice capability |
| [capabilities/toolhouse-logs.yaml](capabilities/toolhouse-logs.yaml) | Logs capability |
| [capabilities/toolhouse-metrics.yaml](capabilities/toolhouse-metrics.yaml) | Metrics capability |

### JSON Schema

| File | Description |
|---|---|
| [json-schema/toolhouse-agent-schema.json](json-schema/toolhouse-agent-schema.json) | JSON Schema for the Toolhouse Agent / Worker entity |

### JSON Structure

| File | Description |
|---|---|
| [json-structure/toolhouse-agent-structure.json](json-structure/toolhouse-agent-structure.json) | Structured documentation of the Toolhouse Agent / Worker model |

### JSON-LD Context

| File | Description |
|---|---|
| [json-ld/toolhouse-context.jsonld](json-ld/toolhouse-context.jsonld) | JSON-LD context (AIWorker, Agent, WorkerRun, AgentRun, Tool, Schedule, ApiKey, McpServer) |

### Examples

| File | Description |
|---|---|
| [examples/toolhouse-list-agents-example.json](examples/toolhouse-list-agents-example.json) | GET /me/agents — list agents response |
| [examples/toolhouse-upsert-agent-example.json](examples/toolhouse-upsert-agent-example.json) | POST /me/agents — create agent request/response |

### Vocabulary

| File | Description |
|---|---|
| [vocabulary/toolhouse-vocabulary.yml](vocabulary/toolhouse-vocabulary.yml) | Domain vocabulary and taxonomy for the Toolhouse platform |

### Plans, Rate Limits, and FinOps

| File | Description |
|---|---|
| [plans/toolhouse-plans-pricing.yml](plans/toolhouse-plans-pricing.yml) | API Commons Plans 0.1 — Business / Business Max / Enterprise tiers (reconciled 2026-05-22) |
| [rate-limits/toolhouse-rate-limits.yml](rate-limits/toolhouse-rate-limits.yml) | API Commons Rate Limits 0.1 — credit quotas, schedule floor, attachment caps |
| [finops/toolhouse-finops.yml](finops/toolhouse-finops.yml) | FOCUS-aligned FinOps framework for worker_run_credits and operational meters |

## Common Properties

- [Website](https://toolhouse.ai/)
- [Documentation](https://docs.toolhouse.ai/toolhouse)
- [Documentation Sitemap](https://docs.toolhouse.ai/toolhouse/sitemap.md)
- [LLMs.txt](https://docs.toolhouse.ai/toolhouse/llms-full.txt)
- [Blog](https://toolhouse.ai/blog)
- [Pricing](https://toolhouse.ai/pricing)
- [Login](https://app.toolhouse.ai)
- [About](https://toolhouse.ai/about)
- [GitHub Organization](https://github.com/toolhouseai)
- [Privacy Policy](https://toolhouse.ai/privacy)
- [Terms of Service](https://toolhouse.ai/tos)
- [Twitter](https://x.com/toolhouseai)
- [LinkedIn](https://www.linkedin.com/company/toolhouseai)
- [Discord](https://discord.com/invite/xPvyBxhHtu)
- [YouTube](https://youtube.com/@toolhouseai)
- [Support](https://help.toolhouse.ai/)
- [Status](https://toolhouse.betteruptime.com/)

## Notable Findings (2026-05-22 Refresh)

- Toolhouse has rebranded around **"AI workers"** as the primary product noun (used interchangeably with "AI agents" in docs).
- Public pricing has been restructured: the previously published **Basic (free)** and **Pro ($10/mo)** tiers are gone. The entry tier is now **Business at $500/mo** (25,000 credits, 50 workers, 30-day logs). **Business Max** is $1,200/mo (80,000 credits, 500 workers, 1-year logs). All plans include **free unlimited tokens**.
- Workers API host is `agents.toolhouse.ai` with text + NDJSON streaming, stateful run IDs via `X-Toolhouse-Run-ID`, and 10 MB attachment uploads.
- Schedule cadence floor is **10 minutes** per worker schedule.
- Tavily is now an Official Partner integration; 100+ integrations available across the gallery (GitHub, Stripe, Salesforce, HubSpot, Slack, Notion, Google Workspace, etc.).
- Toolhouse reports **7,000+ teams** on the platform and is backed by NextGenerationEU funding.
- Python SDK latest release **v1.3.1** (Dec 23, 2024) — hand-written, not OpenAPI-generated.
- The previously listed `toolhouse-cli` repo is no longer in the public GitHub org listing.

## Timestamps

- **Created:** 2026-03-26
- **Modified:** 2026-05-22

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
