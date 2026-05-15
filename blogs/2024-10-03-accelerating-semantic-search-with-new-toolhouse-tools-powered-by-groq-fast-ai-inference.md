---
title: "Accelerating Semantic Search with New Toolhouse Tools, Powered by Groq Fast AI Inference"
slug: accelerating-semantic-search-with-new-toolhouse-tools-powered-by-groq-fast-ai-inference
date: 2024-10-03
url: https://toolhouse.ai/blog/accelerating-semantic-search-with-new-toolhouse-tools-powered-by-groq-fast-ai-inference
source: toolhouse.ai/blog
---

# Accelerating Semantic Search with New Toolhouse Tools, Powered by Groq Fast AI Inference

_Published 2024-10-03 — [Original post](https://toolhouse.ai/blog/accelerating-semantic-search-with-new-toolhouse-tools-powered-by-groq-fast-ai-inference)_

Accelerating Semantic Search Accelerating Semantic Search with New Toolhouse Tools, Powered by Groq Fast AI Inference Semantic search is one of the biggest breakthroughs in AI: we now have a search engine that understands the meaning of words and phrases in a search query. This approach gives users more relevant results than keyword search, which only matches on exact words or synonyms.

Building a semantic search engine comes with its own challenges, particularly in terms of speed and architecture. Semantic search is one of the biggest breakthroughs in AI: we now have a search engine that understands the meaning of words and phrases in a search query. This approach gives users more relevant results than keyword search, which only matches on exact words or synonyms.

Building a semantic search engine comes with its own challenges, particularly in terms of speed and architecture. Oct 3, 2024 4 minutes Daniele Bernardi Semantic search is one of the biggest breakthroughs in AI: we now have a search engine that understands the meaning of words and phrases in a search query. This approach gives users more relevant results than keyword search, which only matches on exact words or synonyms.

Building a semantic search engine comes with its own challenges, particularly in terms of speed and architecture. That's why we're excited to announce our partnership with Groq, the leader in AI inference acceleration. Thanks to Groq LPU™ (Language Processing Unit) AI inference technology, Toolhouse now offers developers fast, cutting-edge AI tools for semantic search.

Introducing the Toolhouse Semantic Search Tool Suite Toolhouse offers several tools to store and fetch search results semantically. Our first set of semantic search tools allows LLMs to store, fetch, and delete user memories. These tools are available today in the Tool Store . Memories are difficult to store – users can have long conversations with an agent, and an agent may rely on one or more LLMs to complete their assigned task.

Sharing the entire context across LLMs is simply not feasible – it's expensive, it increases latency, and not all memories will fit into each LLM's context window. Besides, integrating and hosting a semantic search product is often time consuming and expensive. To solve these problems, Toolhouse created fast access storage. When developers install the Semantic Memory Search tool , they equip their LLMs with the ability to retrieve past conversations.

The tool instructs the LLM on how to do so without the need to use additional prompting. Every time the LLM requires a memory from the user, it creates a semantic query (for example, a phrase), and sends its query to the Semantic Memory Search tool. The tool will look into past contexts, then make an inference call to filter and return memories that are relevant to the initial query.

The result is returned to the LLM. As part of this first set of semantic tools, we’re excited to make two additional tools available: Memory Store and Semantic Memory Delete . Memory Store provides LLMs with the ability to store conversations in memory. Memory Delete lets the LLM delete memories that match a specific semantic query. All tools are compatible with any major LLM, as well as any LLM that can expose a completion API compatible with the OpenAI format.

More Speed, More Savings In our preliminary tests, Semantic Memory Store performed incredibly well, consistently delivering responses in less than 300ms at high-watermark. This is possible due to Toolhouse's optimized cloud, as well as Groq's fast inference speed. How to Use the Toolhouse Semantic Search The Semantic Search toolset is available today to all Early Access customers – you can sign up for Early Access here .

Here’s how to use it: Log into Toolhouse Ensure you have Toolhouse installed in your LLM calls. This integration is only needed once, and it takes three lines of code . Pass a user identifier metadata . Metadata allow Toolhouse to retrieve the memories for the right users. Metadata are hashed and scoped at your instance level, so any user ID you send is not identifiable, not even by Toolhouse.

Install the Semantic Memory Search tool . We're Here to Help We'd love to hear your input and feedback about the Semantic Memory Tools. You can join our community on Discord , or follow us on LinkedIn and X . If you built something that uses these tools, do let us know, and we'll be happy to showcase your use case. ‹ Toolhouse is getting an upgrade Yes, you can build your pitch deck with AI.

Just do it right. › Docs Pricing Community Business Start Building Don't build agents. Delegate work. ')"> ')"> ')"> Product Docs Pricing Compare Base44 Lindy Sana Zapier Company About Careers Privacy Terms Funded by the European Union NextGenerationEU © 2026 Toolhouse Technologies, Inc. All rights reserved
