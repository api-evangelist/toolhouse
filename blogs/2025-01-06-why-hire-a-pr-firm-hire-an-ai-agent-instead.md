---
title: "Why hire a PR firm? Hire an AI agent instead!"
slug: why-hire-a-pr-firm-hire-an-ai-agent-instead
date: 2025-01-06
url: https://toolhouse.ai/blog/why-hire-a-pr-firm-hire-an-ai-agent-instead
source: toolhouse.ai/blog
---

# Why hire a PR firm? Hire an AI agent instead!

_Published 2025-01-06 — [Original post](https://toolhouse.ai/blog/why-hire-a-pr-firm-hire-an-ai-agent-instead)_

Why hire a PR firm? Hire an AI agent instead! Why hire a PR firm? Hire an AI agent instead! AI is significantly reducing the effort and complexity of any project. Apps that required large teams and budgets can now be built in days, if not hours. An example of this are so called social listening platforms. Social listening apps can monitor your brand’s accounts and provide valuable insights about the overall sentiment of your followers.

These apps are usually costly and sometimes not entirely fit for the purpose you have in mind. What if you only wanted to get a daily digest of people talking about your company? AI is significantly reducing the effort and complexity of any project. Apps that required large teams and budgets can now be built in days, if not hours. An example of this are so called social listening platforms.

Social listening apps can monitor your brand’s accounts and provide valuable insights about the overall sentiment of your followers. These apps are usually costly and sometimes not entirely fit for the purpose you have in mind. What if you only wanted to get a daily digest of people talking about your company? Jan 6, 2025 2 minutes Fabio Pulvirenti tl;dr: Click here to clone and run an agent that monitors X for mentions of your favorite X accounts and categorizes the sentiment of each tweet.

Introduction AI is significantly reducing the effort and complexity of any project. Apps that required large teams and budgets can now be built in days, if not hours. An example of this are so called social listening platforms. Social listening apps can monitor your brand’s accounts and provide valuable insights about the overall sentiment of your followers. These apps are usually costly and sometimes not entirely fit for the purpose you have in mind.

What if you only wanted to get a daily digest of people talking about your company? What about AI? AI models can do a lot, but they lack the fundamental access to the real world. If you wanted an AI agent to check the pulse of your community on X, you’d need the following: A good AI model Access to the X API (currently $4,200/month) Code to integrate the X API into your AI model A set of prompts to ensure the AI models knows how to call the X API, and what to do in case it doesn’t get the right results or if the X API are down (trust me, they go down) A backend where you can host and run your integration That’s a ton!

You’re basically building a company, not a tool. Who can afford to spend time and effort mastering prompt engineering? How to you ensure repeatable results? And do you have $4,200 a month to spare for Elon? A better way of building Agentic AI Thanks to Toolhouse, we can reduce all this effort to just three lines of code. With Toolhouse, every AI model receives “superpowers” – special tools that can free AI of their constraints.

Your agent can now browse the web, or get the latest information outside of the model’s native knowledge, and obviously get the latest posts from people mentioning your brand. All this in just a few lines of code th = Toolhouse() completion_response = client.chat.completions.create(tools=th.get_tools(), messages=msgs) response = th.run_tools(completion_response) Behind the scenes, we do this: We talk to your AI agent to give it “superpowers” – i.e.

tools to browse the internet, look up posts on X, get previous chats from this user, and more. We dynamically adapt the list of tools to the specific model provider you’re using. This is needed because each provider (OpenAI, Anthropic, etc) need to be instructed in ways that are incompatible among one another. We dynamically prompt the agent with precise instructions on how to use each “superpower” Should the agent decide to use a tool, we take the request from the agent, execute it on our backend, and return the response to the agent We repeat these operations if the agent wants to use more tools All we need is a Good Prompt With our AI code reduced to just a mere three lines of code, we only need the right prompt for the task.

Toolhouse makes this a breeze too. We created a blueprint you can clone – this is actually the prompt we use daily to monitor our Toolhouse accounts. This works well on Claude 3.5 Sonnet. Based on the AI model your agent uses, you may want to modify the prompt, but here’s what our agent will do: It will get the list of accounts you want to monitor It will perform one X search per account It will read the results and categorize it into positive coverage, negative coverage, requests for help, and other noteworthy mentions It will then send an email to a distribution list Let’s take a look at the prompt itself: Compile a digest of tweets regarding Toolhouse ( @toolhouseai ): Get tweets about @toolhouseai , @i_am_daniele , @sunglassesface , or @aaishika .

Perform a separate search_x search for each account. Read each tweet and add it to one of those following categories: positive coverage, negative coverage, request for help, other. Exclude tweets authored by the accounts I gave you, so you can focus on people mentioning those accounts. Discard tweets older than 24 hours (make sure to call current_time to compute the time difference.) If a section contains no tweets, make sure to say that clearly.

Send email with this digest to daniele@toolhouse.ai . make sure to show each tweet you selected. make sure to format it nicely with HTML. If a tweet has images, wrap the images in <img> tags so they can show up in the email. Make sure each tweet is clickable by compiling an URL from its conversation ID. For example, if the conversation ID is 2183472987123981, the link should be https://x.com/t/status/2183472987123981 .

The subject line should be: “Toolhouse X Digest”. You may wonder: how did you get to write such a succinct, plain English prompt, and make it work all the time? Well, it’s easier than you think. Tips to write Good Prompts Start small, expand later. You may be tempted to write a very detailed prompt with strict instructions. When do you that, you’ll realize that the model will eventually still find ways to override your instructions.

Start with a minimum set of instructions, and test the model’s behavior over multiple runs to see if they consistently yield the same result. Trust your agent. AI models evolved very quickly, and their agentic capabilities became more reliable over the past year. More so, Toolhouse feeds optimized prompts for each one of the available tools, which further aligns the agent to perform your desired behavior.

As a result, Agents can not reason better than ever, which in turn lets you significantly shorten your user prompts. Forget the complexity. Chain of thought, few shots, ReAct… They’re all so 2024. Toolhouse wraps the complexity of running agents into just three lines of code, so you can build more sophisticated use cases with little effort and no specialized knowledge.

Give this agent a go Use this Toolhouse blueprint to create your own version of this social media monitoring agent. All you have to do is to sign up for Toolhouse, then click Run. Our Playground is free to use, which means you won’t spend LLM tokens to run these prompts. Let us know what you think on Discord or on X at @ToolhouseAI – we’re all ears thanks to our social media monitoring agent!

‹ Summarizing AI at CES 2025 with AI AI Agents › Docs Pricing Community Business Start Building Don't build agents. Delegate work. ')"> ')"> ')"> Product Docs Pricing Compare Base44 Lindy Sana Zapier Company About Careers Privacy Terms Funded by the European Union NextGenerationEU © 2026 Toolhouse Technologies, Inc. All rights reserved
