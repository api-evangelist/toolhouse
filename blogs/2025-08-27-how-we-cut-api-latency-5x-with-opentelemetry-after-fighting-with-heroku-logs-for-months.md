---
title: "How we cut API latency 5x after implementing OpenTelemetry"
slug: how-we-cut-api-latency-5x-with-opentelemetry-(after-fighting-with-heroku-logs-for-months)
date: 2025-08-27
url: https://toolhouse.ai/blog/how-we-cut-api-latency-5x-with-opentelemetry-(after-fighting-with-heroku-logs-for-months)
source: toolhouse.ai/blog
---

# How we cut API latency 5x after implementing OpenTelemetry

_Published 2025-08-27 — [Original post](https://toolhouse.ai/blog/how-we-cut-api-latency-5x-with-opentelemetry-(after-fighting-with-heroku-logs-for-months))_

How we cut API latency 5x after implementing OpenTelemetry After Fighting with Heroku Logs for months we implemented OTEL and reduced latency fivefold. Aug 27, 2025 4 minutes Toolhouse Engineering Team From “Just Vibes” to Observability At one point, our alerting system was so bad that I got a Slack notification because Heroku thought our gateway had thrown a 503.

I panicked, checked logs across dynos, and saw… nothing useful. Just uvicorn noise, the usual. INFO : 200 GET / INFO : 200 GET / health INFO : 200 GET / api / v1 / do - stuff No error stacktrace. No upstream correlation. Just vibes. After an hour of grepping around, I gave up, assumed it was one of those “weird edge cases,” and went back to browsing Reddit. That was our observability strategy: get alerted, shrug, and hope it doesn’t happen again.

The Problem Before OTEL Our setup was fragmented and brittle: Shallow alerts. BetterStack + Heroku would yell about 500s, but never told us *why* . Upstream errors cascaded down as 503s at the gateway, and we got noise instead of insight. Scattered logs Heroku dynos meant we were chasing logs across instances, often with exception handling swallowing the root cause.

Broken logging Python logging wasn’t even properly configured. We got `uvicorn` status lines and almost nothing from the actual business logic. Blind debugging With no traces, many errors got dismissed as freak accidents. We couldn’t even start debugging edge cases. Slow endpoints Some routes took multiple *seconds* . Not a great user experience: Users complained, tests dragged, shipping slowed because it took more to refresh.

Result: we were flying blind. Incidents = wasted time, confused engineers, unhappy customers. Why OpenTelemetry The solution we needed was coming to become clear. We needed a way to aggregate logs and other system metrics into a clean interface that would allow us to better understand and react to incidents and alerts, whilst making stronger strategic decisions around our products.

As open source advocates we wanted a solution that was open source and vendor neutral, so we had the flexibility to change providers at will, in order to get the best value for the company. We wanted a vendor-neutral was non-negotiable, no lock-in, no surprise bills. OpenTelemetry fit perfectly: logs + traces + metrics, open source, wide support. We didn’t want to self-host a full stack (we’re scrappy), so Grafana Cloud’s free tier became our backend.

Their FREE tier was good for us (although we sometime feel like we’re abusing it). It covers the volume of logs we are generating, whilst also allowing us to implement tracing, which solves the issue of getting more visibility into the system’s performance. There was also a clear implementation path using open telemetry instrumentation, which meant we did not need to make huge code changes.

The Rollout Our initial implementation involved a single telemetry.py file in our backend, which implemented a proof of concept tracing system using jaeger. Initially this was disabled by a feature flag, but after encountering an issue with BetterStack causing false positive alerts, we ended up turning it on in production as a mitigation strategy. This immediately identified a number of issues that would otherwise have been hidden, which gave the leadership team confidence to move forwards with the full rollout.

The next goal was to fix logging, and enable OTLP (OpenTelemetry Protocol, the standardized network protocol used to define how telemetry data) exports of logs, so that we could correlate them with the new trace data. To handle the rest of the python services we basically copy/pasted and adapted this file and changed the instrumentation classes used to match the service dependencies.

This worked for the tool runtime and the code interpreter sandbox. In a table, this is chronologically what happened. Step Change Outcome 1 Add telemetry.py in backend First traces lit up 2 Turn on in prod (after BetterStack false alert) Confidence skyrocketed 3 Fix logging across 56 files Real logs, finally 4 Instrument tool runtime + code interpreter Coverage across Python services 5 Hack OTEL into Cloudflare Workers ( @microlabs/otel-cf-workers ) Full distributed tracing 6 Grafana dashboards + alerts No more “just vibes” alerts 7 (Next) Grafana Faro SDK for frontend Trace per user session Pitfalls Along the Way - The 56-file PR Migrating everything to logging.getLogger was painful.

But correlation was impossible without it. - Cloudflare Workers The official Node SDK didn’t work (missing APIs). Had to use @microlabs/otel-cf-workers - Vercel AI SDK Supposed to “just work.” Didn’t. Still off. F*** it. The Open Telemetry SDK handled the hard parts with log sinking and Grafana cloud required no extra config vs tracing. Wins: the ones we didn’t expect Many of the improvements we applied after seeing the metrics came from small improvements like using database connection pools and parallelizing API calls.

Initially, because our database ( hosted by Neon ), we had a significant round trip latency to initialize a database call. We managed to remove this by switching to a pool, which removed the cold start from initializing a TCP connection and SSL context, and removing the pre-flight statement to set the search path, which we replaced with a global permeant config change in our hosted PostgreSQL.

After these changes, the average SQL statement took ~20ms to run, significantly faster then the ~500ms before. This was actually faster then our redis implementation, which suffered from a ~25ms/r penalty, for the same reasons (TCP connection initialization and SSL context): we ended up adding a few lines to ensure our Redis clients used a connection pool which dropped the penalty to ~2-3ms/r, another order of magnitude improvement.

All in all Latency drops Adding connection pools cut DB calls from ~500ms to ~20ms. Redis went from ~25ms/r → ~2–3ms/r. Suddenly, SQL was faster than Redis (confused the whole #eng Slack). Architecture diagrams for free Grafana’s node graph auto-documented our system. Now invisible services look embarrassing, so everyone *want* to add instrumentation. Happier users Endpoints went from 1–2s to ~200–300ms.

Users noticed. Tests sped up. Everyone shipped faster. Lessons Learned We learned the good way: Logs without traces are useless. We had logs for months. Didn’t matter, they weren’t useful in times of crisis. Connection pools matter. Never underestimate the “boring” infra fixes. Observability isn’t optional. Without it, we were debugging our code as if we were blindfolded.

What’s Next We already use PostHog for a lot of front-end metrics but we need to implement proper Frontend tracing. In the future our next moves will be to deploy the Grafana Faro SDK in the frontend so that we can correlate traces per session and identify which endpoints are most commonly used by users so that we can target even more optimizations. Closing Overall, our OTEL rollout was a success.

Sure there were some minor issues along the way, but the situation has improved considerably compared to before, and we have a framework to understand the application: our OTEL rollout was just right for us. We fought SDK bugs, made monster PRs, and swore at Heroku logs: we went from shrugging at alerts to confidently tracing requests across the stack. If you’re still stuck with Heroku logs and BetterStack alerts, my advice: stop suffering.

Add OpenTelemetry. You’ll wonder how you ever shipped without it. Toolhouse Changelog August 2025 › Docs Pricing Community Business Start Building Don't build agents. Delegate work. ')"> ')"> ')"> Product Docs Pricing Compare Base44 Lindy Sana Zapier Company About Careers Privacy Terms Funded by the European Union NextGenerationEU © 2026 Toolhouse Technologies, Inc.

All rights reserved
