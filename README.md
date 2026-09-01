<div align="center">

# ⚡ Prathamesh Sawarkar — Developer Portfolio

**Software Engineer · Artificial Intelligence · Cybersecurity · IoT · Human Impact**

[![Live on Vercel](https://img.shields.io/badge/Vercel-Live%20Demo-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://prathameshsawarkar.vercel.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-FFD600?style=for-the-badge&logo=opensourceinitiative&logoColor=black)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![WCAG AA](https://img.shields.io/badge/Accessibility-WCAG%20AA-08C5CE?style=for-the-badge&logo=w3c&logoColor=white)](#accessibility--performance)

<br />

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-featured-projects">Projects</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-quick-start">Quick Start</a> •
  <a href="#-deployment">Deployment</a> •
  <a href="#-documentation">Documentation</a> •
  <a href="#-contact">Contact</a>
</p>

---

</div>

## 📌 Overview

This is the personal portfolio of **Prathamesh Sawarkar**, a B.Tech Honours student in **Cyber Security & Blockchain** at **Lovely Professional University (LPU)**. 

The portfolio is built with a bespoke **Neobrutalist design system** — bold borders, crisp hard shadows, punchy CMYK-inspired accents, zero external UI framework bloat, and sub-100ms load times.

---

## ✨ Features

- 🎨 **Neobrutalist Aesthetic**: Hand-crafted tokens (`--bg`, `--cyan`, `--magenta`, `--yellow`), signature hard offsets, custom grid rails, and dynamic typography.
- 🌓 **Theme Engine**: Instant Light / Dark mode toggle with persistent state saved via `localStorage` and system color-scheme detection fallback.
- 📱 **Fully Responsive & Accessible**: Custom desktop rail navigation + accessible modal drawer for mobile screens. Built according to **WCAG 2.1 AA** standards with full keyboard trap support, focus indicators, and ARIA attributes.
- 🔍 **Interactive Project Modal & Router**: Dynamic hash routing (`#project/:slug` and `#certificate/:slug`) with embedded interactive system-flow diagrams and deep links.
- 📜 **Live Verified Certificate & Evidence Viewer**: Real-time modal viewer for certificates (Cisco, Infosys Springboard, InternsElite, Times Foundation, NIIT) with full PDF preview integration.
- 🚀 **Zero-Config Deployment**: Optimized static architecture with caching headers, security policies, OpenGraph metadata, and full Vercel / GitHub Pages compatibility.

---

## 🛠️ Tech Stack & Design System

| Layer | Technologies / Tokens |
| :--- | :--- |
| **Structure** | Semantic HTML5, Microdata, OpenGraph & Twitter Card Meta |
| **Styling** | Modern CSS3 (CSS Custom Properties, CSS Grid, Flexbox, Fluid Typography) |
| **Typography** | `Syne` (Display/Headings), `Space Grotesk` (Subheads), `Inter` (Body), `Space Mono` (Data/Chips) |
| **Interactivity** | Vanilla JavaScript (ES6+), Hash History Routing, IntersectionObserver, Keyboard Trap Focus |
| **Performance** | Zero runtime dependencies, 100/100 Lighthouse Performance, sub-50KB bundle |
| **Hosting** | Vercel (Edge Network) & GitHub Pages |

---

## 📂 Featured Projects Showcased

1. 🧠 **AI Rehabilitation Platform** — Full-stack rehabilitation suite with doctor, patient, and admin portals powered by OpenCV and MediaPipe computer vision exercise tracking.
2. 📊 **LPU CodeViz** — Interactive academic visualization platform built with React, Vite, and Tailwind CSS for computer science students.
3. 💊 **Smart Pharmacy System** — Automated pharmacy workflow management with digital prescriptions and real-time inventory automation.
4. 🗳️ **Biometric EVM** — Hardware-embedded electronic voting machine featuring biometric voter authentication and cryptographic anti-fraud logging.
5. ✋ **Touchless Appliance Control** — Arduino & ultrasonic sensor-driven hands-free appliance automation.
6. 🦾 **Rehabilitation Hand** — Sensor-driven assistive embedded system for post-paralysis hand movement therapy.
7. 🛡️ **Face Recognition System (Maharashtra Police)** — Photo/CCTV matching tool built as freelance crime-investigation software.
8. 📞 **CDR Analysis System (Maharashtra Police)** — Call Detail Record processing and relationship mining pipeline built for investigative analysis.

---

## 🚀 Quick Start (Local Development)

### 1. Clone the repository
```bash
git clone https://github.com/LTPratham/Prathamesh_Sawarkar_Portfolio.git
cd Prathamesh_Sawarkar_Portfolio
```

### 2. Run locally

You can serve the portfolio using any standard static file server:

#### Option A: Using NPM & Serve
```bash
npm install
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

#### Option B: Using Python
```bash
# Python 3
python -m http.server 3000
```

#### Option C: Using VS Code Live Server
Right-click `index.html` and select **"Open with Live Server"**.

---

## ☁️ Deployment

### Deploy to Vercel (Recommended)

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FLTPratham%2FPrathamesh_Sawarkar_Portfolio)

1. Push your repository to **GitHub**.
2. Go to [Vercel Dashboard](https://vercel.com/dashboard) and click **"Add New"** > **"Project"**.
3. Import your `Prathamesh_Sawarkar_Portfolio` repository.
4. Leave all build settings as default (Framework Preset: `Other`, Root Directory: `./`).
5. Click **Deploy**. Vercel will immediately deploy and provide an SSL-secured live URL.

### Deploy to GitHub Pages

1. Navigate to your repository on GitHub: **Settings** > **Pages**.
2. Under **Build and deployment** > **Source**, choose **GitHub Actions** (or **Deploy from a branch** -> `main` / `/root`).
3. Your site will automatically build and publish to `https://<username>.github.io/<repo-name>/`.

---

## 🧠 Documentation ("Project Brain")

This repository maintains formal system documentation following the standardized project-brain architecture:

```
documentation/
├── implementation-plans/    # Dated technical plans and roadmaps
├── main-documentation/       # PRD, System Architecture, & Workflows
│   ├── prd.md               # Product Requirements Document
│   ├── system-architecture.md# Neobrutalism design tokens & component system
│   └── workflows.md         # Release, Vercel deployment, & maintenance guides
├── licensing/               # Software licenses & acceptable use policy
├── progress-tracking/       # Living progress & milestone tracker
└── bugs-and-fixes/          # Historical records of fixes and audits
```

---

## 📞 Connect & Contact

- 🌐 **Portfolio Live**: [prathameshsawarkar.vercel.app](https://prathameshsawarkar.vercel.app)
- 💼 **LinkedIn**: [linkedin.com/in/prathamesh-sawarkar](https://www.linkedin.com/in/prathamesh-sawarkar)
- 🐙 **GitHub**: [@LTPratham](https://github.com/LTPratham)
- 📧 **Email**: [Prathameshsawarkar1@gmail.com](mailto:Prathameshsawarkar1@gmail.com)
- 📱 **Phone**: +91 87678 63134

---

<div align="center">

© 2026 **Prathamesh Sawarkar**. Built with passion, discipline, and Neo-Brutalist precision.

</div>
