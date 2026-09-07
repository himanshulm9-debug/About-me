# ⚡ himanshu-bio-server — High-Performance Fastify Backend & Telegram Cloud Tunnel

<div align="center">

[![GitHub repo](https://img.shields.io/badge/GitHub-himanshulm9--debug%2Fhimanshu--bio--server-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/himanshulm9-debug/himanshu-bio-server)
[![Deployment](https://img.shields.io/badge/Deployment-Render.com%20Web%20Service-46E3B7?style=for-the-badge&logo=render&logoColor=black)](https://render.com)
[![Fastify](https://img.shields.io/badge/Fastify-v5-black?style=flat-square&logo=fastify)](https://fastify.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Telegram Storage](https://img.shields.io/badge/Storage-Telegram%20Tunnel%200MB%20Disk-2CA5E0?style=flat-square&logo=telegram)](https://core.telegram.org/bots/api)

<p align="center">
  The asynchronous backend engine for Himanshu's portfolio ecosystem. Built with Fastify (~75,000 req/sec), TypeScript, and Telegram Bot API document tunneling for 100% free, 0 MB permanent disk cloud storage.
</p>

</div>

---

## 🌟 Overview

**`himanshu-bio-server`** is the headless API and microservice backend serving the **Bio Hub (`himanshu-bio.vercel.app`)** and **SEO Engine (`seo978.vercel.app`)**. It provides real-time DOM crawler parsing, rate-limiting & quota tracking, and document ingestion without incurring cloud disk storage fees.

---

## ✈️ Telegram Cloud Storage Tunneling (0 MB Permanent Disk)

Cloud hosting platforms like Render.com have ephemeral disks or strict storage quotas on free tiers. To eliminate storage costs and disk overflow vulnerabilities, **`himanshu-bio-server` implements Telegram Cloud Tunneling**:

```
[User Document Upload] (PDF / DOCX / TXT)
            │
            ▼
[Fastify Multipart Ingestion] ── Buffer stored temporarily in /tmp
            │
            ▼
[Telegram Bot API: bot.sendDocument()] ── Direct TLS Stream
            │
            ▼
[Private Telegram Storage Channel] ── Permanent, unlimited cloud storage
            │
            ▼
[Immediate Purge: fs.unlinkSync()] ── Local file deleted instantly
            │
            ▼
[0 MB Permanent Disk Usage on Render.com]
```

### Key Technical Attributes:
1. **Zero Permanent Footprint**: Uploaded files reside in `/tmp` for less than 800ms before being piped to Telegram and purged with `fs.unlinkSync()`.
2. **Infinite Free Retention**: Telegram acts as an unlimited object store for document archives and SEO audit snapshots.
3. **Document Tracking**: Channel message ID, file name, and file size are returned to the client and indexed in Firestore.

---

## 🛡️ Quota & Abuse Prevention (`middleware/quota.ts`)

- **Strict Google Auth Enforcement**: Rejects unauthenticated guest crawl requests with `HTTP 401 Unauthorized`.
- **Google User Tier**: 20 deep technical scans per calendar day (UTC reset), tracked and synced via Upstash Redis KV / Firebase.
- **Admin Bypass**: Authenticated administrators bypass quota checks for unlimited audits.

---

## 📡 REST API Specifications

### 1. Technical SEO Crawler
- **Endpoint**: `POST /api/seo/scan`
- **Headers**: `Authorization: Bearer <Google_ID_Token>`
- **Payload**:
  ```json
  {
    "url": "https://example.com"
  }
  ```
- **Response**: Full DOM audit, title, meta descriptions, open graph tags, canonical links, heading hierarchy (H1-H6), broken links, performance estimate, and security score.

### 2. Document NLP Ingestion
- **Endpoint**: `POST /api/seo/upload`
- **Headers**: `Authorization: Bearer <Google_ID_Token>`, `Content-Type: multipart/form-data`
- **Payload**: Form file field `file` (`.pdf`, `.docx`, `.txt`, `.csv`)
- **Process**: Parses keyphrases using binary NLP streaming, pipes file to Telegram Storage Channel, purges local `/tmp` file, and returns analysis metrics with `telegramMessageId`.

### 3. Service Health Check
- **Endpoint**: `GET /health`
- **Response**: `{ "status": "ok", "timestamp": "2026-09-06T11:42:00.000Z" }`

---

## 🚀 Local Development Setup

```bash
# Clone the repository
git clone https://github.com/himanshulm9-debug/himanshu-bio-server.git
cd himanshu-bio-server

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env

# Build TypeScript
npm run build

# Start production server
npm run start

# Or run in development watch mode
npm run dev
```
The server will start listening at `http://localhost:5000`.

---

## ⚙️ Environment Variables Reference (`.env`)

```env
PORT=5000
NODE_ENV=development
ALLOWED_ORIGINS=https://himanshu-bio.vercel.app,https://seo978.vercel.app,https://crypto978.vercel.app

# Telegram Cloud Storage Tunnel
TELEGRAM_BOT_TOKEN=123456789:ABCdefGHIjklMNOpqrsTUVwxyz
TELEGRAM_STORAGE_CHAT_ID=-1001234567890

# Rate Limiting & Quota Management (Upstash Redis)
KV_REST_API_URL=https://upstash-redis-instance.upstash.io
KV_REST_API_TOKEN=your_upstash_redis_token

# Email & Notifications (Resend)
RESEND_API_KEY=re_123456789
EMAIL=contact@himanshu.dev
```

---

## ☁️ Render.com Deployment

A pre-configured `render.yaml` blueprint is included in the repository root. Simply connect the repository to Render.com as a **Web Service** and supply the private environment variables in the Render dashboard.

---

## 👤 Author & Maintainer
**Himanshu** - [@himanshulm9-debug](https://github.com/himanshulm9-debug)
