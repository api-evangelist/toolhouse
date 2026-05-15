---
title: "Connect your Agents to any workflow with Callbacks and Last Agent Message"
slug: connect-your-agents-to-any-workflow-with-callbacks-and-last-agent-message
date: 2025-03-27
url: https://toolhouse.ai/blog/connect-your-agents-to-any-workflow-with-callbacks-and-last-agent-message
source: toolhouse.ai/blog
---

# Connect your Agents to any workflow with Callbacks and Last Agent Message

_Published 2025-03-27 — [Original post](https://toolhouse.ai/blog/connect-your-agents-to-any-workflow-with-callbacks-and-last-agent-message)_

Connect your Agents to any workflow with Callbacks and Last Agent Message We made Agents API even easier to integrate with workflow automation tools. Mar 27, 2025 4 minutes Daniele Bernardi We're thrilled to announce the expansion of Agent Runs, a game-changing feature that has revolutionized the way developers and power users interact with Toolhouse agents. Developers ran 20,000 Agent Runs in just a month from the release of Agents, and the number keeps growing.

Developers have built many use cases, including sales assistants, marketing agents, investment analysts, and more. Today we're giving Agent Runs and Schedules two new powerful tools: Callbacks and Last Agent Messages. This new functionality is available to day to current users and new users who sign up for Toolhouse . Callbacks: unlocking workflow automation everywhere Callbacks allow agents to autonomously call a service after completing their task, enabling developers to trigger workflows outside of Toolhouse, send logging information or notifications to existing services, or integrate with external APIs and webhooks.

You can specify a callback in your Agent Run API by passing a callback_url parameter. If you use Schedules, you can also call your callback every time the agent completes its scheduled run. curl "https://api.toolhouse.ai/v1/agent-runs" \ - H "Authorization: Bearer $YOUR_TOOLHOUSE_API_KEY" \ -- json '{ "callback_url" : "https://webhooks.example.com/my-callback-service" "chat_id" : "your_chat_id" , "vars" : { "name" : "John Doe" } } ' Imagine being able to automate complex processes, such as triggering a workflow in Airflow or sending a notification to a Slack channel, all without manual intervention.

Callbacks make this possible, giving you the flexibility to create customized workflows that meet their specific needs. Last agent message: get the result, not the full JSON history In addition to Callbacks, we've also improved to the response from an Agent Run. The new last_agent_message field returns the last message in the agent history, making it easier for developers to extract the result of the Agent Run without having to perform complex array manipulation or JSON parsing.

This enhancement is particularly useful for developers who integrate Toolhouse into their existing automation workflows like Zapier, Gumloop, or Make. By providing a simpler and more convenient way to access the outcome of an Agent Run, we're saving developers time and effort, and enabling them to focus on building more sophisticated and automated workflows. Simplicity means more power Callbacks and Last Agent Message empower developers and power users to automate and streamline their workflows anywhere they choose to build them.

With these new capabilities, you can: Automate complex processes and workflows Integrate Toolhouse with external APIs and webhooks Trigger workflows outside of Toolhouse Send logging information or notifications to existing services Simplify your development workflow with improved API functionality We're excited to see the innovative ways you'll use these new capabilities to take your automation workflows to the next level.

Stay tuned for more updates and announcements, and happy automating! ‹ A simpler way to add attachments to context Bring your friends, earn $$$ › Docs Pricing Community Business Start Building Don't build agents. Delegate work. ')"> ')"> ')"> Product Docs Pricing Compare Base44 Lindy Sana Zapier Company About Careers Privacy Terms Funded by the European Union NextGenerationEU © 2026 Toolhouse Technologies, Inc.

All rights reserved
