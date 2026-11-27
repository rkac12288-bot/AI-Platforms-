# Pharmacy Operations ERP

An analytics and control platform for a pharmacy chain, built to **protect margin and grow sales**: keep prices compliant, never run out of what sells, clear expiring stock before it becomes a write-off, and make theft and breakage losses visible.

> Demo data only: 700 SKUs across 6 categories for a fictional pharmacy distribution chain.

## The problem it solves

Pharmacies lose money quietly — products expiring on the shelf, best sellers out of stock, prices drifting above the regulated or recommended price, and shrinkage nobody traces. This platform turns the inventory file into daily actions with the money at stake attached.

## Modules

| Module | What it does |
|---|---|
| **Overview** | SKUs, units, inventory value, losses, low stock and clearance at a glance, by stock status and category |
| **Pricing Compliance** | Flags any price above the recommended retail price (MSRP) |
| **Low Stock Engine** | Items below their reorder threshold, ranked by sales impact |
| **Audit & Loss Ledger** | Theft and breakage losses traced by product and category |
| **Markdown Trigger** | Products expiring within 30 days with a suggested clearance price |
| **AI Engine** | Written analysis of theft loss, markdown and low-stock patterns |
| **Action Matrix** | Every open issue turned into an owner, priority and next step |
| **Knowledge Base** | Rules and definitions behind each calculation |
| **Settings & Triggers** | Thresholds for stock, expiry and price alerts |

Every list exports to CSV (watchlist, pricing compliance, critical stock, clearance, audit report, action matrix).

## Tech

- Single self-contained HTML file, vanilla JavaScript
- No backend: the dataset is embedded and all logic runs in the browser

## Presentation

`presentation.html` tells the story of the platform in 9 slides: the problem, the hidden cost, how the platform works, the key insight and the results. Use the arrow keys to move between slides.

## Run it

Open `index.html` in any modern browser.
