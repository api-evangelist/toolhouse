---
title: "Your agents are now APIs: introducing the Streaming API"
slug: introducing-the-streaming-api
date: 2025-05-20
url: https://toolhouse.ai/blog/introducing-the-streaming-api
source: toolhouse.ai/blog
---

# Your agents are now APIs: introducing the Streaming API

_Published 2025-05-20 — [Original post](https://toolhouse.ai/blog/introducing-the-streaming-api)_

Your agents are now APIs: introducing the Streaming API Agent deployment is simpler than ever. Learn how to deploy agents as API and integrate them in your workflow. May 20, 2025 4 minutes Daniele Bernardi We just launched the Toolhouse Streaming API , the easiest way to deploy your locally-built agents into an API hosted in our infrastructure. If you know how to call an API, you now know how to build agents.

Engineers have a deployment problem The "works on my machine" phase is only half the battle to productionize an agent. The more painful half typically involves setting up your runtime, managing API access, and handling statefulness of your agent. We keep hearing that even for larger teams with sophisticated operations, this represents significant engineering time better spent elsewhere.

This is one of the many cases where tech companies ask developers to reinvent the wheel – we (and our users) believe instead there is a lot of value in bringing convenience to agentic deployments. The Solution: Deploy agents as an API The Toolhouse Streaming API converts your agents into callable API endpoints with a single command: running th deploy will automatically deploy your agent on the Toolhouse infrastructure.

This single command packs a punch: It packages your agent file It provisions the infrastructure (with support for deployment regions coming soon) Sets up authentication Provides a dedicated streaming endpoint Every deployed agent will have its own endpoint that you can call via API: This endpoint will stream the response back to the client, as you would expect by a standard completion API call: Agents can be public or private.

Public agents can be called without an API key. Toolhouse Pro users can choose to make their agents private, meaning they can require an API Key to run. This is useful to protect internal or private agent from unwanted traffic. Just like it happens for th run and Agent Studio, your agents will be connected to the Toolhouse runtime, which includes our MCP servers, memory, storage, and all the stack you need to build sophisticated agents.

There is no custom integration required. Stateful interactions This new streaming API supports statefulness through session management. Each agent call will return a context identified called Run ID. Referencing the Run ID in subsequent calls will give your agent continuity. # First request curl -v -XPOST https://agents.toolhouse.ai/your-agent-id \ --json '{"message": "What AI companies do you know about?"}' # The API will respond with a x-toolhouse-run-id header curl -XPUT https://agents.toolhouse.ai/your-agent-id/ $RUN_ID \ --json '{"message": "Please introduce me to people at Groq"}' Giving statefulness to agents expands the array of use cases you can build with Toolhouse.

For example, you can now use Toolhouse to build conversational agents. To showcase the power of statefulness, we built Handshake , an app that makes an intro to my contacts on my behalf. Handshake has access to a selection of my LinkedIn contacts – you can ask queries like “give me contacts who work at AI companies” and the agent can offer to make an intro to my contacts.

Apps like Handshake shows how Toolhouse can accelerate the development of “talk to your data” use cases: simply bring your data in, upload it via Toolhouse RAG, and you’re good to go. Built for engineers, loved by vibe coders In our user testing we found out that the simplicity of this pattern is loved by both engineers and vibe coders. Engineers can drastically simplify their agentic orchestration.

Because every agent is an API, they can call multiple agents both in parallel and sequentially as fetch requests: const body = JSON . stringify ( { vars : { latestRelease : '1.2.3' } } ) ; const method = 'POST' ; const config = { method , body } // Calls 3 Github agents each one specialized // in retrieving specific parts of the repo. // These agents run in parallel.

const [ allCommitsMessagesInLatestRelease , contributors , latestReadme ] = await Promise . all ( [ fetch ( 'https://agents.toolhouse.ai/get-all-commits' , config ) . then ( response => response . text ( ) ) , fetch ( 'https://agents.toolhouse.ai/get-all-contributors' , config ) . then ( response => response . text ( ) ) , fetch ( 'https://agents.toolhouse.ai/get-readme-for-release' , config ) .

then ( response => response . text ( ) ) , ] ) ; // After the retrieval, another agent // writes an announcement blog post. const response = await fetch ( '<https://agents.toolhouse.ai/devrel-agent-blog>' , { method body : JSON . stringify ( { allCommitsMessagesInLatestRelease , contributors , latestReadme } ) ; // Here's the blog post! const blogPost = await response .

text ( ) ; Vibe coders can integrate Toolhouse in Lovable or v0 with this simple prompt: Build a chatbot interface similar to ChatGPT. When the user types Enter on their first message, call POST <https://agents.toolhouse.ai/YOUR_AGENT_ID> with this JSON body: {vars: { "message": "the user message" }}. The request will return an X-Toolhouse-Run-ID header. Save it in the runId variable.

On any subsequent user message, call PUT <https://agents.toolhouse.ai/YOUR_AGENT_ID/runId> Start building today You can read our documentation on how to leverage this pattern, or clone the Handshake agent to create similar experiences. If you’re building with Toolhouse, let us know on Discord – we’d love to feature your work. ‹ Introducing Toolhouse RAG: Free Yourself From RAG Complexity Ship to production in one command: introducing the Toolhouse CLI › Docs Pricing Community Business Start Building Don't build agents.

Delegate work. ')"> ')"> ')"> Product Docs Pricing Compare Base44 Lindy Sana Zapier Company About Careers Privacy Terms Funded by the European Union NextGenerationEU © 2026 Toolhouse Technologies, Inc. All rights reserved
