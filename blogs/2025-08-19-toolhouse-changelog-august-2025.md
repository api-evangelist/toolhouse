---
title: "Toolhouse Changelog August 2025"
slug: toolhouse-changelog-august-2025
date: 2025-08-19
url: https://toolhouse.ai/blog/toolhouse-changelog-august-2025
source: toolhouse.ai/blog
---

# Toolhouse Changelog August 2025

_Published 2025-08-19 — [Original post](https://toolhouse.ai/blog/toolhouse-changelog-august-2025)_

Toolhouse Changelog August 2025 What has changed in Toolhouse this month? Aug 19, 2025 4 minutes Orlando Kalossakas We’ve been focused on making Toolhouse more powerful, flexible, and easy to use. From enhancing integrations to improving the developer experience, our goal is to help you build, deploy, and manage AI agents more efficiently. Recent Updates Some of the features we’ve shipped recently include: Zapier and n8n Integrations : Connect Toolhouse agents to thousands of apps without writing custom code.

MCP Discovery : Automatically detect and connect the external services your agents need. Together.ai Model Support & BYOM : Run agents on open-weight models like Qwen and Kimi or bring your own model from supported providers. Agent Studio Previews : See live previews of agent outputs, making it faster to iterate on prompts and configurations. CLI Enhancements : Generate custom prompts to scaffold frontends with platforms like Lovable, v0, or Bolt.

Looking Ahead We’re continuing to focus on developer experience, seamless integrations, and expanding the capabilities of your agents. Expect more tools, automation options, and ways to tailor agents to your workflows in the coming months. N8N You can now integrate Toolhouse agents with n8n to connect agents directly into your workflows. Previously, connecting Toolhouse to external services required manual setup or custom glue code.

With this update, you can now build and automate workflows using Toolhouse inside n8n with minimal effort. What’s new When building an n8n workflow, you can now: Use custom Toolhouse nodes to send and receive data. Trigger agents with webhooks. Pipe outputs from Toolhouse into hundreds of supported n8n integrations. How it works Add Toolhouse as a node in any workflow.

Agents can be triggered automatically based on workflow conditions, and results can be routed to other apps and services in your stack. This feature is available now for all Toolhouse users. learn more about our n8n integration here Agent Studio You can now see previews of your agent outputs directly in Agent Studio. This update makes it easier to see agent output and fine tune agent behavior in real time.

How it Works Simply open your agent in Agent Studio, enter sample inputs in the preview pane, and the agent will generate responses instantly. You can adjust your prompt or configuration and redeploy your agent before using them in your projects. Zapier Overview Toolhouse now integrates directly with Zapier, allowing you to run your agents inside automated workflows.

With this update, you can connect Toolhouse to thousands of apps such as Slack, Gmail, Airtable, and HubSpot, all without writing code. Instead of building custom integrations, you can trigger agents from Zapier events, pass in data, and route agent responses back into the apps you already use. What’s new When building a Zap, you can now: Connect Toolhouse using your API key straight from the Toolhouse event step.

Select any of your existing Toolhouse agents in a dropdown. Send custom messages to agents and receive responses within your Zap. How it works Go to the Toolhouse integration page on Zapier and connect your account. Set up a trigger and configure delay or weekend scheduling options. In the Toolhouse action step, log in using your API key from the Toolhouse dashboard.

Choose an agent and craft your message. Test the step to verify outputs, then publish your Zap to automate your AI workflows. check out the documentation here Toolhouse CLI What’s new When deploying agents with the CLI, you’ll now receive a custom prompt that helps you scaffold a frontend using your favorite platforms, including Lovable, v0, or Bolt. How it works We added a new command to the CLI: th vibe .

You can run th vibe on any deployed YAML file to receive a prompt for your agent. learn more here MCP Discovery Overview Toolhouse now simplifies the process of integrating your agents with external services through MCP Discovery. When you create an agent in Agent Studio, Toolhouse automatically detects the necessary MCP servers, enabling seamless interaction with tools like Notion, Linear, Google Calendar, and more.

What’s New Automatic MCP Server Detection : Upon creating an agent, Toolhouse identifies and connects to the required MCP servers based on your agent's needs. Enabling and Disabling MCP Servers If MCP Discovery detects servers that aren't needed, you can easily disable them by toggling the 'Enabled' switch in the sidebar. Streamlined Publishing : Once configured, publish your agent, and it will be live and fully integrated with the selected MCP servers without additional setup.

How It Works Describe Your Agent : In Agent Studio, write a natural-language prompt detailing your agent's intended tasks. Run the Prompt : Toolhouse analyzes the prompt and displays a sidebar with recommended MCP servers. Configure MCP Servers : Enter the necessary credentials in the sidebar to enable your agent's access to the services. Publish Your Agent : Click 'Publish' to deploy your agent, now equipped with the ability to interact with the selected tools.

Integrating Custom MCP Servers You can still import your preferred MCP servers by instructing Agent Studio to "add my MCP server" followed by the URL to the desired MCP server. check out our documentation to learn more Toolhouse + Together AI Overview Toolhouse agents can now leverage powerful open-source models from Together.ai , including Qwen and Kimi. This integration allows for advanced reasoning capabilities at a competitive cost per million tokens, providing enhanced performance for your agents.

What’s New Advanced Reasoning Capabilities : Utilize open-weight models such as Qwen and Kimi for complex problem-solving tasks. Custom API Keys : Use your own API keys from your preferred service, offering better cost control, usage tracking, and enhanced privacy. Seamless Integration : Configure your agent to run on Together.ai models while still leveraging Toolhouse’s Model Context Protocol (MCP) integration with platforms like GitHub.

Learn more about using different models here ‹ How we cut API latency 5x after implementing OpenTelemetry Now Running on Together.ai Models! › Docs Pricing Community Business Start Building Don't build agents. Delegate work. ')"> ')"> ')"> Product Docs Pricing Compare Base44 Lindy Sana Zapier Company About Careers Privacy Terms Funded by the European Union NextGenerationEU © 2026 Toolhouse Technologies, Inc.

All rights reserved
