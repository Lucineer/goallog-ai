# GoalLog.ai — AI Goal Tracker

Track goals with an assistant that remembers context and adapts to you.

---

## Why this exists

Most goal trackers are rigid. They forget why you set a goal and don't adjust when life happens. This is a different approach: a stateless agent that works with your history, not against it.

## Try it now

Live instance: https://goallog-ai.casey-digennaro.workers.dev
No account or email required to test the core features.

---

## What it does

*   Tracks goals and habits with clean, structured endpoints.
*   Provides analytics on consistency and progress drift.
*   Uses AI to offer adaptive check-ins based on your tracking history.
*   Runs on Cloudflare Workers with zero dependencies.
*   Follows a BYOK (Bring Your Own Keys) model for AI providers.
*   Is designed to be forked and customized for your workflow.

## One Limitation

This is optimized for personal, low-to-moderate usage. While the Worker itself costs $0, your AI provider API calls are your responsibility and costs will scale with your usage.

---

## Quick Start

1.  Fork this repository.
2.  Deploy it to Cloudflare Workers.
3.  Add your AI provider API keys as environment variables.

All logic is in `worker.ts`. Adjust the coaching prompts, metrics, or endpoints there.

## How it works

GoalLog.ai is an agent runtime built for Cloudflare Workers. It uses the Worker's KV store for persistence and operates with stateless endpoints. You bring your own AI API keys, so your data never routes through a third-party server.

## License

MIT License. Superinstance & Lucineer (DiGennaro et al.).

---

<div align="center">
  <a href="https://the-fleet.casey-digennaro.workers.dev">The Fleet</a> • 
  <a href="https://cocapn.ai">Cocapn</a>
</div>