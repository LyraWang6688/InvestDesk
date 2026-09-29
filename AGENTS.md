# InvestDesk Agent Rules

This project is no longer a Next.js web app. The old frontend code has been removed.

Current source of truth:

- `docs/architecture.md`

Current product direction:

- Feishu Base is the database, application UI, and Agent center.
- InvestDesk Skills define structured data protocols for holdings, transactions, insights, and watchlist rules.
- The self-developed system should focus on initialization, template setup, and real-time quote/NAV synchronization.
- The future codebase should be a lightweight worker/CLI project, likely `Node.js + TypeScript + Playwright + lark-cli`.

Do not recreate the old Next.js frontend unless the user explicitly asks for it.

When adding implementation later, prefer a worker-oriented structure:

```text
src/
  cli/
  feishu/
  instruments/
  quotes/
  jobs/
```

Keep user-facing investment recommendations phrased as reminders or review prompts, not automatic buy/sell instructions.
