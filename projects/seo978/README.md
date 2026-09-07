# ⚡ seo978 — SEO-INDEXING Technical SEO Engine & DOM Crawler

<div align="center">

[![GitHub repo](https://img.shields.io/badge/GitHub-himanshulm9--debug%2Fseo978-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/himanshulm9-debug/seo978)
[![Direct Deployment](https://img.shields.io/badge/Direct%20Live-seo978.vercel.app-0070F3?style=for-the-badge&logo=vercel&logoColor=white)](https://seo978.vercel.app)
[![Multi--Zone Stream](https://img.shields.io/badge/Multi--Zone-himanshu--bio.vercel.app%2Fapps%2Fseo-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://himanshu-bio.vercel.app/apps/seo)
[![Google OAuth](https://img.shields.io/badge/Auth-Google%20OAuth%202.0-EA4335?style=flat-square&logo=google)](https://firebase.google.com/)
[![NLP Engine](https://img.shields.io/badge/NLP-pdf--parse%20v2-green?style=flat-square)](https://www.npmjs.com/package/pdf-parse)

<p align="center">
  Enterprise on-page SEO diagnostics, live DOM crawler, binary document NLP keyword extractor, competitor gap analyzer, and Googlebot indexing automation.
</p>

</div>

---

## 🌟 Overview

**SEO-INDEXING (`seo978`)** is a technical SEO automation suite designed to inspect, audit, and accelerate search engine visibility. Built with a responsive cyberpunk glassmorphism interface, it features deep DOM hierarchy inspection, binary document keyword extraction, competitor keyword gap analysis, real-time broken link probing, and automated Google Indexing API submission.

It is accessible both directly via **[seo978.vercel.app](https://seo978.vercel.app)** and via the main portfolio multi-zone rewrite at **[himanshu-bio.vercel.app/apps/seo](https://himanshu-bio.vercel.app/apps/seo)**.

---

## 🔐 Identity Architecture: Persistent Guest UID & Account Unification

To balance frictionless visitor trial with abuse prevention, **SEO-INDEXING implements an automated guest-to-user unification architecture**:

```
Unauthenticated Visitor arrives at seo978
         │
         ▼
[Auto-Assign Persistent Device UID] (guest_<rand>_<timestamp> stored in localStorage)
         │
         ├── Guest Clearance: 20 scans/day (20s cooldown)
         └── Isolated Guest History Partition: seo_scan_history_guest_...
         │
         ▼ User Clicks "Sign in with Google"
[Google OAuth Authentication] (Firebase browserLocalPersistence)
         │
         ├── 1. Local State Migration: mergeGuestHistoryToUser(guestId, googleUser.uid)
         ├── 2. Backend Reconciliation: userStore.linkGuestToUser(guestId, googleUser.uid)
         └── 3. Result: Guest and Google data are permanently unified into one!
```

- **Frictionless Guest Allowance**: First-time visitors are automatically assigned a persistent unique browser UID and can immediately run audits without mandatory signup.
- **Account Unification**: The instant a user signs in with Google, all their prior guest scans, document analyses, and broken link audits are automatically migrated into their Google account partition with zero data loss.
- **Admin Quota Slider & Telemetry Sync**: The Super Admin can dynamically adjust any user's daily limit (from 0 to 200+ scans/day) or toggle active/blocked status via the Admin Command Center (`/admin`), which propagates instantly in real-time.
- **Super Admin Auto-Elevation**: Verified admin (`himanshulm9@gmail.com`) receives automatic Level 5 `⚡ UNLIMITED` clearance with 0-second cooldown.

---

## 🛠️ Core Diagnostic Modules

### 1. Live Web Crawler & DOM Security Inspector (`CrawlerTab.tsx`)
- Parses complete HTML DOM structure, HTTP response headers, OpenGraph / Twitter Cards, canonical tags, and robots directives.
- Real-time accessibility, contrast, and mobile viewport responsive checks.
- Dynamic animated SVG radial health gauges with color-graded feedback.
- Account-isolated scan history partition with 1-click historical report reload and re-scan.

### 2. Binary PDF & Document NLP Keyword Extractor (`NlpUploadTab.tsx`)
- Drag-and-drop document NLP keyword extraction engine supporting `.pdf`, `.docx`, `.txt`, and `.csv`.
- Extracts 1-, 2-, and 3-word n-gram keyphrases, keyword density percentages, and search intent classification.
- Document uploads are processed ephemerally and tunneled to Telegram Cloud Storage, consuming **0 MB permanent server disk**.

### 3. Competitor Keyword Gap & Overlap Engine (`CompetitorGapTab.tsx`)
- Side-by-side crawl comparison of your domain against competitor URLs.
- Identifies common ranking keywords, missed keyword opportunities, and content gaps.
- Account-isolated competitor comparison drawer.

### 4. Real-Time Broken Link & Redirect Inspector (`BrokenLinksTab.tsx`)
- Concurrently probes internal and external hyperlinks for `200 OK`, `301/302` redirects, and `404/500` dead links.
- Exportable CSV audit reports with response latency profiling and account-isolated history.

### 5. Search Engine Bot Dispatcher (`BotIndexerTab.tsx`)
- Automated batch submission of URLs and XML sitemaps to Google Indexing API and IndexNow.
- Validates Google Cloud Service Account JSON keys before publishing with cooldown protection.

---

## 🚀 Local Development Setup

```bash
# Clone the repository
git clone https://github.com/himanshulm9-debug/seo978.git
cd seo978

# Install dependencies
npm install

# Run local development server
npm run dev

# Build for production
npm run build
```

---

## 🛠️ Tech Stack

- **Language & Framework**: TypeScript 5.7, React 19
- **Bundler & Tooling**: Vite 6, Rollup
- **Styling**: Tailwind CSS with Cyber-Glass Design Tokens
- **Icons**: Lucide React
- **Authentication**: Firebase Authentication with `browserLocalPersistence` and Google OAuth
- **Deployment**: Vercel Serverless Edge

---

## 👤 Author & Maintainer
**Himanshu** - [@himanshulm9-debug](https://github.com/himanshulm9-debug)
