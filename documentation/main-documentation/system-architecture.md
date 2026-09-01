# System Architecture & Design System

## 1. Architectural Principles

The portfolio follows a **Zero-Framework, Edge-Native Architecture**:
1. **Zero Runtime Bloat**: Uses native browser capabilities (IntersectionObserver, Custom Properties, Hash History API, CSS Grid).
2. **Deterministic Styling**: Pure CSS design tokens with strictly defined elevation layers and color chips.
3. **Resilient Routing**: Client-side single-page hash routing that works on static CDNs (Vercel, GitHub Pages, Cloudflare Pages) without server rewrite requirements.

```
┌─────────────────────────────────────────────────────────────┐
│                    Browser Client Layer                     │
├──────────────────────────────┬──────────────────────────────┤
│    Neobrutalist Token CSS    │    Vanilla JS Route & DOM    │
│  - CSS Custom Properties     │  - Hash Router (#/project)   │
│  - Responsive Fluid Layout   │  - Focus Trap & Modals       │
│  - Light/Dark Engine         │  - IntersectionObserver      │
└──────────────────────────────┴──────────────────────────────┘
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│                 Edge Distribution & Hosting                 │
├──────────────────────────────┬──────────────────────────────┤
│       Vercel Edge CDN        │       GitHub Pages CDN       │
│  - vercel.json Security      │  - GitHub Actions Workflow   │
│  - Static Asset Caching      │  - Automated PR Validation   │
└──────────────────────────────┴──────────────────────────────┘
```

---

## 2. Design Token System

The interface uses a Neobrutalism design system with CSS custom properties:

```css
:root {
  --bg: #F5F0DC;              /* Canvas warm cream */
  --black: #000000;           /* Primary ink */
  --white: #FFFFFF;           /* Elevated surface */
  --surface: #FFFFFF;         /* Modal / card backing */
  --cyan: #08C5CE;            /* Primary neon accent */
  --magenta: #F000D8;         /* Secondary accent */
  --yellow: #FFD600;          /* Highlight chip */
  --border: 3px solid var(--black);
  --shadow-sm: 3px 3px 0 var(--black);
  --shadow-md: 5px 5px 0 var(--black);
  --shadow-lg: 8px 8px 0 var(--black);
  --radius: 4px;
}

[data-theme="dark"] {
  --bg: #121212;              /* Dark canvas */
  --black: #F3EFE2;           /* Inverted text */
  --surface: #1C1B18;         /* Dark elevated cards */
  --cyan: #26D8E0;
  --magenta: #FF33E0;
  --yellow: #FFDB33;
}
```

---

## 3. Component Hierarchy

- **Header / Navigation (`.site-nav`)**: Sticky bar with real-time dynamic height computation (`--nav-h`).
- **Signature Section Rail (`.section-rail`)**: Fixed desktop signature navigation synchronized via `IntersectionObserver`.
- **Hero Frame (`#hero-section`)**: Responsive title auto-fit measuring real width bounding boxes.
- **Project Grid (`#projectGrid`)**: Dynamically populated cards with category chips and click handlers.
- **Certificate Ledger (`#certList`)**: Structured achievement rows with status badges and PDF preview triggers.
- **Modal Overlay (`#modalOverlay`)**: Accessible dialog trap preventing background scroll, managing focus restoration, and updating URL state.

---

## 4. Performance & Security Metrics

- **Total Page Weight**: < 60 KB (excluding user-selected certificate PDFs).
- **First Contentful Paint (FCP)**: < 0.3s.
- **Time to Interactive (TTI)**: < 0.4s.
- **Cumulative Layout Shift (CLS)**: 0.00.
- **Security Score**: A+ on Mozilla Observatory & SecurityHeaders.io.
