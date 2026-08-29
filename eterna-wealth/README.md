# Eterna Wealth — The Portfolio That Explains Itself

### What if every number on your dashboard could tell you what to *do* about it?

That's Eterna Wealth. Click any metric, chart point, or holding — and instead of a definition, you get a plain-English story: what it means, why it matters, which holdings are driving it, and the **one move to make**. A dashboard reports. Eterna advises.

**🔗 [Open the live demo →](https://rkac12288-bot.github.io/AI-Platforms-/eterna-wealth/)** &nbsp;·&nbsp; runs entirely in your browser, no install.

![Status](https://img.shields.io/badge/status-demo-e0a84a) ![Build](https://img.shields.io/badge/build-none-3db876) ![Dependencies](https://img.shields.io/badge/dependencies-zero%20backend-22b8a8) ![File](https://img.shields.io/badge/single--file-HTML-4a8ae0)

---

## 🎬 See it in 12 seconds

<!-- Record a 12s clip (click a metric → story opens → switch roles) and save as demo.gif here: -->
![Eterna Wealth demo](./demo.gif)

<!-- Video walkthrough: upload to YouTube/Loom, then uncomment and set the URL + thumbnail:
[![Watch the walkthrough](./demo-thumbnail.png)](VIDEO_URL)
-->

> One click turns a cold number into a decision. That's the whole product — and the demo above shows it without a single word of narration.

---

## The problem everyone in finance knows

Every wealth dashboard throws the same wall of numbers at you — Sharpe, VaR, drawdown, IRR — and leaves you asking the only question that matters: **"…so what do I actually do?"**

Answering it today takes an analyst in the room. That doesn't scale, it slows every decision, and it means the CEO, the CFO, and the portfolio manager are all squinting at the same screen that was built for none of them.

## The idea: storytelling-first intelligence

Eterna answers "what do I do?" on **every single number**. Click anything and it unfolds a four-part story:

1. **What it is** — in plain English, in context. No jargon.
2. **Why it matters** — the stakes: a mandate breached, a risk limit, a funding gap.
3. **What's driving it** — the *exact* holdings responsible, named.
4. **The action that moves it** — the single next step, spelled out.

It never just shows you the number. It tells you what to do about it — and every story ends in a decision.

## One portfolio, three lenses

The same book reframes itself for whoever's in the room. One click switches the entire platform's voice:

- **CEO** → a strategic briefing: the headline, the risks, the one decision for the board.
- **CFO** → P&L, fees, provisions, and liquidity: every dollar accounted for.
- **PM** → trade-level detail: factor exposure, drift, and specific buy/sell calls.

One source of truth, told three ways. Nobody has to translate for anybody.

---

## What it actually does

Beyond the storytelling, Eterna is a full portfolio operating system:

**🏛 Executive Cockpit** — a story-led daily health check. Every KPI is clickable and opens its full narrative plus attribution — which assets moved it and why.

**🎭 Role Lenses (CEO / CFO / PM)** — the entire interface reframes to the reader's job. Same data, three completely different framings, one click apart.

**💬 AI Analyst that never breaks** — ask anything and get a portfolio-specific answer. It calls a language model for narration, but if that's unreachable (offline, opened as a local file, API down), a **local analysis engine** takes over and answers from the same live data. The AI is an enhancement, never a hard dependency — so it *works on a plane*.

**📄 One-click board reporting** — designed daily briefings and full monthly/quarterly board decks, generated straight from the live portfolio. Work that took an analyst half a day is now a button.

**🏦 Credit Monitor** — IFRS 9 staging, credit gauges, and provisioning, with plain-English explanations of what each credit event means for the book.

**📊 Analytics suite** — a Monte Carlo simulation (a range of possible futures from real return/volatility statistics) and a real-data walk-forward test (decide week-by-week on real prices, no look-ahead). **Built to plug into live market-data APIs in production.**

**🏗️ How It's Built** — in-app documentation of the AI pipeline (context → model call → parse → fallback), with a real request/response, so the engineering is transparent.

**👥 Team Layer** — chat, a decision log with voting, and pinned notes, so the whole team works in one place.

**🧭 Guided Tour** — a spotlight walkthrough that onboards a first-time user in under a minute.

---

## Why you can trust what you see

Good analytics earn trust by showing their work and never over-claiming. Eterna is explicit about what's what:

- ✅ **Real** — all in-browser computation: every metric, chart, drill-down story, and the local AI engine. The walk-forward test runs on **real prices you supply**.
- 🟡 **Demo** — the sample portfolio holdings and NAVs are generated demo data, shown by a persistent **"DEMO DATA"** badge on every screen.
- ⚠️ **Illustrative** — the institutional data connectors (Bloomberg, ANBIMA, PostgreSQL, Preqin) on the Settings page show how the platform *would* wire into production sources. They're clearly labeled as illustrative and make no real connections in this demo.

No black boxes, no numbers presented as more real than they are.

## Tech stack

- **Vanilla JavaScript** — no framework, no bundler, no build step
- **Chart.js** for all data visualization
- **Claude API** for AI narration (optional; local fallback engine when unavailable)
- **~9,500 lines**, one self-contained HTML file, no backend, no database

## Run it yourself

**Just open the file.** Download `index.html`, open it in any modern browser, and the whole platform runs client-side — no install, no setup. Try it offline to watch the AI fallback engine take over seamlessly.

## Deploy your own copy (GitHub Pages, free)

1. Rename the platform file to **`index.html`** and put it in this folder.
2. In the repository: **Settings → Pages → Source: Deploy from a branch → Branch `main` / `root` → Save.**
3. Wait ~1 minute — your live demo appears at
   `https://rkac12288-bot.github.io/AI-Platforms-/eterna-wealth/`

Any folder with an `index.html` is published automatically, so every platform in this repo gets its own clean, shareable live link.

## Design principles

🎯 **Storytelling over data-dumps** — every number explains itself
👥 **Built for the whole room** — CEO, CFO, and PM each get their own lens
🛡️ **Graceful degradation** — the AI is an enhancement, never a hard dependency
🔍 **Intellectual honesty** — demo data, illustrative connectors, and simulations are all labeled as such

---

*Part of my [AI Platforms](../) collection — where I explore how AI can make complex, high-stakes data genuinely legible to the people who have to act on it.*
