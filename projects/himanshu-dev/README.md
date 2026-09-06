# 🤖 himanshu-dev — Standalone YouTube Audio Player & Google Gemini AI Assistant

<div align="center">

[![GitHub repo](https://img.shields.io/badge/GitHub-himanshulm9--debug%2Fhimanshu--dev-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/himanshulm9-debug/himanshu-dev)
[![Status](https://img.shields.io/badge/Architecture-Decoupled%20Micro--App-8A2BE2?style=for-the-badge)](https://github.com/himanshulm9-debug/himanshu-dev)
[![Google Gemini](https://img.shields.io/badge/AI-Google%20Gemini%20Flash%20%2F%20Pro-4285F4?style=flat-square&logo=google)](https://ai.google.dev/)
[![YouTube API](https://img.shields.io/badge/Media-YouTube%20IFrame%20API-FF0000?style=flat-square&logo=youtube)](https://developers.google.com/youtube)

<p align="center">
  A dedicated developer cockpit combining a persistent YouTube background audio streamer with a multimodal Google Gemini conversational AI assistant.
</p>

</div>

---

## 🌟 Overview

**`himanshu-dev`** is an independent, standalone project intentionally decoupled from the primary `himanshu-bio-combined` portfolio monorepo. It serves as an interactive multimedia and intelligence workstation featuring:

1. **Persistent YouTube Media Station**: Low-latency, uninterrupted background audio streaming with playlist queue management, volume controls, and track scrubbing.
2. **Google Gemini Conversational AI**: High-velocity developer chat assistant powered by the Google Gemini API with syntax-highlighted code blocks, streaming responses, and contextual memory.

---

## 💡 Why Decoupled from `himanshu-bio-combined`?

During the system architecture design, the YouTube streaming player and Gemini AI chat UI were strategically extracted into `himanshu-dev` for several critical architectural reasons:

| Rationale | Detail |
| :--- | :--- |
| **🚀 Lighthouse Performance** | Heavy third-party media iframes (`www.youtube.com/iframe_api`) and bulky AI client SDKs add significant JavaScript execution time. Isolating them preserves 95+ Lighthouse performance on the main portfolio. |
| **🎧 Audio Playback Persistence** | YouTube audio streams stutter or reset when parent DOM trees unmount during multi-zone navigation. Decoupling ensures media playback is isolated and uninterrupted. |
| **🔑 API Key & Quota Isolation** | Google Gemini API quotas, rate-limiting, and client-side token consumption are segregated from core portfolio and SEO audit operations. |
| **📦 Micro-Frontend Modularity** | Keeps the primary portfolio lightweight, elegant, and strictly focused on showcase presentations, career profiles, and live tools. |

---

## ✨ Features

### 1. 🎵 Persistent YouTube Audio Player
- Embedded headless YouTube player utilizing the official YouTube IFrame Player API.
- Support for custom playlists, video search, volume normalization, and background loop modes.
- Keyboard shortcuts for play/pause (`Space`), next track (`Ctrl+Right`), and mute (`M`).

### 2. 🧠 Google Gemini AI Conversational Assistant
- Direct integration with Google Gemini 1.5 Flash / Pro models via `@google/genai`.
- Live token streaming for instantaneous response rendering.
- Markdown rendering with code block copy buttons and programming language tag detection.
- Contextual prompt templates for code explanation, refactoring, and technical Q&A.

### 3. 🎨 Dark Cyber-Cockpit UI
- Minimalist, distraction-free developer interface.
- Glassmorphic panels, responsive drawer layouts, and custom sound wave animations.

---

## 🚀 Local Development Setup

```bash
# Clone the repository
git clone https://github.com/himanshulm9-debug/himanshu-dev.git
cd himanshu-dev

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env

# Start development server
npm run dev
```

---

## ⚙️ Environment Variables Reference (`.env`)

```env
PORT=3001
VITE_GEMINI_API_KEY=AIzaSy...your_gemini_api_key
VITE_DEFAULT_PLAYLIST_ID=PL...your_favorite_playlist
```

---

## 👤 Author & Maintainer
**Himanshu** - [@himanshulm9-debug](https://github.com/himanshulm9-debug)
