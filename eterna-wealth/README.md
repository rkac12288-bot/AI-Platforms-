# Eterna Wealth — Storytelling-First Portfolio Intelligence

> A single-file wealth management platform where every number explains itself. Click any metric, chart point, or holding and instead of a definition you get a story: what it is, why it matters, which assets are driving it, and the one action that moves it.

**🔗 Live demo:** `https://rkac12288-bot.github.io/AI-Platforms-/eterna-wealth/`
*(works once GitHub Pages is enabled on the repository — see the top-level README)*

![Status](https://img.shields.io/badge/status-demo-e0a84a) ![Build](https://img.shields.io/badge/build-none-3db876) ![Dependencies](https://img.shields.io/badge/dependencies-zero%20backend-22b8a8) ![File](https://img.shields.io/badge/single--file-HTML-4a8ae0)

---

## What it is

Eterna Wealth is an institutional-grade portfolio analytics platform built as a **single, self-contained HTML file** — no build step, no backend, no database. It reframes portfolio data the way a trusted analyst would explain it: in plain English, framed for whoever is reading (CEO, CFO, or portfolio manager), always ending in a decision.

The core idea is **storytelling-first intelligence**. Most dashboards throw dozens of metrics on a screen and leave the executive asking "…so what do I actually do?" Eterna answers that question on every number.

## Why it's interesting (the engineering)

- **Graceful AI degradation.** The AI analyst calls a language model for narration, but that call is an *enhancement, not a dependency*. If the network is down, the file is opened locally (CORS), or the API is unreachable, a deterministic **local analysis engine** takes over in-browser and produces a genuine, portfolio-specific answer — the user never sees an error. This is documented on the in-app **"How It's Built"** page with a real request/response.
- **Zero-install architecture.** One `.html` file. It opens anywhere — including offline on a plane — with all metrics, charts, backtests, and recommendations computed client-side.
- **Point-in-time honesty.** The Advice Backtest enforces no look-ahead bias in code: at each simulated month the recommendation engine is hard-blocked from seeing future data. Decide, act, *then* reveal the next period.
- **Intellectual honesty by design.** Demo data is clearly badged, illustrative data connectors are explicitly labeled, and simulated results are never presented as real market history.

## Features

| Area | What it does |
|------|-------------|
| **Executive Cockpit** | Story-led daily health check — click any KPI for the full narrative + attribution |
| **Role Lenses (CEO / CFO / PM)** | The same data reframed three ways — strategic, financial, or trade-level |
| **Storytelling Drill-Downs** | Click any metric, chart point, or holding for a plain-English 3-part story |
| **AI Analyst** | Ask anything; get portfolio-specific answers — with the on-device fallback engine |
| **Backtest & Validate** | Monte Carlo (10,000 paths), walk-forward, and statistical validation tests |
| **Advice Backtest** | A controlled experiment testing whether following the platform's own advice improves risk-adjusted results, with no hindsight |
| **Daily Reports** | One-click, board-ready briefings with the day's activity timeline |
| **Board Presentation** | Auto-generated monthly & quarterly board decks |
| **Credit Monitor** | IFRS 9 staging, credit gauges, provisioning |
| **Team Layer** | Chat, decision log with voting, and pinned notes |
| **Guided Tour** | A spotlight walkthrough that onboards new users |

## Tech stack

- **Vanilla JavaScript** — no framework, no bundler
- **Chart.js** for all data visualization
- **Claude API** for AI narration (optional; local fallback engine when unavailable)
- **~9,500 lines**, one file, no backend

## Running it

**Just open the file.** Download `index.html` and open it in any modern browser — that's the whole setup. Everything runs client-side.

For the live AI narration, the app calls a language-model API; when that isn't reachable, the built-in local analysis engine handles it automatically, so the platform is fully functional offline.

## Important notes on the data

This is a **demonstration platform**, and it says so throughout:

- **All portfolio holdings, prices, and NAVs are generated sample data** — not real market data or live accounts (shown by the persistent "DEMO DATA" badge).
- **The institutional data connectors** (Bloomberg, ANBIMA, PostgreSQL, Preqin, etc.) shown on the Settings page are **illustrative** — they show how the platform *would* wire into production data sources, but make no real connections in this demo.
- **Backtest and simulation results** use generated market paths with real-date labels and are clearly marked as simulations, not actual historical performance.

## Design principles

🎯 **Storytelling over data-dumps** — every number explains itself
🛡️ **Graceful degradation** — the AI is an enhancement, never a hard dependency
📦 **Zero-install** — one file, opens anywhere, no backend
🔍 **Point-in-time honesty** — simulations never let future data leak into past decisions

---

*Part of my [AI Platforms](../) collection.*
