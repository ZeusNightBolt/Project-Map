# Project-Map

Index of active projects, grouped by domain. This repo publishes a landing page (`index.html`),
titled **ZeusBot Project Directory**, via GitHub Pages at
**https://zeusnightbolt.github.io/Project-Map/** — a dark, neon-themed interface with four
tabbed sections: **Trader Command Zone**, **Agentic Workflows**, **Casino**, and
**Passion Projects**. The tables below are the underlying source of truth.

**Featured:** [Grand Atlantic](https://zeusnightbolt.github.io/GrandAtlanticLive/) gets a glowing,
animated hero banner (rotating gradient border, scanline sweep, "bankroll" flow animation) at the
top of the **Casino** tab, above the grid of individual trainers — it isn't repeated as a regular
card in that grid.

Link convention: each card opens the project's live **GitHub Pages** deployment on click. Source
repositories are **private**, so repository links have been removed from every card — there's
nothing public to send visitors to. Where a project has no public deployment at all (source-only,
no Pages site), the card is informational only and isn't clickable; its footer says so explicitly
(see CRE AI Agent below).

## Card preview art

Every card shows a stylized preview image at the top — a generated "browser window" mockup
(traffic-light dots, a URL pill, and a large icon on a gradient backdrop in that project's category
color) rather than a real screenshot. The environment this page was built in can't reach
`*.github.io` to capture actual screenshots of the live sites (an org-level network policy, not a
per-tool setting), so these are deliberately abstract stand-ins meant to make each card more
visually inviting to click through, not a literal representation of each site's UI. The rendered
PNGs live in `assets/previews/` (one file per project); the HTML template used to generate them
was not committed — recreate a similar template if a preview needs regenerating, or swap in a real
screenshot per project once one is available.

## Favicon & link-preview assets

`assets/` holds the real, hosted icon and social-preview files (`favicon.svg`, `favicon-32.png`,
`favicon-64.png`, `apple-touch-icon.png`, `icon-512.png`, `og-image.png`). These are committed as
actual files rather than inline data URIs — many link-preview crawlers (iMessage, Slack, X, etc.)
and iOS's apple-touch-icon require a real, fetchable image URL and won't reliably resolve a
`data:` URI, which is why an earlier version of this page showed a stale/wrong icon when shared.
`index.html`'s `og:image`/`twitter:image` point at `assets/og-image.png`, a rendered 1200×630 card,
so that's what should appear as the link preview everywhere.

## 📡 Trader Command Zone

| Project | Icon | Live site | Tech | Description |
|---|---|---|---|---|
| **BoltNews** | ⚡ | [zeusnightbolt.github.io/BoltNews](https://zeusnightbolt.github.io/BoltNews/) | Python 3.12, multi-agent LLM pipeline, cron, static HTML dashboard, GitHub Pages | Daily automated cross-asset news-intelligence pipeline for a fundamental long/short PM. Synthesizes pre-market, post-market, and weekend research briefings across equities, rates, credit, FX, commodities, volatility, and crypto using multi-agent discovery lanes. |
| **BetNews** | 🏈 | [zeusnightbolt.github.io/BetNews](https://zeusnightbolt.github.io/BetNews/) | Python 3.11+ (stdlib only), Polymarket Gamma API, RSS feeds, vanilla JS search, GitHub Actions → Pages | Daily automated betting-intelligence briefing: consensus odds, positive-EV screens, and underdog trend analysis aggregated across Polymarket, Kalshi, DraftKings, FanDuel, and 60+ other sportsbooks and analytics sources. |
| **Equity Screener** | 📈 | [zeusnightbolt.github.io/equity-screener](https://zeusnightbolt.github.io/equity-screener/) | Python, DuckDB/Polygon warehouse, pandas, GitHub Pages | Daily dashboard ranking low-priced, $5B+ market-cap VTI stocks across seven deterministic scoring sleeves (RSI inflection, value, momentum, squeeze) plus a wave-stage classifier and an adaptive, factor-momentum-tilted EV master score. |
| **AI Assisted Earnings Screener** | 🧠 | [zeusnightbolt.github.io/AI-Assisted-Earnings-Screener](https://zeusnightbolt.github.io/AI-Assisted-Earnings-Screener/) | Python, SEC EDGAR, DoltHub, DuckDB, DeepSeek LLM, GitHub Actions → Pages | Screens for the best technical/fundamental setups heading into earnings by cross-referencing VTI holdings against a SEC EDGAR/DoltHub earnings calendar, reusing the equity screener's 7-sleeve scoring engine and adding LLM commentary. |
| **BoltFactors** | 🧮 | [zeusnightbolt.github.io/BoltFactors](https://zeusnightbolt.github.io/BoltFactors/) | Python, DuckDB/Polygon warehouse, cron (5x daily), static HTML dashboard | AI-powered factor briefing — five-times-daily quantitative factor summaries generated from the VTI market-data warehouse, tracking regime shifts across value, momentum, quality, and volatility factors. |

## 🤖 Agentic Workflows

| Project | Icon | Live site | Tech | Description |
|---|---|---|---|---|
| **CRE AI Agent** | 🏢 | — *(private, no public deployment)* | Python, Selenium/Firefox CDP scraping, Streamlit, static HTML dashboard | Automated commercial real estate pipeline: scrapes LoopNet listings past Akamai bot protection via Firefox remote-debugging, then serves the deal set through an interactive underwriting dashboard for per-deal deep dives. |
| **YouTube Briefings** | ▶️ | [zeusnightbolt.github.io/yt-briefing](https://zeusnightbolt.github.io/yt-briefing/) | Python, static HTML dashboard, GitHub Actions → Pages | Intelligence generator for a tracked list of YouTube creators — turns their channel and video activity into a structured, digestible briefing. |

## 🎰 Casino

Featured above the table below: **Grand Atlantic** (🏛️) — [zeusnightbolt.github.io/GrandAtlanticLive](https://zeusnightbolt.github.io/GrandAtlanticLive/) · React, Vite, Vanilla JS, client-side only. Flagship five-table casino floor aggregating Blackjack, Roulette, Baccarat, Craps, and Poker trainers behind one animated front end, sharing a single bankroll and profit goal across all five games.

| Project | Icon | Live site | Tech | Description |
|---|---|---|---|---|
| **Blackjack Trainer** | 🃏 | [zeusnightbolt.github.io/BlackjackTrainer](https://zeusnightbolt.github.io/BlackjackTrainer/) | React 18, Vite 5, Tailwind CSS 3, GitHub Actions → Pages | Interactive basic-strategy and Hi-Lo card-counting trainer set at an Atlantic City high-limit table, with move-by-move coaching, count-aware bet sizing, behavioral guardrails, and full-shoe simulation. |
| **Poker Trainer** | ♠️ | [zeusnightbolt.github.io/PokerTrainer](https://zeusnightbolt.github.io/PokerTrainer/) | Vanilla JS/HTML/CSS (no build step), GitHub Actions → Pages | Browser-based No-Limit Texas Hold'em trainer — play against randomized bots with a live Chen-formula/pot-odds strategy coach, a Monte Carlo equity/variance tracker, and interactive range-chart and quiz tools. |
| **Roulette Trainer** | 🎡 | [zeusnightbolt.github.io/RouletteTrainer](https://zeusnightbolt.github.io/RouletteTrainer/) | React, Vite, crypto-secure RNG, CI-verified Monte Carlo, GitHub Actions → Pages | Dark-theme double- and single-zero roulette simulator built to test whether wheel-quadrant "droughts" carry tradeable information — live telemetry, χ² stats, bankroll analytics, and a Fallacy Lab running 100k simulated spins. |
| **Craps Trainer** | 🎲 | [zeusnightbolt.github.io/CrapsTrainer](https://zeusnightbolt.github.io/CrapsTrainer/) | React, Vite, Monte Carlo-verified engine, GitHub Actions → Pages | Mathematically verified craps trainer and simulator covering every bet on the table, with a live coach recommending the edge-minimizing next move and a Monte Carlo strategy simulator. |
| **Baccarat Trainer** | 🐉 | [zeusnightbolt.github.io/BaccaratTrainer](https://zeusnightbolt.github.io/BaccaratTrainer/) | Vanilla JS (ES modules, no framework/bundler), ESLint, Node test runner, Playwright, GitHub Actions → Pages | Commission-free EZ Baccarat trainer with the Dragon Bonus and Sun 7 / Moon 8 side bets, a full electronic road board, and live coaching — Coach Me, Play, and Drill modes, plus a "Genie" companion for intuition-based calls. |

## 🎨 Passion Projects

Off-thesis builds — things made for the fun of it, not because a PM asked for them.

| Project | Icon | Live site | Tech | Description |
|---|---|---|---|---|
| **VibeNYC** | 🗽 | [zeusnightbolt.github.io/VibeNYC](https://zeusnightbolt.github.io/VibeNYC/) | Python, static HTML dashboard, GitHub Actions → Pages | Attribution-first, continuously refreshed New York City intelligence — a living feed of what's happening across the city, with every claim traceable back to its source. |
