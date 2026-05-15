---
title: "Introducing Toolhouse Schedules"
slug: introducing-toolhouse-schedules
date: 2025-02-03
url: https://toolhouse.ai/blog/introducing-toolhouse-schedules
source: toolhouse.ai/blog
---

# Introducing Toolhouse Schedules

_Published 2025-02-03 — [Original post](https://toolhouse.ai/blog/introducing-toolhouse-schedules)_

introducing-toolhouse-schedules Introducing Toolhouse Schedules Today we're super stoked to announce a powerful new feature. A gift that keeps on giving, designed to increase the value of your AI prompts super-powered by function calling: Schedules! Schedules empowers you to automate both full-fledged agents and simple AI prompts, running them on demand or at specified intervals.

Feb 3, 2025 4 minutes Orlando Kalossakas Today we're super stoked to announce a powerful new feature. A gift that keeps on giving, designed to increase the value of your AI prompts super-powered by function calling: Schedules ! Think of it like a timer for the AI world. Schedules empowers you to automate both full-fledged agents and simple AI prompts, running them on demand or at specified intervals.

Schedules takes the power of agents and combines it with the flexibility of scheduled execution. This means you can automate those repetitive tasks, like scraping data, filtering emails, or even creating memes, without lifting a finger. But Schedules goes beyond just agents. You can also schedule individual AI prompts, making it incredibly versatile for a wide range of use cases.

The ability to automate both complex agents and simple prompts opens up a world of possibilities. How does it work If you haven't checked the video embedded above, you should! If you prefer to see some code, continue below! Each Schedule you set up, creates a timer on an Agent Run via API, in fact, the difference between Scheduleds and Agent Runs is that Agent Runs run once immediately, while Scheduled runs only run at a given cadence.

A cadence can be repeat or one time. Just like Agent Runs, you can optionally specify a bundle to further tailor the functionality of your agent, as well as a Toolhouse ID metadata. Here's a JavaScript example from our docs, notice that you have to create a prompt via Prompt Studio first in this example, but you can also do it programmatically via API async function createAgentRun ( toolhouseApiKey , chatId ) { try { const url = 'https://api.toolhouse.ai/v1/agent-runs' ; //Endpoint to create an agent run const headers = { 'Authorization' : `Bearer ${ toolhouseApiKey } ` , 'Content-Type' : 'application/json' , } ; const body = JSON .

stringify ( { 'chat_id' : chatId , 'cadence' : '0 17 * * 0' , // This is cron notation, translates to At 17:00 on Sunday. } ) ; const response = await fetch ( url , { method : 'POST' , headers : headers , body : body , } ) ; if ( response . ok ) { const data = await response . json ( ) ; console . log ( data ) ; } else { console . error ( 'Failed to retrieve data:' , response .

status , response . statusText ) ; } } catch ( error ) { console . error ( 'An error occurred:' , error ) ; } } // Example usage const toolhouseApiKey = 'YOUR_TOOLHOUSE_API_KEY' ; const chatId = 'your_chat_id' ; //Get this from the Prompt Studio await createAgentRun ( toolhouseApiKey , chatId ) ; Imagine some uses cases Automated reporting: Schedule an agent to gather data from various websites and generate a report every morning.

Regular content creation: Schedule prompts to generate social media updates or blog post drafts on a daily or weekly basis. Proactive monitoring: Schedule an agent to monitor website performance and alert you to any issues. More Work for AI, Less Work for you Schedules broadens the utility of AI, helping individuals save time on everyday tasks while providing businesses with new opportunities for automation and engagement.

We're incredibly excited to see what you'll create with this powerful new feature! As always, this is an evolving feature, and we encourage you to share your feedback so we can continue to improve and expand its capabilities. Ciao, Toolhouse Team ‹ Agent Studio now supports variables Free LLM usage, Prompt Studio, Agent Runs, and more! › Docs Pricing Community Business Start Building Don't build agents.

Delegate work. ')"> ')"> ')"> Product Docs Pricing Compare Base44 Lindy Sana Zapier Company About Careers Privacy Terms Funded by the European Union NextGenerationEU © 2026 Toolhouse Technologies, Inc. All rights reserved
