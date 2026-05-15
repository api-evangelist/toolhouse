---
title: "Toolhouse: the AI developer's unfair advantage"
slug: ai-developers-unfair-advantage
date: 2024-08-10
url: https://toolhouse.ai/blog/ai-developers-unfair-advantage
source: toolhouse.ai/blog
---

# Toolhouse: the AI developer's unfair advantage

_Published 2024-08-10 — [Original post](https://toolhouse.ai/blog/ai-developers-unfair-advantage)_

Toolhouse: the AI developer's unfair advantage Toolhouse: the AI developer's unfair advantage Despite all the buzz around AI, building actually useful agents is hard. It’s just as hard as writing and maintaining API integrations before all the ecosystem of developer tools matured. If you're not deep in the world of LLMs you may not appreciate that all these models are limited, and that popular frameworks still don’t save you from the effort of working around those limitations.

You will need to equip your agents with tools that extend the basic functionality of its underlying LLMs. Aug 10, 2024 5 minutes Daniele Bernardi Despite all the buzz around AI, building actually useful agents is hard. It’s just as hard as writing and maintaining API integrations before all the ecosystem of developer tools matured. If you're not deep in the world of LLMs you may not appreciate that all these models are limited, and that popular frameworks still don’t save you from the effort of working around those limitations.

You will need to equip your agents with tools that extend the basic functionality of its underlying LLMs. You might be asking yourself: Agents? Tools? What are you talking about? Glad you asked! What LLMs cannot do LLMs are trained on a controlled, extremely specific set of data. Therefore, LLMs have to knowledge of current events, and they’re not able to see what’s happening outside of their knowledge.

Try to ask an LLM for the current time, and see it fail: There’s much more that an LLM cannot do: they can’t fully browse the internet; they can’t look into your calendar; they can’t send the emails they write for you or run the code they can generate for you. What’s more, they can’t remember what you said if you start a new conversation. So, why your favorite AI notetakers work?

They’re clearly able to plug LLMs and calendars together. That is done using tools (sometimes known as function calling ). What are tools and why do LLMs need them Think of tools as plugins for your LLMs. A tool is code you build, host, and run on your environment. You make the LLM aware of this code, so that it can ask you to execute it when needed. For example, LLMs are notoriously bad at doing math.

You could tell the LLM that they can call a math tool whenever they need help with calculations. Thanks to its reasoning capabilities, the LLM will understand that it cannot perform an accurate calculation and it will call your tool instead. Tools can also be used to equip LLMs with live data, or to perform actions like browsing the web or sending emails (and much more).

The problem with tools The concept of tools sound easy on the surface, but their implementation is actually tricky and more complex that you may imagine. Here’s why: You need to build the tool. Tools are extensions that live in your codebase and are ran in your infrastructure. This means you’ll now have additional code you’ll need to maintain. Usually, tools constitute the majority of the AI-related code.

You need to make sure the tool is safe to run in production. In our prior example may be tempted to simply use an eval to return the result of an equation, but evals are not safe. What if the user can exploit it to run malicious code? What if the LLM brings the eval to break your code? Those are just some of the considerations you need to take into account when you have to put your tool in the hands of actual users.

You need to create the right prompt in the right format for each LLM you want to use. Your LLM will not know about your tools unless you clearly provide an explanation. So, in addition to your actual tool code, you will need to provide a JSON Schema with each tool and their arguments. Each entry should be clearly described — this basically requires good prompt engineering skills in order to trigger the right behavior.

And if you switch between LLMs, both the format and the prompt needs to change. ChatGPT, Claude, Gemini, and Command-r all have incompatible tool schema definitions, so you’ll need to rewrite the same thing all over. Prompts make a ton of difference between LLM, so what works for ChatGPT may not work for Llama, which means that you’ll need to create different prompts for the same tool.

You need to check that the LLM did not hallucinate on the tool call. The LLM has decided to call a tool. When using tools, LLMs are prone to hallucinate; for example, they can misspell the function name, and call a function that does not exist in your code. How do you handle that? This needs a lot of boilerplate code. You need to return the result in the right format.

Assuming everything goes well, you’ll need to package the response in the format required by the LLM provider you are using. Not only this, but you also need to ensure that the tool response does not waste precious tokens. For example, suppose you’re building a tool to retrieve the contents of a page; its output will be the entire page, including its HTML code, CSS files, and some JavaScript.

If LLM reads all that, it may more prone to hallucinate; even if it does, you are creating more input tokens than needed. You’ll need to strip all the unnecessary details, which is non trivial. Real pain from real world experiences When building serious AI experiences, developers face significant pain points. We’ve felt this pain firsthand. After building countless tools, it quickly became apparent that we were wasting precious hours—hours that should have been spent perfecting a smooth user experience, instead lost in the weeds of integration with 3rd party systems.

Why does it have to be this way? Imagine spending your day writing code - only to be derailed by convoluted integration processes. Instead of innovating, you end up wrestling with tools that aren't working as you would expect. It’s not just about getting tools to work —it’s about giving developers the freedom to focus on what truly matters: A great developer experience.

Engineers deserve a developer experience that’s as delightful as it is powerful , one that allows them to craft good user experiences using code that should work across any LLM, and with just a few lines of code. Did someone say great developer experience? Enter Toolhouse! Toolhouse was born out of a need to empower developers like you. It’s the world’s first marketplace of AI tools—think “npm install” but for AI function calling, also known as tool use.

With just three lines of code , Toolhouse unlocks a world of knowledge and actions for your AI experiences, compatible with any model and any provider. Let’s go over some scenarios: Scenario 1 : You’re building an AI assistant that needs to tap into real-time data from a variety of sources. Without Toolhouse , you’d have to hunt down APIs, write custom integration code, and pray everything works as expected.

With Toolhouse, it’s as simple as selecting the tools you need and integrating them in seconds. Scenario 2 : Imagine you need to integrate a specific data source or trading algorithm into your chatbot. Instead of spending hours configuring and testing a third-party library, you can simply “npm install” the chosen tool from Toolhouse. In just three lines of code, your chatbot is now ready to go!

Scenario 3 : You’re tasked with building a content moderation system for a social platform. Traditionally, you’d cobble together various services, hoping they fit. Toolhouse lets you seamlessly integrate multiple moderation tools, with configurable moderation logic, ensuring your platform is safe and reliable—again, in just three lines of code. And it doesn’t stop there.

Toolhouse also provides a platform for developers to distribute and monetize their tools. If you’ve built something amazing, why not share it with the world and get paid for it? Toolhouse is built by developers for developers We’re incredibly excited to see what you’ll build with Toolhouse. Whether you’re enhancing an LLM with specialized knowledge or enabling complex actions, Toolhouse is here to simplify the process.

No more wasted time, no more integration nightmares—just pure, unbridled creativity. Please join us on Discord or sign-up to our beta and get $150 credits for $1 ( https://waitlist.toolhouse.ai/buy/052c6026-9b1e-42cf-b54c-049c60a56b42 ) ‹ Yes, you can build your pitch deck with AI. Just do it right. Docs Pricing Community Business Start Building Don't build agents.

Delegate work. ')"> ')"> ')"> Product Docs Pricing Compare Base44 Lindy Sana Zapier Company About Careers Privacy Terms Funded by the European Union NextGenerationEU © 2026 Toolhouse Technologies, Inc. All rights reserved
