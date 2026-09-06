# 👨‍💻 Himanshu — Executive Portfolio & Projects Directory

<div align="center">

[![GitHub Profile](https://img.shields.io/badge/GitHub-himanshulm9--debug-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/himanshulm9-debug)
[![Main Hub](https://img.shields.io/badge/Main%20Hub-himanshu--bio.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://himanshu-bio.vercel.app)
[![SEO Suite](https://img.shields.io/badge/SEO%20Engine-se978.vercel.app-0070F3?style=for-the-badge&logo=google&logoColor=white)](https://se978.vercel.app)
[![Crypto Suite](https://img.shields.io/badge/Crypto%20App-crypto978.vercel.app-00E599?style=for-the-badge&logo=bitcoin&logoColor=white)](https://crypto978.vercel.app)
[![Backend Engine](https://img.shields.io/badge/Backend%20API-Render.com-46E3B7?style=for-the-badge&logo=render&logoColor=black)](https://render.com)

<p align="center">
  Welcome to my central portfolio index. This repository acts as the master directory connecting all of my open-source projects, live cloud deployments, multi-zone web platforms, and technical architecture specifications.
</p>

</div>

---

## 🌟 Live Ecosystem & Deployments Map

| Project Name | Live Production Deployment | Source Code Repository | In-Depth Documentation | Focus Area |
| :--- | :--- | :--- | :--- | :--- |
| **Main Bio Hub** | [himanshu-bio.vercel.app](https://himanshu-bio.vercel.app) | [himanshulm9-debug/himanshu-bio-ui](https://github.com/himanshulm9-debug/himanshu-bio-ui) | [Bio Hub Docs](./projects/bio-hub/README.md) | Next.js 16, 3D WebGL Canvas, Bento Grid, Resume Studio |
| **INDEX MATRIX** | [se978.vercel.app](https://se978.vercel.app) | [himanshulm9-debug/se978](https://github.com/himanshulm9-debug/se978) | [SEO Suite Docs](./projects/se978/README.md) | Technical SEO Crawler, Google Login Gatekeeper, PDF NLP Extractor |
| **CryptoPro** | [crypto978.vercel.app](https://crypto978.vercel.app) | [himanshulm9-debug/crypto-visualizer](https://github.com/himanshulm9-debug/crypto-visualizer) | [Crypto Docs](./projects/crypto-visualizer/README.md) | Live Candlestick Charts, Binance/CoinGecko Feeds, Pair Search |
| **Backend API Engine** | `Render.com Web Service` | [himanshulm9-debug/himanshu-bio-server](https://github.com/himanshulm9-debug/himanshu-bio-server) | [Backend Docs](./projects/backend-server/README.md) | Fastify (~75k req/sec), Telegram Cloud Storage Tunnel, Rate Limiting |
| **YouTube & Gemini Suite** | *Decoupled Service* | [himanshulm9-debug/himanshu-dev](https://github.com/himanshulm9-debug/himanshu-dev) | [AI & Media Docs](./projects/himanshu-dev/README.md) | Persistent Audio Player & Google Gemini AI Conversational Assistant |

---

## 🏛️ Architecture Highlights

### 1. 🌐 Seamless Vercel Multi-Zone Edge Rewrites
Rather than forcing users to jump between disconnected websites, the platform uses **Vercel Edge Rewrites** to stream distinct deployments under a single unified address bar:
- `/apps/seo/*` ➔ Streamed from `https://se978.vercel.app` in `<50ms`.
- `/apps/crypto/*` ➔ Streamed from `https://crypto978.vercel.app` in `<50ms`.
- The user's URL bar stays clean on `himanshu-bio.vercel.app` with zero reload flash and shared glassmorphic dock navigation.

### 2. 🔐 Mandatory Google Login Gatekeeper (SEO Platform)
- **Strict Zero-Guest Policy**: Guests cannot run scans. Clicking the SEO platform immediately opens the Google Login modal.
- **Quota Protection**: Google authenticated users receive **20 scans / day** (tracked in Firebase Firestore), while Admin accounts retain unlimited scans.

### 3. ✈️ Telegram Cloud Storage Tunneling
- Document uploads (PDFs, resumes, text) are processed ephemerally on Render.com in RAM/`/tmp`.
- Files are asynchronously tunneled to a **Private Telegram Channel** via the Telegram Bot API (`bot.sendDocument()`) for infinite, 100% free cloud storage.
- Local temporary buffers are immediately purged (`fs.unlinkSync()`), guaranteeing **0 MB permanent server disk usage** on Render.

---

## 🌳 Repository Structure

```
About-me/
├── .gitignore
├── README.md                           # Master Portfolio & Ecosystem Index (this file)
├── docs/
│   └── UNIFIED_ARCHITECTURE.md         # 400+ line end-to-end technical system specification
└── projects/
    ├── bio-hub/
    │   └── README.md                   # himanshu-bio-ui (Next.js 16, Three.js, Multi-Zone)
    ├── se978/
    │   └── README.md                   # se978 (INDEX MATRIX SEO Engine & Google Login Gatekeeper)
    ├── crypto-visualizer/
    │   └── README.md                   # crypto-visualizer (CryptoPro Market Charts & Feeds)
    ├── backend-server/
    │   └── README.md                   # himanshu-bio-server (Fastify API & Telegram Cloud Tunnel)
    └── himanshu-dev/
        └── README.md                   # himanshu-dev (Decoupled YouTube Player & Gemini AI Chat)
```

---

## 📂 Documentation Vault

Each subfolder contains full, standalone documentation with setup instructions, API contracts, and environment variable references:

- 📄 **[`projects/bio-hub/README.md`](./projects/bio-hub/README.md)**: Main Portfolio Hub, 3D Particle Hero, and Multi-Zone Edge config.
- 📄 **[`projects/se978/README.md`](./projects/se978/README.md)**: INDEX MATRIX SEO Engine, DOM crawler, and Google Auth Gatekeeper.
- 📄 **[`projects/crypto-visualizer/README.md`](./projects/crypto-visualizer/README.md)**: CryptoPro visualizer, chart math, and WebSocket feeds.
- 📄 **[`projects/backend-server/README.md`](./projects/backend-server/README.md)**: Fastify API endpoints, Telegram storage bridge, and Firebase setup.
- 📄 **[`projects/himanshu-dev/README.md`](./projects/himanshu-dev/README.md)**: Standalone YouTube streaming player and Google Gemini AI chatbot.
- 📐 **[`docs/UNIFIED_ARCHITECTURE.md`](./docs/UNIFIED_ARCHITECTURE.md)**: Complete 400+ line technical architecture specification.

---

## 🚀 1-Command Multi-Repo Sync Tool (`push-all.sh`)

Instead of manually navigating into 5 separate folders to commit and push changes, you can manage the entire ecosystem with a single command from the root directory:

```bash
# Check git status across all 5 repositories
./push-all.sh status

# Automatically stage, commit, and push changes across all 5 repos
./push-all.sh "feat: sync updates across portfolio ecosystem"

# Create missing repos on GitHub via GitHub CLI
./push-all.sh create
```

### GitHub CLI One-Time Authentication:
If you haven't authenticated GitHub CLI (`gh`) yet:
```bash
gh auth login
# 1. Select GitHub.com -> HTTPS
# 2. Select 'Yes' to authenticate Git with GitHub credentials
# 3. Choose 'Login with a web browser' and confirm authorization
```

---

## 🛠️ Manual Publication (Individual Repository)

If you prefer to manually manage this repository alone:

```bash
cd "/home/hj/Desktop/bio ultimate/About-me"
git add .
git commit -m "feat: update documentation"
git push -u origin main
```

---

## 📬 Contact & Connect

**Himanshu**
- **GitHub**: [@himanshulm9-debug](https://github.com/himanshulm9-debug)
- **Live Portfolio**: [https://himanshu-bio.vercel.app](https://himanshu-bio.vercel.app)
- **Email**: [contact@himanshu.dev](mailto:contact@himanshu.dev)

---

<div align="center">
  <sub>Engineered with precision, TypeScript, Next.js, Fastify, and Vercel Multi-Zones. © 2026 Himanshu.</sub>
</div>
