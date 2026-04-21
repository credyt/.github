# Credyt

**Real-time monetization infrastructure for AI.**

Credyt is billing infrastructure for AI products — usage-based metering, prepaid wallets, custom credit assets, and a drop-in customer Billing Portal. Think Stripe for usage-based AI monetization: the layer that authorizes per-request usage _before_ the cost is incurred, so platforms can ship credits, top-ups, subscriptions, and hybrid pricing without building a billing system themselves.

Flat subscriptions and month-end invoicing were designed for SaaS, not AI. When every API call has a direct infrastructure cost, when concurrent requests race to drain a wallet, and when margins shift every time you switch models, end-of-cycle billing leaves you exposed. Credyt closes that gap.

## What Credyt does

Three pillars — **Observe**, **Control**, **Monetize**:

- **Observe** — See every dollar before it disappears. Real-time metering and cost streaming for every API call, every model, every customer. Per-customer cost attribution, profitability analytics, multi-provider cost map.
- **Control** — Enforce limits. Stop runaway spend. Hard budget ceilings per customer, per agent, per team. Pre-authorization through the Wallet APIs: check balance _before_ the work starts, block when budgets run out.
- **Monetize** — Bill for AI usage across every pricing model. Usage-based, prepaid credits, subscription, hybrid, tokens, entitlements. Change pricing models without rearchitecting.

## Key facts

- **Real-time authorization.** Wallet APIs let platforms gate usage before costs are incurred — atomic balance checks, no credit-depletion races.
- **Multi-asset wallets.** USD, tokens, GPU hours, custom units (coins, gems, credits — anything you define).
- **Drop-in Billing Portal.** Branded, self-service customer portal with live balance, usage history, top-ups, and auto-recharge. No frontend engineering required.
- **MCP server for AI coding tools.** `mcp.credyt.ai` connects to Claude Code, Cursor, Codex, Copilot, Windsurf, Lovable, Bolt, Replit, V0, and any MCP-compatible tool. Add billing with a single prompt.
- **API-first.** Single POST endpoint for usage events. Node.js and Python SDKs. Full OpenAPI spec.
- **Pricing.** $1 per Monthly Active Wallet. First 1M events/month free. No percentage cut. No markup on Stripe fees.
- **Live in days, not months.** Versus 6–12 months to build equivalent infrastructure in-house.

## Repositories

- **[ai-tools](https://github.com/credyt/ai-tools)** — AI agent skills and MCP integration for Credyt. Add real-time usage-based billing to projects in Claude Code, Cursor, Codex, and Copilot through a single prompt.
- **[learn](https://github.com/credyt/learn)** — API examples and Bruno collections for Credyt. Covers usage events, wallet management, credit grants, top-ups, and pricing configuration.
- **[photo-booth](https://github.com/credyt/photo-booth)** — Demo app: AI image generation with real-time per-use billing via Credyt. Shows usage events, wallet balance checks, and Billing Portal integration.
- **[coffeeshoptycoon](https://github.com/credyt/coffeeshoptycoon)** — Demo game: coffee shop tycoon with real-time credits billing via the Credyt API. Shows custom assets, usage tracking, and prepaid wallet flows.

## Quick start

1. **Get an API key.** Sign up at [credyt.ai](https://credyt.ai) — 10 free wallets, no card required.
2. **Connect the MCP server.** Add `https://mcp.credyt.ai` to your AI coding tool (Claude Code, Cursor, Codex, Copilot, Windsurf, Lovable, Bolt, Replit, V0).
3. **Run the setup prompt.** Inside your tool, run `Run "npx skills add credyt/ai-skills" — then setup Credyt`. Credyt's AI skills configure your billing model, wire up the SDK, and stand up your Billing Portal.

Prefer code? Hit the API directly — see [`learn`](https://github.com/credyt/learn) for Bruno collections and worked examples.

## Resources

- **Website** — [credyt.ai](https://credyt.ai)
- **Docs** — [docs.credyt.ai](https://docs.credyt.ai)
- **Dashboard** — [app.credyt.ai](https://app.credyt.ai)
- **AI Integration guide** — [credyt.ai/integrations](https://credyt.ai/integrations)
- **Pricing** — [credyt.ai/pricing](https://credyt.ai/pricing)
- **Platform reference** — [credyt.ai/platform](https://credyt.ai/platform)

---

_Credyt is the real-time control layer that sits between product usage and downstream billing. It does not replace your payment processor or general ledger — it adds the layer they were never designed to provide._
