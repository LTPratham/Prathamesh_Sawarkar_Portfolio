# Bug & Quality Audit Log: Initial Repository Setup

**Date**: 2026-09-01  
**Category**: Repository Structure & Deployment Optimization  
**Severity**: Medium (Deployment Friction / SEO)  
**Status**: Resolved  

---

## 1. Description
Prior to setup, all portfolio source code and assets resided inside a subfolder (`portfolio/`). When pushed to GitHub and connected to Vercel, this caused two primary issues:
1. **GitHub Experience**: Visiting the GitHub repository root showed only a single folder rather than immediate repository documentation and files.
2. **Vercel Zero-Config Deployment**: Vercel defaults to building from the repository root `./`. Without setting a manual Root Directory override in the Vercel dashboard, static deployment would fail to locate `index.html`.
3. **SEO & Social Sharing Missing**: Missing OpenGraph/Twitter meta tags meant link sharing across LinkedIn, Twitter, Discord, and WhatsApp would lack rich unfurl cards. Missing favicon caused 404 console requests.

---

## 2. Root Cause
Initial folder bundling placed all site assets under a subfolder without automated root deployment configuration or manifest files.

---

## 3. Fix Applied
1. Moved `portfolio/index.html` and `portfolio/assets/` to repository root (`./index.html`, `./assets/`).
2. Configured `vercel.json` with explicit caching and security headers.
3. Added high-contrast Neobrutalist inline SVG favicon, OpenGraph, Twitter card tags, `site.webmanifest`, `robots.txt`, and `sitemap.xml`.
4. Initialized Git version control with `.gitignore` and `.gitattributes` to prevent tracking of OS/editor artifacts and to normalize LF line endings.

---

## 4. Files Modified / Created
- `index.html` (Updated `<head>` with SEO, OpenGraph, Twitter, Favicon, Manifest tags)
- `vercel.json` (Created)
- `package.json` (Created)
- `README.md` (Created)
- `site.webmanifest` (Created)
- `robots.txt` (Created)
- `sitemap.xml` (Created)
- `LICENSE` (Created)
- `CONTRIBUTING.md` (Created)
- `CODE_OF_CONDUCT.md` (Created)
- `SECURITY.md` (Created)
- `.github/workflows/deploy.yml` (Created)
- `.github/workflows/ci.yml` (Created)
- `.github/ISSUE_TEMPLATE/bug_report.yml` (Created)
- `.github/ISSUE_TEMPLATE/feature_request.yml` (Created)
- `.github/PULL_REQUEST_TEMPLATE.md` (Created)
- `documentation/*` (Created)

---

## 5. Verification
- Verified all internal anchor navigation (`#home`, `#about`, `#projects`, etc.).
- Verified modal hash routing (`#project/...`, `#certificate/...`).
- Verified local serving via `npx serve` with zero broken assets or console errors.
