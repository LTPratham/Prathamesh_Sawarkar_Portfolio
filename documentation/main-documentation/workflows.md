# Workflows & Operations Guide

## 1. Local Development Workflow

### Prerequisites
- Node.js 18+ (optional, for local `serve` or `prettier`) or Python 3.x.

### Steps
1. Run local dev server:
   ```bash
   npm run dev
   # or
   python -m http.server 3000
   ```
2. Open `http://localhost:3000`.
3. Format code prior to commits:
   ```bash
   npm run format
   ```

---

## 2. Adding a New Project Case Study

To add a new project to the portfolio:
1. Open `index.html`.
2. Locate the `PROJECTS` array (around line 1650).
3. Add a new project object:
   ```javascript
   {
     slug: 'new-project-slug',
     num: '09',
     title: 'Project Title',
     short: 'Brief one-line summary.',
     tags: ['React', 'Python', 'AI'],
     thumbColor: 'var(--cyan)',
     problem: 'Problem statement describing the engineering challenge.',
     why: 'Personal or business rationale.',
     approach: 'Architecture and methodology applied.',
     stack: ['Technology 1', 'Technology 2'],
     contribution: 'Individual role and deliverables.',
     result: 'Outcomes, performance, or deployment status.',
     flow: ['Step 1', 'Step 2', 'Step 3', 'Outcome']
   }
   ```
4. If you have screenshots, place them in `assets/projects/` and add `evidenceImage: 'assets/projects/your-image.png'`.

---

## 3. Adding a New Certificate

1. Place the PDF certificate file into `assets/certificates/`.
2. Generate a preview thumbnail PNG (approx. 800px width) and place into `assets/certificates/previews/`.
3. Open `index.html` and add an entry to the `CERTIFICATES` array:
   ```javascript
   {
     slug: 'certificate-slug',
     num: '09',
     title: 'Certificate Name',
     org: 'Issuing Organization',
     meta: ['Completion Date: ...', 'Credential ID: ...'],
     file: 'assets/certificates/filename.pdf',
     preview: 'assets/certificates/previews/filename.png',
     fileType: 'pdf'
   }
   ```

---

## 4. Vercel & GitHub Deployment Workflow

```
Developer Local
   │
   ├─► git add .
   ├─► git commit -m "feat: new project added"
   └─► git push origin main
         │
         ├───► GitHub Actions (Runs CI checks & GitHub Pages deploy)
         │
         └───► Vercel Git Integration
                 │
                 ▼
          Automatic Zero-Downtime Production Deployment
          (https://prathameshsawarkar.vercel.app)
```
