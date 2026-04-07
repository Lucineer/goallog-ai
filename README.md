# GoalLog.ai — AI Goal Tracker

You set goals. You forget them. This is a simple, open-source agent that helps you track them.

An AI-powered goal tracker for consistent progress reviews and accountability, built as a single Cloudflare Worker.

---

## Why this exists

Most goal trackers are either static to-do lists or locked-down SaaS platforms. This is an alternative: a minimal agent you can run yourself. Your data stays in your infrastructure, and you control the logic.

---

## Try It Now

Test the public instance. No login required:
https://goallog-ai.casey-digennaro.workers.dev

---

## How It Works

This is a stateless agent runtime for Cloudflare Workers. You interact with it via a simple web interface. It stores your goal history in a Cloudflare KV namespace and uses your AI API key to generate check-in prompts and reviews.

**Key Features:**
*   **Self-Hosted Data:** All data persists in your own Cloudflare KV store. No external databases or third-party servers.
*   **Configurable Coaching:** The agent's personality and check-in questions are defined in plain text within the Worker. You can edit them in minutes.
*   **Bring Your Own AI Key:** Connect to OpenAI, Anthropic, or other compatible providers. You pay your provider directly.
*   **Zero Dependencies:** The entire application is contained in one file (`worker.ts`). There is no build step or npm installation.
*   **Fork-First Design:** This codebase is intended to be forked and adapted to your specific needs.

**An Honest Limitation:** This tool requires manual check-ins. It won't automatically track your habits or send push notifications. Its value comes from the structured reflection you perform when you use it.

---

## Quick Start

1.  **Fork** this repository.
2.  **Deploy** it to Cloudflare Workers.
3.  **Configure** your `AI_API_KEY` as a Worker secret and update the `coachingPrompt` in `worker.ts` if desired.

That's it. Your instance is live.

---

## Architecture

GoalLog.ai is a single-script application built for Cloudflare Workers. It uses:
*   **Cloudflare Workers** as the runtime.
*   **Cloudflare KV** for persistent goal history storage.
*   **Structured prompts** sent to the AI provider of your choice.

All logic is in `worker.ts`. The web interface is basic HTML and vanilla JavaScript served from the same Worker.

---

## Contributing

This project follows the Cocapn Fleet's fork-first philosophy. The most valuable contribution is to fork the repository and build the version you need. If you have a change that benefits the core base, a pull request is welcome.

---

## License

MIT License.

---

Superinstance & Lucineer (DiGennaro et al.).

<div align="center">
  <a href="https://the-fleet.casey-digennaro.workers.dev">The Fleet</a> •
  <a href="https://cocapn.ai">Cocapn</a>
</div>