# Core Macro Risk Monitor

**Agentic Insight Capital** — Multi-dimensional real-time macro risk surveillance dashboard.

## Overview

A single-page institutional-grade dashboard monitoring 14 macro indicators across 7 risk categories, with compound signal detection for systemic risk conditions. Built to match the Agentic Insight Capital design system.

### Indicators Tracked

| Category | Indicators |
|---|---|
| Credit Risk | HY Spread (BAMLH0A0HYM2), IG CDS, US 5Y Sovereign CDS |
| Rates / Liquidity | US 10Y Yield (DGS10), Yield Curve 2Y–10Y (T10Y2Y), Real Yield TIPS (DFII10) |
| Volatility / Stress | MOVE Index, VIX, OVX |
| Commodities / Inflation | Oil (Brent), Gold, Copper/Gold Ratio |
| Currency / Capital Flows | DXY (Dollar Index) |
| Banking / System Stress | KRE (Regional Banks) |
| Optional | TED Spread, FRA-OIS, Baltic Dry Index, Tanker Rates |

### Master Risk Conditions (compound signals)

- 🔴 **Inflation Shock Mode** — Oil >110 + 10Y yield rising + DXY rising
- 🔴 **Stress Building** — HY spreads >500 + MOVE >140 + VIX >30
- 🔴🔴 **System Break (Crisis)** — HY >600 + MOVE >160 + KRE dropping >10% + curve steepening
- 🟢 **Gold Breakout** — Real yields <1.5 + DXY falling + credit stress rising
- 🔵 **Deflation Shift** — Oil <95 + yields falling + credit widening

## Quick Start

1. Clone this repository
2. Open `index.html` in any browser — it runs with demo data immediately
3. Click **⚙ SETTINGS** to enter your API keys for live data

No build tools, no npm install, no server required. It's a single HTML file.

## API Keys (free)

### FRED API (St. Louis Federal Reserve)

1. Go to [https://fred.stlouisfed.org/docs/api/api_key.html](https://fred.stlouisfed.org/docs/api/api_key.html)
2. Create a free account and request an API key
3. Paste the key in Settings → FRED API KEY

Provides: HY Spread, 10Y Yield, Yield Curve, Real Yield (TIPS)

### Finnhub API

1. Go to [https://finnhub.io/register](https://finnhub.io/register)
2. Create a free account — the key is shown on your dashboard
3. Paste the key in Settings → FINNHUB API KEY

Provides: VIX, Oil (Brent), Gold, DXY, KRE

API keys are stored in your browser's localStorage and never transmitted anywhere except to the respective API endpoints.

## Deploy to GitHub Pages

1. Create a new GitHub repository
2. Push `index.html` and `README.md` to the `main` branch
3. Go to **Settings → Pages**
4. Set source to **Deploy from a branch**, select `main`, root `/`
5. Your dashboard will be live at `https://yourusername.github.io/reponame/`

## Features

- **Minimal Mode** — Toggle to show only: HY Spread, 10Y Yield, MOVE, Oil, VIX, KRE
- **Auto-Refresh** — Polls APIs every 60 seconds when enabled
- **30-Day Sparklines** — Visual trend for each indicator
- **Threshold Alerts** — Color-coded status badges (Normal → Elevated → High Risk → Crisis)
- **Settings Persistence** — API keys saved in localStorage across sessions
- **Responsive** — Works on desktop, tablet, and mobile
- **Zero Dependencies** — React 18 + Babel loaded from CDN, no build step

## Design System

Matches the Agentic Insight Capital brand:

- **Fonts**: Cormorant Garamond (display) + Outfit (body)
- **Colors**: Navy (#0a1628) / Gold (#b8973a) / Slate (#8899b0) / White (#f0f2f5)
- **Style**: Dark luxury finance — sharp corners, gold accents, minimal decoration

## License

© 2026 Agentic Insight Capital. All rights reserved.
