# 💻 himanshu-bio-ui — Main Portfolio Hub & Multi-Zone Router

<div align="center">

[![GitHub repo](https://img.shields.io/badge/GitHub-himanshulm9--debug%2Fhimanshu--bio--ui-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/himanshulm9-debug/himanshu-bio-ui)
[![Vercel Deployment](https://img.shields.io/badge/Live-himanshu--bio.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://himanshu-bio.vercel.app)
[![Next.js](https://img.shields.io/badge/Next.js-16-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-blue?style=flat-square&logo=react)](https://react.dev/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-v4-38B2AC?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)
[![Three.js](https://img.shields.io/badge/3D-Three.js-black?style=flat-square&logo=three.js)](https://threejs.org/)

<p align="center">
  The flagship frontend for Himanshu's portfolio ecosystem. Built with Next.js 16 (App Router), Three.js 3D particle canvas, and Vercel Multi-Zone Edge Rewrites linking the entire suite seamlessly.
</p>

</div>

---

## ✨ Features

- 🌌 **3D Particle Cosmos Hero**: Dynamic interactive Three.js WebGL particle field that tracks mouse movements and camera physics.
- 🎴 **Cyberpunk Bento Grid**: High-density interactive application cards with hover spotlights and instant launcher buttons.
- 🌐 **Vercel Multi-Zone Edge Router**: Routes `/apps/seo/*` and `/apps/crypto/*` to independent Vercel deployments at the edge in `<50ms` with zero reload flash.
- 🛸 **Shared Glassmorphic Dock**: Floating Mac-style navigation dock with automatic background hover pre-fetching (`<link rel="prefetch">`).
- 👤 **Persona & Mindset Showcase**: Interactive cards featuring cybersecurity credentials (MCA at Poornima University, BCA at PCGE Parishkar), Arch Linux cockpit, concept-only development ethos, and gaming/soundtrack dashboard.
- 📝 **Resume Studio**: Interactive resume builder with ATS-friendly templates and instant PDF generation.

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/himanshulm9-debug/himanshu-bio-ui.git
cd himanshu-bio-ui

# Install dependencies
npm install

# Start local development
npm run dev
```
Open [http://localhost:3000](http://localhost:3000).

---

## ⚙️ Edge Rewrites Configuration (`vercel.json`)

```json
{
  "rewrites": [
    { "source": "/apps/seo/:path*", "destination": "https://seo978.vercel.app/:path*" },
    { "source": "/apps/crypto/:path*", "destination": "https://crypto978.vercel.app/:path*" }
  ]
}
```

---

## 👤 Author
**Himanshu** - [@himanshulm9-debug](https://github.com/himanshulm9-debug)
