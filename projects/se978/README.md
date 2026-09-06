# ⚡ se978 — INDEX MATRIX Technical SEO Engine & DOM Crawler

<div align="center">

[![GitHub repo](https://img.shields.io/badge/GitHub-himanshulm9--debug%2Fse978-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/himanshulm9-debug/se978)
[![Direct Deployment](https://img.shields.io/badge/Direct%20Live-se978.vercel.app-0070F3?style=for-the-badge&logo=vercel&logoColor=white)](https://se978.vercel.app)
[![Multi--Zone Stream](https://img.shields.io/badge/Multi--Zone-himanshu--bio.vercel.app%2Fapps%2Fseo-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://himanshu-bio.vercel.app/apps/seo)
[![Google OAuth](https://img.shields.io/badge/Auth-Google%20Login%20Gatekeeper-EA4335?style=flat-square&logo=google)](https://firebase.google.com/)
[![NLP Engine](https://img.shields.io/badge/NLP-pdf--parse%20v2-green?style=flat-square)](https://www.npmjs.com/package/pdf-parse)

<p align="center">
  Enterprise on-page SEO diagnostics, live DOM crawler, binary document NLP keyword extractor, competitor gap analyzer, and Googlebot indexing automation.
</p>

</div>

---

## 🌟 Overview

**INDEX MATRIX (`se978`)** is a technical SEO automation suite designed to inspect, audit, and accelerate search engine visibility. Built with a responsive cyberpunk glassmorphism interface, it features deep DOM hierarchy inspection, binary document keyword extraction, and automated Google Indexing API submission.

It is accessible both directly via **[se978.vercel.app](https://se978.vercel.app)** and via the main portfolio multi-zone rewrite at **[himanshu-bio.vercel.app/apps/seo](https://himanshu-bio.vercel.app/apps/seo)**.

---

## 🔐 Strict Google Login Gatekeeper & Abuse Protection

To safeguard backend crawler compute and third-party APIs against scrapers and unauthenticated bot abuse, **INDEX MATRIX enforces a zero-guest policy**:

```
Visitor clicks /apps/seo
         │
         ▼
[Google Auth Gatekeeper] ──── No active Google Session?
         │                               │
         ▼ (Authenticated)               ▼ (Unauthenticated)
[Check Daily Quotas]             [Display Google Login Modal]
  ├── Google User: 20 scans/day       (Zero guest scans permitted)
  └── Admin: Unlimited scans
```

- **Zero Free Guest Scans**: Unauthenticated visitors cannot initiate scans or audits. Clicking any audit action immediately triggers the Google OAuth popup modal (`js/google-auth-gatekeeper.js`).
- **Quota Allocation**:
  - **Standard Google Users**: 20 deep technical scans per calendar day (UTC reset), tracked and synced via Firebase Firestore and Upstash Redis.
  - **Verified Admin**: Unlimited audits, access to raw GSC bot dispatch logs, and project history purge capabilities.
- **Cooldown Timers**: Built-in 20-second cooldown protection on indexing triggers prevents rapid re-submissions.

---

## 🛠️ Core Diagnostic Modules

### 1. Live Web Crawler & DOM Security Inspector (`CrawlerTab.tsx`)
- Parses complete HTML DOM structure, HTTP response headers, OpenGraph / Twitter Cards, canonical tags, and robots directives.
- Real-time accessibility, contrast, and mobile viewport responsive checks.
- Dynamic animated SVG radial health gauges with color-graded feedback.

### 2. Binary PDF & Document NLP Keyword Extractor (`NlpUploadTab.tsx`)
- Drag-and-drop document NLP keyword extraction engine supporting `.pdf`, `.docx`, `.txt`, and `.csv`.
- Extracts 1-, 2-, and 3-word n-gram keyphrases, keyword density percentages, and search intent classification.
- Document uploads are processed ephemerally and tunneled to Telegram Cloud Storage, consuming **0 MB permanent disk**.

### 3. Competitor Keyword Gap & Overlap Engine (`CompetitorGapTab.tsx`)
- Side-by-side crawl comparison of your domain against competitor URLs.
- Identifies common ranking keywords, missed keyword opportunities, and content gaps.

### 4. Real-Time Broken Link & Redirect Inspector (`BrokenLinksTab.tsx`)
- Concurrently probes internal and external hyperlinks for `200 OK`, `301/302` redirects, and `404/500` dead links.
- Exportable CSV audit reports with response latency profiling.

### 5. Search Engine Bot Dispatcher (`BotIndexerTab.tsx`)
- Automated batch submission of URLs and XML sitemaps to Google Indexing API and IndexNow.
- Validates Google Cloud Service Account JSON keys before publishing with a 20-second anti-abuse cooldown.

---

## 🚀 Local Development Setup

```bash
# Clone the repository
git clone https://github.com/himanshulm9-debug/se978.git
cd se978

# Install dependencies
npm install

# Run local development server
npm run dev

# Build for production
npm run build
```
The Vite development server will launch at `http://localhost:5174`.

---

## 🛠️ Tech Stack

- **Language & Framework**: TypeScript 5.7, React 19
- **Bundler & Tooling**: Vite 6, Rollup
- **Styling**: Tailwind CSS with Cyber-Glass Design Tokens
- **Authentication**: Strict Google OAuth Gatekeeper Modal (`GoogleGatekeeperModal.tsx`)
- **Deployment**: Vercel Serverless Edge

---

## ⚙️ Environment Variables (`.env`)

```env
PORT=8080
NODE_ENV=development
SESSION_SECRET=your_hmac_sha256_secret_key
MONGO_URI=mongodb+srv://user:pass@cluster.mongodb.net/indexmatrix
FIREBASE_PROJECT_ID=himanshu-bio-seo
FIREBASE_CLIENT_EMAIL=firebase-adminsdk@himanshu-bio-seo.iam.gserviceaccount.com
FIREBASE_PRIVATE_KEY="-----BEGIN PRIVATE KEY-----\n..."
TELEGRAM_BOT_TOKEN=123456789:ABCdefGHIjklMNOpqrsTUVwxyz
TELEGRAM_STORAGE_CHANNEL_ID=-1001234567890
```

---

## 👤 Author & Maintainer
**Himanshu** - [@himanshulm9-debug](https://github.com/himanshulm9-debug)
