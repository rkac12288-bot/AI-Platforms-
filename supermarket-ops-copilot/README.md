# Supermarket Ops Copilot

An operations console for a neighbourhood supermarket that sells through a delivery marketplace (Wolt). It turns the store's order history into daily decisions that **grow online sales and cut losses** from stockouts, item replacements, cancellations and slow picking.

> Demo data only. "Cedar Market" is a fictional store; the catalogue, orders, stock and store layout are generated example data.

## The problem it solves

When a customer orders online and an item is missing, the store either replaces it, removes it, or the whole order is cancelled. Each of those costs revenue, ratings and repeat customers. Most small stores only see this as a long list of rejected items in the delivery app, with no link to stock, reorders or the shelf layout.

## Modules

| Module | What it does |
|---|---|
| **Executive briefing** | Six-chapter story for the owner: where revenue comes from, what is growing or fading, when customers order, basket economics, service quality, and decisions for the next 30 days |
| **Compare periods** | Week-on-week and month-on-month comparison with a written explanation of what drove the change |
| **Command center** | 30-day revenue, orders, basket, cancellations, short lines and pick time against the store's monthly targets |
| **Sales dashboard** | Weekly revenue and order trends, hour-by-day demand heatmap |
| **Manager alerts** | Prioritised alerts with the money at stake and a concrete action for the owner or operations team |
| **Stock & losses** | Days of cover per item and stockout risk before the next delivery |
| **Deal-breakers** | Items whose absence causes whole-order cancellations |
| **Replacements & reorder** | Frequently replaced items with a restock / delist / watch decision and a reorder quantity |
| **Planogram picking** | Store map with an optimised picking route and a phone-friendly pick list |
| **Owner & ops reports** | Ready-to-send daily summaries |
| **Growth simulator** | What-if sliders for basket size, availability and order volume against revenue targets |
| **Import data** | Drop in the delivery platform's order export or a stock CSV to replace the demo data |

## Tech

- Single self-contained HTML file, vanilla JavaScript
- Chart.js from CDN, IBM Plex fonts
- Bilingual product names (Hebrew / English), right-to-left text handled per field
- Light and dark themes, responsive down to phone width
- No backend: all calculations run in the browser

## Presentation

`presentation.html` tells the story of the platform in 9 slides: the problem, the hidden cost, how the platform works, the key insight and the results. Use the arrow keys to move between slides.

## Run it

Open `index.html` in any modern browser, or use the GitHub Pages link in the main README.

## Origin

Built with Claude for a real store, then anonymised for this portfolio. In production, Claude was connected to the store's delivery-platform order system to analyse rejected and replaced items and guide the owner and operations on stock, reorders and picking.
