# Implementation Plan: Portfolio Vercel & GitHub Repository Setup

**Date**: 2026-09-01  
**Author**: Antigravity Assistant & Prathamesh Sawarkar  
**Status**: Implemented  

---

## 1. Executive Summary

This implementation plan covers the restructuring and deployment readiness setup for Prathamesh Sawarkar's personal engineering portfolio. The goal is to transition the project from a local subfolder into a production-grade, open-source-ready GitHub repository with zero-friction continuous deployment on Vercel and GitHub Pages.

---

## 2. Scope of Work

1. **Repository Structure Migration**:
   - Flatten nested `portfolio/` directory structure to repository root (`./index.html`, `./assets/`).
   - Standardize asset references across projects, certificates, previews, and PDF documents.

2. **Vercel & Web Server Configuration**:
   - Create `vercel.json` with strict security headers (Content Security Policy, X-Frame-Options, X-Content-Type-Options, Referrer-Policy, Permissions-Policy).
   - Configure cache control policies (immutable 1-year cache for static assets, revalidate for HTML).
   - Enable clean URLs and standard routing.

3. **SEO & Discovery Engine**:
   - Integrate OpenGraph (`og:title`, `og:description`, `og:image`, `og:url`, `og:type`) and Twitter Card meta tags.
   - Embed high-contrast Neobrutalist SVG favicon with inline fallback.
   - Generate `robots.txt`, `sitemap.xml`, and `site.webmanifest` for crawler indexing and mobile web app support.

4. **GitHub Open Source Infrastructure**:
   - Complete `README.md` with interactive live demo badge, visual structure, project breakdowns, quick-start guide, and contact channels.
   - Add `.github/workflows/deploy.yml` and `ci.yml` for automated GitHub Pages hosting and static file integrity testing.
   - Establish `LICENSE` (MIT), `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, and issue/PR templates.

5. **Project Brain Documentation**:
   - Full suite under `documentation/` covering PRD, architecture, workflows, licensing, progress, and audit logs.

---

## 3. Verification & Quality Assurance

- **Link Audit**: Verify all relative anchors (`#about`, `#experience`, `#projects`, `#innovation`, `#achievements`, `#skills`, `#human-impact`, `#career-goal`, `#contact`) and modal hash routes (`#project/...`, `#certificate/...`).
- **Asset Integrity**: Verify all PDF downloads (`Prathamesh_Sawarkar_CV_FINAL.pdf`, certificate PDFs) and preview images (`assets/certificates/previews/*.png`, `assets/portrait.jpg`).
- **Performance & Accessibility**: Ensure zero external script dependencies, WCAG AA contrast compliance, keyboard focus trapping on modals, and smooth animations with reduced-motion fallbacks.
