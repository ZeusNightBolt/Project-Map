# Project-Map

Index of active projects, grouped by domain. This repo publishes a landing page (`index.html`)
via GitHub Pages at **https://zeusnightbolt.github.io/Project-Map/** — the table below is the
underlying source of truth.

Link convention: a project links to its live **GitHub Pages** deployment when one exists;
otherwise it links straight to the **repository**. Where a Pages site exists, the repository is
also listed separately.

## Market Related

| Project | Live site | Repository | Tech | Description |
|---|---|---|---|---|
| **BoltNews** | [zeusnightbolt.github.io/BoltNews](https://zeusnightbolt.github.io/BoltNews/) | [repo](https://github.com/ZeusNightBolt/BoltNews) | Python 3.12, multi-agent LLM pipeline, cron, static HTML dashboard, GitHub Pages | Daily automated cross-asset news-intelligence pipeline for a fundamental long/short PM. Synthesizes pre-market, post-market, and weekend research briefings across equities, rates, credit, FX, commodities, volatility, and crypto using multi-agent discovery lanes. |
| **Equity Screener** | [zeusnightbolt.github.io/equity-screener](https://zeusnightbolt.github.io/equity-screener/) | [repo](https://github.com/ZeusNightBolt/equity-screener) | Python, DuckDB/Polygon warehouse, pandas, GitHub Pages | Daily dashboard ranking low-priced, $5B+ market-cap VTI stocks across seven deterministic scoring sleeves (RSI inflection, value, momentum, squeeze) plus a wave-stage classifier and an adaptive, factor-momentum-tilted EV master score. |
| **AI Assisted Earnings Screener** | [zeusnightbolt.github.io/AI-Assisted-Earnings-Screener](https://zeusnightbolt.github.io/AI-Assisted-Earnings-Screener/) | [repo](https://github.com/ZeusNightBolt/AI-Assisted-Earnings-Screener) | Python, SEC EDGAR, DoltHub, DuckDB, DeepSeek LLM, GitHub Actions → Pages | Screens for the best technical/fundamental setups heading into earnings by cross-referencing VTI holdings against a SEC EDGAR/DoltHub earnings calendar, reusing the equity screener's 7-sleeve scoring engine and adding LLM commentary. |

## Agentic / Workflow

| Project | Live site | Repository | Tech | Description |
|---|---|---|---|---|
| **CRE AI Agent** | — *(no Pages deployment)* | [repo](https://github.com/ZeusNightBolt/CRE-AI-Agent) | Python, Selenium/Firefox CDP scraping, Streamlit, static HTML dashboard | Automated commercial real estate pipeline: scrapes LoopNet listings past Akamai bot protection via Firefox remote-debugging, then serves the deal set through an interactive underwriting dashboard for per-deal deep dives. |

## Gambling / Casino

| Project | Live site | Repository | Tech | Description |
|---|---|---|---|---|
| **Blackjack Trainer** | [zeusnightbolt.github.io/BlackjackTrainer](https://zeusnightbolt.github.io/BlackjackTrainer/) | [repo](https://github.com/ZeusNightBolt/BlackjackTrainer) | React 18, Vite 5, Tailwind CSS 3, GitHub Actions → Pages | Interactive basic-strategy and Hi-Lo card-counting trainer set at an Atlantic City high-limit table, with move-by-move coaching, count-aware bet sizing, behavioral guardrails, and full-shoe simulation. |
| **Poker Trainer** | [zeusnightbolt.github.io/PokerTrainer](https://zeusnightbolt.github.io/PokerTrainer/) | [repo](https://github.com/ZeusNightBolt/PokerTrainer) | Vanilla JS/HTML/CSS (no build step), GitHub Actions → Pages | Browser-based No-Limit Texas Hold'em trainer — play against randomized bots with a live Chen-formula/pot-odds strategy coach, a Monte Carlo equity/variance tracker, and interactive range-chart and quiz tools. |
| **Roulette Trainer** | [zeusnightbolt.github.io/RouletteTrainer](https://zeusnightbolt.github.io/RouletteTrainer/) | [repo](https://github.com/ZeusNightBolt/RouletteTrainer) | React, Vite, crypto-secure RNG, CI-verified Monte Carlo, GitHub Actions → Pages | Dark-theme double- and single-zero roulette simulator built to test whether wheel-quadrant "droughts" carry tradeable information — live telemetry, χ² stats, bankroll analytics, and a Fallacy Lab running 100k simulated spins. |
| **Craps Trainer** | [zeusnightbolt.github.io/CrapsTrainer](https://zeusnightbolt.github.io/CrapsTrainer/) | [repo](https://github.com/ZeusNightBolt/CrapsTrainer) | React, Vite, Monte Carlo-verified engine, GitHub Actions → Pages | Mathematically verified craps trainer and simulator covering every bet on the table, with a live coach recommending the edge-minimizing next move and a Monte Carlo strategy simulator. |
| **BetNews** | [zeusnightbolt.github.io/BetNews](https://zeusnightbolt.github.io/BetNews/) | [repo](https://github.com/ZeusNightBolt/BetNews) | Python 3.11+ (stdlib only), Polymarket Gamma API, RSS feeds, vanilla JS search, GitHub Actions → Pages | Daily automated betting-intelligence briefing: consensus odds, positive-EV screens, and underdog trend analysis aggregated across Polymarket, Kalshi, DraftKings, FanDuel, and 60+ other sportsbooks and analytics sources. |
