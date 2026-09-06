# 🪙 crypto-visualizer (CryptoPro) — Real-Time Cryptocurrency Visualizer & Market Analytics

<div align="center">

[![GitHub repo](https://img.shields.io/badge/GitHub-himanshulm9--debug%2Fcrypto--visualizer-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/himanshulm9-debug/crypto-visualizer)
[![Direct Deployment](https://img.shields.io/badge/Direct%20Live-crypto978.vercel.app-00E599?style=for-the-badge&logo=vercel&logoColor=white)](https://crypto978.vercel.app)
[![Multi--Zone Stream](https://img.shields.io/badge/Multi--Zone-himanshu--bio.vercel.app%2Fapps%2Fcrypto-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://himanshu-bio.vercel.app/apps/crypto)
[![React](https://img.shields.io/badge/React-19-blue?style=flat-square&logo=react)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-6-646CFF?style=flat-square&logo=vite)](https://vitejs.dev/)

<p align="center">
  Real-time cryptocurrency price tracker, historical interactive charts, market capitalization tables, and live financial market analytics.
</p>

</div>

---

## 🌟 Overview

**CryptoPro (`crypto-visualizer`)** is a crypto visualizer and market analytics web application built with React 19 and Vite. It provides real-time pricing feeds, responsive candlestick and line charts across multiple timeframes, market cap rankings, top gainers/losers, and deep coin metric analytics.

It runs standalone on Vercel at **[crypto978.vercel.app](https://crypto978.vercel.app)** and seamlessly streams inside the main portfolio ecosystem under **[himanshu-bio.vercel.app/apps/crypto](https://himanshu-bio.vercel.app/apps/crypto)** via Vercel Edge Rewrites.

---

## ✨ Features & Architecture

- 📈 **Multi-Asset Candlestick & Area Charts (`CandleChart.tsx`)**: High-performance HTML5 canvas-rendered candlestick and smooth bezier line charts with customizable timeframes (24h, 7d, 30d, 1y), volume histogram bars, asset exchange tags, and crosshair inspection tooltips.
- 🪙 **Live Crypto Market Overview (`MarketStats.tsx`) & Top 100 Screener (`MarketTable.tsx`)**: Real-time snapshot of the global crypto market, BTC & ETH dominance, 24-hour trading volume, and filtering across 100+ cryptocurrencies with 7-day sparklines.
- 🏢 **Global Stocks Tab & Top 200 Screener (`StockTable.tsx`)**: Enterprise-grade equities screener covering 200 top-performing stocks across all major sectors (Technology & AI, Semiconductors, Financials, Healthcare, Consumer, Energy, CleanTech) with search, sector pills, quick presets (Top Gainers, Top Losers, High Volume, Mega Cap $200B+, High Dividend, Low P/E), and multi-column sorting.
- ⚡ **Live Tape & Last Executed Trades (`StockLastTrades.tsx`)**: Real-time simulated NYSE & NASDAQ trade print stream with execution timestamps, buy/sell/block order tags, share sizes, and notional dollar values.
- 📊 **Deep Fundamentals & Coin Inspection Drawers (`StockDrawer.tsx` & `CoinDrawer.tsx`)**: Slide-out modal drawers displaying 52-week high/low progress gauges, trailing and forward P/E, EPS, Beta, dividend yields, Wall Street 12-month target prices with upside %, and direct research links.
- 💱 **Multi-Currency Converter (`CurrencySelector.tsx`)**: Dynamic conversion between major fiat currencies (USD, EUR, INR, GBP, JPY) applied seamlessly across both Crypto and Stocks with live exchange multipliers.
- 🎨 **Glassmorphic Cyber-Dark Interface**: Designed with Tailwind CSS, custom dark mode aesthetics, smooth dock navigation, and zero layout shift.

---

## 🌐 Vercel Multi-Zone Routing

CryptoPro is deployed as an autonomous Vercel project (`crypto978.vercel.app`). When accessed through the main portfolio:

```
User visits: himanshu-bio.vercel.app/apps/crypto
                     │
            [Vercel Edge Rewrite]
                     │
                     ▼
Fetches & Streams from: crypto978.vercel.app
(Zero URL redirection, zero reload flash, shared Mac-style dock navigation)
```

Configuration in `apps/crypto978/vercel.json`:
```json
{
  "rewrites": [
    { "source": "/(.*)", "destination": "/index.html" }
  ],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        { "key": "Access-Control-Allow-Origin", "value": "*" },
        { "key": "X-Frame-Options", "value": "SAMEORIGIN" }
      ]
    }
  ]
}
```

---

## 🚀 Local Development Setup

```bash
# Clone the repository
git clone https://github.com/himanshulm9-debug/crypto-visualizer.git
cd crypto-visualizer

# Install dependencies
npm install

# Start Vite local development server
npm run dev

# Build for production
npm run build
```
Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## 🛠️ Tech Stack

- **Language & Framework**: TypeScript 5.7, React 19
- **Bundler & Tooling**: Vite 6, Rollup
- **Styling**: Tailwind CSS with Cyber-Glass Design Tokens
- **Market Data APIs**: CoinGecko & Binance Public REST APIs
- **Deployment**: Vercel Serverless Edge

---

## 👤 Author & Maintainer
**Himanshu** - [@himanshulm9-debug](https://github.com/himanshulm9-debug)
