# Product Requirements Document (PRD)

## 1. Product Overview

**Product Name**: Prathamesh Sawarkar Portfolio  
**Target URL**: `https://prathameshsawarkar.vercel.app/`  
**Owner**: Prathamesh Sawarkar  
**Classification**: High-Performance Personal Engineering Portfolio & Technical Showcase  

---

## 2. Problem Statement & Target Audience

### Problem Statement
Standard engineering portfolios often suffer from template conformity, heavy JavaScript framework overhead, slow initial page loads, and superficial project showcases that fail to demonstrate deep technical rigor across software, AI, cybersecurity, and hardware.

### Target Audience
- **Technical Recruiters & Hiring Managers**: Seeking top-tier software engineers with AI, cybersecurity, and full-stack capabilities.
- **Venture Founders & Collaborators**: Exploring innovative partnerships in AI, assistive technology, IoT, and brain-computer interfaces.
- **Academic & Engineering Peers**: Reviewing research, patent-filed innovations (BCI), and open-source contributions.

---

## 3. Core Functional Requirements

### 3.1. Neobrutalist UI & Theming
- **Tokens**: High-contrast Neobrutalist tokens (`--bg`, `--cyan`, `--magenta`, `--yellow`, `--border: 3px solid var(--black)`, `--shadow-lg: 8px 8px 0 var(--black)`).
- **Dual Themes**: Instant Light Mode (`#F5F0DC`) and Dark Mode (`#121212`) toggling with persistent `localStorage` synchronization and OS `prefers-color-scheme` support.
- **Fluid Layout**: Full responsive support spanning mobile devices (320px) to ultra-wide desktop monitors (1920px+).

### 3.2. Project Showcase & Deep Linking
- **Dynamic Hash Router**: Client-side hash routing supporting `#project/:slug` and `#certificate/:slug`.
- **System Flow Visualizer**: Built-in SVG-style step-by-step pipeline visualizer for every project case study without external charting libraries.
- **Modals & Accessibility**: Accessible modal overlay with focus trapping, `Escape` key listeners, background click dismissal, and proper `aria-modal` / `role="dialog"` attributes.

### 3.3. Verified Achievements & Certificate Hub
- **Direct Viewer**: Real-time modal viewing for verified certificates from Cisco, Infosys Springboard, InternsElite, Times Foundation, and NIIT.
- **Asset Access**: Direct links to original PDF certificates and resume (`assets/Prathamesh_Sawarkar_CV_FINAL.pdf`).

### 3.4. Security & Performance
- **Zero Heavy Runtime**: 100% Vanilla HTML5, CSS3, and ES6+ JavaScript.
- **Sub-100ms TTI**: Instant time-to-interactive with preconnected fonts and optimized asset delivery.
- **Security Headers**: Production-ready headers configured via `vercel.json` (CSP, X-Frame-Options, X-Content-Type-Options, Referrer-Policy).

---

## 4. Non-Functional Requirements

- **Availability**: 99.99% uptime via Vercel Edge Network.
- **Accessibility**: Compliance with WCAG 2.1 Level AA (contrast ratio > 4.5:1, skip-to-content links, visible focus outlines).
- **SEO Optimization**: Full OpenGraph protocol, Twitter cards, meta descriptions, sitemap.xml, and robots.txt.
