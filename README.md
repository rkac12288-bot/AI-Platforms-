# AI Platforms — From Business Problem to Working Product

### Five platforms. Five industries. One idea: data should tell people what to *do*.

Most dashboards report numbers and stop there. Every platform in this repository goes one step further: it finds where money, time or trust is leaking, explains why in plain language, and ends in a decision someone can act on today.

Each one started as a real business problem — lost orders in a supermarket, expiring stock in a pharmacy, ungoverned AI in a large holding, unreadable risk metrics in wealth management, endless scrolling on a streaming app — and became a tool that opens in a browser, with no install.

![Platforms](https://img.shields.io/badge/platforms-5-4a8ae0) ![Industries](https://img.shields.io/badge/industries-retail%20·%20pharma%20·%20finance%20·%20media-22b8a8) ![Install](https://img.shields.io/badge/install-none-3db876) ![Data](https://img.shields.io/badge/data-demo%20%26%20anonymised-e0a84a)

---

## The platforms

### 🛒 Supermarket Ops Copilot — *every missing item has a price*
A neighbourhood supermarket sells through a delivery app. When a shelf is empty, the customer cancels the whole basket and the store never learns why. The copilot connects delivery orders to the shelf: it predicts stockouts days ahead, finds the **deal-breaker items** that cancel entire orders, shortens reorder cycles and routes pickers by aisle.

**Impact in the demo:** delivery revenue **+158%**, cancellations **9.1% → 3.4%**, picking **19% faster**.

[▶ Live demo](https://rkac12288-bot.github.io/AI-Platforms-/supermarket-ops-copilot/) · [🎞 Presentation](https://rkac12288-bot.github.io/AI-Platforms-/supermarket-ops-copilot/presentation.html) · [📂 Code](supermarket-ops-copilot/)

### 🏛 Eterna CoE Command — *fourteen GenAI experiments, one EBITDA engine*
In a large holding, every function buys its own AI tools, data leaks into public chatbots and nobody can tell the board what GenAI is worth. Eterna CoE Command runs a **hub-and-spoke** Centre of Excellence: one secure platform, governance for LGPD, BACEN and the AI Bill built in, and ROI tracked per function and division — with a view for each executive.

**Impact in the demo:** **R$14.2M** ROI (77% over target), **+68 bps** EBITDA, cost per AI interaction **60% lower**, **zero** data incidents.

[▶ Live demo](https://rkac12288-bot.github.io/AI-Platforms-/eterna-coe-command/) · [🎞 Presentation](https://rkac12288-bot.github.io/AI-Platforms-/eterna-coe-command/presentation.html) · [📂 Code](eterna-coe-command/)

### 💊 Pharmacy Operations ERP — *margin leaks out one shelf at a time*
Pharmacy margins are thin, and they leak quietly: products expire unnoticed, best sellers run out, prices drift above the recommended price, units disappear. This control room watches all four, explains each pattern with an AI engine, and turns it into action — a Quick Sale sticker, a reorder, an owner for every issue.

**Impact in the demo:** **$200.7K** recoverable from expiring stock, **$418K** of losses traced, **0** price violations across 700 products.

[▶ Live demo](https://rkac12288-bot.github.io/AI-Platforms-/pharmacy-operations-erp/) · [🎞 Presentation](https://rkac12288-bot.github.io/AI-Platforms-/pharmacy-operations-erp/presentation.html) · [📂 Code](pharmacy-operations-erp/)

### 📈 Eterna Wealth — *the portfolio that explains itself*
Sharpe, VaR, drawdown — and the only question that matters: *so what do I do?* Click any number and Eterna tells its story: what it means, why it matters, which holdings drive it, and the **one move to make**. The same portfolio reframes itself for the CEO, the CFO and the portfolio manager, and the AI analyst keeps working even offline.

[▶ Live demo](https://rkac12288-bot.github.io/AI-Platforms-/eterna-wealth/) · [📂 Code](eterna-wealth/)

### 🎬 AI Movie Recommender — *a recommendation with a reason*
A Python engine on the real 1,000-movie IMDB catalog. Five recommendation methods — content-based, cosine similarity, collaborative filtering, k-means taste groups and a trending fallback — built with statistical care, and closed by a five-chapter story dashboard that argues for the pick.

[🎞 Presentation](https://rkac12288-bot.github.io/AI-Platforms-/movie-recommendation-system/presentation.html) · [📂 Code](movie-recommendation-system/) · run with `python main.py`

---

## At a glance

| Platform | Industry | The problem it solves | Built with |
|---|---|---|---|
| [Supermarket Ops Copilot](supermarket-ops-copilot/) | Retail · delivery | Lost orders, stockouts, slow picking | HTML · JavaScript · Chart.js |
| [Eterna CoE Command](eterna-coe-command/) | Corporate · GenAI governance | Ungoverned AI, no measurable value | HTML · JavaScript · Chart.js |
| [Pharmacy Operations ERP](pharmacy-operations-erp/) | Retail pharmacy | Expiry, stockouts, pricing, shrinkage | HTML · JavaScript |
| [Eterna Wealth](eterna-wealth/) | Wealth management | Metrics nobody can act on | HTML · JavaScript · Chart.js · Claude API |
| [AI Movie Recommender](movie-recommendation-system/) | Media · entertainment | Recommendations nobody trusts | Python · pandas · SciPy · Matplotlib |

---

## How I build

🎯 **Start from the money, not the model.** Every platform begins with the cost of the problem — lost baskets, expired stock, basis points of EBITDA — and is judged by what it changes.

📖 **Storytelling over data dumps.** Numbers come with a narrative: what happened, why, and the next step. Each platform has a presentation that tells that story in 9 slides.

⚡ **Zero friction.** Single-file web apps with no install, no backend and no build step. Open the link and it works — on a laptop, a tablet or a picker's phone.

🛡 **Honest by design.** Demo data is labelled as demo data, illustrative connectors as illustrative, and statistical shortcuts are avoided on purpose.

🤖 **AI as a partner.** Built with Claude as a pair-architect, from framing the business problem to shipping the product.

---

## Run anything locally

- **Web platforms:** download the folder and open `index.html` in any modern browser. Open `presentation.html` for the story, and use the arrow keys to move between slides.
- **Movie recommender:** `pip install -r requirements.txt`, then `python main.py`.

```
AI-Platforms/
├── supermarket-ops-copilot/       index.html · presentation.html · README.md
├── eterna-coe-command/            index.html · presentation.html · README.md
├── pharmacy-operations-erp/       index.html · presentation.html · README.md
├── eterna-wealth/                 index.html · README.md
└── movie-recommendation-system/   Python code · IMDB dataset · presentation.html · README.md
```

---

## A note on data

All company names, people and figures in this repository are **fictional or anonymised**, and no client data is included. The platforms were inspired by real business situations and rebuilt with demo data so they can be shared openly.

---

## About me

I'm **Renata**, an AI Solutions Architect and Business Designer. I started as a geologist and exploration manager — a field where you make expensive decisions from incomplete data — and now design AI platforms that help retail, finance and corporate teams do the same with more confidence.

**In progress:** *Lumina*, the architecture for a therapeutic AI companion with an embodied robot.

📫 [LinkedIn](#) · [Email](#)
