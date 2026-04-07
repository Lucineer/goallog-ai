# GoalLog.ai — AI Goal Tracker ✨

You set a goal. An AI agent checks in with you on the schedule you choose. There are no spam reminders, progress graphs, or dashboards. It provides quiet, consistent accountability.

Test the live instance:  
https://goallog-ai.casey-digennaro.workers.dev

## Why This Exists
Most goal trackers become a chore. This one avoids that by doing a single job: asking you a good question at the right time and remembering your answer.

## Quick Start
1.  **Fork** this repository.
2.  **Deploy** it directly to Cloudflare Workers. No local setup is needed.
3.  **Add** your `AI_API_KEY` as a Worker secret. Optionally, edit the agent's coaching prompt.

Your self-hosted goal tracker will be running in under two minutes.

## Features
*   Your goal history is stored only in your private Cloudflare KV store.
*   Fully customizable coaching prompt. Adjust the tone to what works for you.
*   Use any compatible AI API key (OpenAI, Anthropic, Groq, etc.).
*   Zero dependencies and no build step. The entire application is one file.
*   Fork-first design. This is a tool you copy and own, not a subscription.
*   No user accounts, logins, or third-party tracking.
*   Runs on Cloudflare's edge network with no external database.
*   **One honest limitation:** Your goal history is bound by Cloudflare KV's 10MB per namespace limit.

## How It Is Different
1.  It does not send email, request social invites, or feature productivity leaderboards.
2.  After you deploy it, it is your agent. It cannot be altered, shut down, or monetized by anyone else.
3.  It handles one goal at a time. It does not try to be a multi-purpose life dashboard.

## Architecture
This is a single-file Cloudflare Worker. All application logic, routing, frontend HTML, and AI prompts are contained within `worker.ts`.

## License
MIT License. Use, modify, and distribute this code freely.

---

<div style="text-align:center;padding:16px;color:#64748b;font-size:.8rem"><a href="https://the-fleet.casey-digennaro.workers.dev" style="color:#64748b">The Fleet</a> &middot; <a href="https://cocapn.ai" style="color:#64748b">Cocapn</a></div>