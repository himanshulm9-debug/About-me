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

- 📈 **Interactive Price History Charts (`HistoryChart.jsx`)**: High-performance canvas-rendered charts with customizable timeframes (24h, 7d, 30d, 1y) and cursor inspection tooltips.
- 🪙 **Live Market Overview (`Dashboard.jsx`)**: Instant snapshot of the global crypto market, including 24-hour total trading volume, Bitcoin dominance, and trending tokens.
- 🔍 **Real-Time Market Table & Search (`Market.jsx`)**: Real-time filtering and sorting across top 100+ cryptocurrencies with 24-hour price change percentage badges and liquidity metrics.
- 📊 **Deep Coin Inspection (`CoinPage.jsx`)**: Detailed coin profiles displaying circulating supply, all-time high (ATH), all-time low (ATL), market rank, and official contract addresses.
- 💱 **Multi-Currency Converter**: Dynamic conversion between major fiat currencies (USD, EUR, INR, GBP) and crypto pairs.
- 🎨 **Glassmorphic Cyber-Dark Interface**: Designed with dark theme aesthetics, custom CSS transitions, and zero layout shift.

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
```
Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## 🛠️ Tech Stack

- **Framework**: React 19
- **Bundler & Tooling**: Vite 6, Rollup
- **Styling**: Vanilla CSS3 with Cyber-Glass Design Tokens
- **Market Data APIs**: CoinGecko & Binance Public REST APIs
- **Deployment**: Vercel Serverless Edge

---

## 👤 Author & Maintainer
**Himanshu** - [@himanshulm9-debug](https://github.com/himanshulm9-debug)
