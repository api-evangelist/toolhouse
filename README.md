# Toolhouse

Toolhouse is a Backend-as-a-Service platform for building, deploying, and managing AI agents. Developers define agents as code and deploy them as APIs with a single command. Agents are automatically connected to over 40 pre-built tools including RAG, memory, code execution, browser automation, web scraping, and database connections. Toolhouse also provides an MCP server so any MCP-compatible client can access the full tool library.

**Website:** [https://toolhouse.ai](https://toolhouse.ai)
**Documentation:** [https://docs.toolhouse.ai/toolhouse](https://docs.toolhouse.ai/toolhouse)
**GitHub Org:** [https://github.com/toolhouseai](https://github.com/toolhouseai)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

AI Agents, Agent Infrastructure, Backend as a Service, MCP, Tools

## APIs

### Toolhouse Platform API

The Toolhouse Platform API provides management and orchestration capabilities for AI agents and tools. It includes endpoints for user profile management, billing, API key administration, tool discovery and execution, agent run management with pagination, Agent Studio chat sessions, agent file management, agent subscriptions, bundle management, scheduled agent execution via cron expressions, and MCP server configuration. Authentication uses HTTPBearer JWT tokens.

**Human URL:** [https://docs.toolhouse.ai/toolhouse](https://docs.toolhouse.ai/toolhouse)

**Tags:** Agent Runs, AI Agents, API Keys, Billing, Bundles, Management, Schedules, Tools

**Properties:**
- [Documentation](https://docs.toolhouse.ai/toolhouse)
- [OpenAPI](openapi/toolhouse-openapi-original.yml)
- [SpectralRules](rules/toolhouse-rules.yml)
- [NaftikoCapability](capabilities/shared/toolhouse-platform.yaml)

### Toolhouse Agents API

The Toolhouse Agents API enables execution of deployed AI agents via simple HTTP endpoints. Agents defined as code can be deployed and accessed through REST calls that support streaming responses, conversation continuation via run IDs, and full conversation history retrieval. Public agents require no authentication while private agents use Bearer token authorization.

**Human URL:** [https://docs.toolhouse.ai/toolhouse/advanced-concepts/publish-and-run-your-agents](https://docs.toolhouse.ai/toolhouse/advanced-concepts/publish-and-run-your-agents)

**Tags:** AI Agents, Conversations, Execution, Streaming

## SDKs & Integrations

| Name | URL |
|---|---|
| Python SDK | [https://github.com/toolhouseai/toolhouse-sdk-python](https://github.com/toolhouseai/toolhouse-sdk-python) |
| TypeScript SDK | [https://github.com/toolhouseai/toolhouse-sdk-typescript](https://github.com/toolhouseai/toolhouse-sdk-typescript) |
| MCP Server | [https://github.com/toolhouseai/toolhouse-mcp](https://github.com/toolhouseai/toolhouse-mcp) |
| n8n Integration | [https://github.com/toolhouseai/n8n-nodes-toolhouse](https://github.com/toolhouseai/n8n-nodes-toolhouse) |

## Artifacts

### OpenAPI Specifications

| File | Description |
|---|---|
| [openapi/toolhouse-openapi-original.yml](openapi/toolhouse-openapi-original.yml) | Toolhouse Platform API — OpenAPI 3.1 |

### Spectral Rules

| File | Description |
|---|---|
| [rules/toolhouse-rules.yml](rules/toolhouse-rules.yml) | Spectral ruleset enforcing Toolhouse API conventions |

### Naftiko Capabilities

| File | Description |
|---|---|
| [capabilities/agent-management.yaml](capabilities/agent-management.yaml) | Agent lifecycle management workflow (REST + MCP, 13 tools) |
| [capabilities/shared/toolhouse-platform.yaml](capabilities/shared/toolhouse-platform.yaml) | Shared Toolhouse Platform API definition |

### JSON Schema

| File | Description |
|---|---|
| [json-schema/toolhouse-agent-schema.json](json-schema/toolhouse-agent-schema.json) | JSON Schema for the Toolhouse Agent entity |

### JSON Structure

| File | Description |
|---|---|
| [json-structure/toolhouse-agent-structure.json](json-structure/toolhouse-agent-structure.json) | Structured documentation of the Toolhouse Agent object model |

### JSON-LD Context

| File | Description |
|---|---|
| [json-ld/toolhouse-context.jsonld](json-ld/toolhouse-context.jsonld) | JSON-LD context for Toolhouse domain vocabulary |

### Examples

| File | Description |
|---|---|
| [examples/toolhouse-list-agents-example.json](examples/toolhouse-list-agents-example.json) | GET /me/agents — list agents response |
| [examples/toolhouse-upsert-agent-example.json](examples/toolhouse-upsert-agent-example.json) | POST /me/agents — create agent request/response |

### Vocabulary

| File | Description |
|---|---|
| [vocabulary/toolhouse-vocabulary.yml](vocabulary/toolhouse-vocabulary.yml) | Domain vocabulary and taxonomy for the Toolhouse platform |

## Common Properties

- [Website](https://toolhouse.ai/)
- [Documentation](https://docs.toolhouse.ai/toolhouse)
- [Blog](https://toolhouse.ai/blog)
- [Pricing](https://toolhouse.ai/pricing)
- [Login](https://app.toolhouse.ai)
- [About](https://toolhouse.ai/about)
- [GitHubOrganization](https://github.com/toolhouseai)
- [PrivacyPolicy](https://toolhouse.ai/privacy)
- [TermsOfService](https://toolhouse.ai/tos)
- [Twitter](https://x.com/toolhouseai)
- [LinkedIn](https://www.linkedin.com/company/toolhouseai)
- [Discord](https://discord.com/invite/xPvyBxhHtu)
- [YouTube](https://youtube.com/@toolhouseai)
- [Support](https://help.toolhouse.ai/)
- [Status](https://toolhouse.betteruptime.com/)

## Timestamps

- **Created:** 2026-03-26
- **Modified:** 2026-05-03

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
