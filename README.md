# NexusAI — Intelligent Data Automation Platform

> **Frontend Battle 3.0 · IIT Bhubaneswar · Round 1 Submission**  
> Built by Lakshya Pandey · 26 June 2026

---

## 🚀 Live Demo

🔗 **[Live Site](https://nexusai-frontend-battle.vercel.app)** — Deployed on Vercel

📁 **[GitHub Repository](https://github.com/pandeylakshya207-max/nexusai-frontend-battle)**

---

## 📋 Overview

A premium, high-converting, responsive landing page for a next-generation AI-driven data automation platform. Built under a strict 4-hour countdown as part of **Frontend Battle 3.0** — the flagship event of the Web and Design Society, IIT Bhubaneswar.

> **Architecture Note:** This is a fully static frontend application — no backend, no server, no database, no API calls. All logic (pricing engine, state management, layout transitions) runs entirely client-side in the browser. This is intentional — the competition requires a landing page, and all feature requirements are implemented as pure frontend logic.

---

## ✅ Feature Checklist

### Feature 1 — Matrix-Driven Pricing & Performance-Isolated Currency Switcher
- [x] Three pricing tiers: **Starter**, **Pro**, **Enterprise**
- [x] Three currencies: **INR (₹)**, **USD ($)**, **EUR (€)**
- [x] Two billing cycles: **Monthly** / **Annual** with flat 20% discount multiplier
- [x] Multi-dimensional configuration matrix — **zero hardcoded UI values**
- [x] Regional tariff variables per currency baked into matrix
- [x] **State isolation**: currency/billing toggle updates ONLY targeted text nodes — no parent re-render, no global reflow
- [x] Verified clean in Chrome DevTools Performance tab

### Feature 2 — Bento-to-Accordion Wrapper with State Persistence
- [x] Desktop (>768px): Modern **Bento Grid** layout with hover active state tracking
- [x] Mobile (≤768px): Touch-optimized **Accordion** list
- [x] **Context Lock Constraint**: active hover index on desktop transfers to accordion on window resize past breakpoint
- [x] Smooth panel open via `requestAnimationFrame` on layout transition
- [x] **Zero external libraries** — no Framer Motion, no Radix, no Headless UI
- [x] Pure CSS Transitions with hardware-accelerated transforms

### SEO & Semantic HTML
- [x] Full `<meta>` tags, Open Graph (OG), Twitter Card
- [x] Semantic structure: `<header>`, `<main>`, `<section>`, `<article>`, `<nav>`, `<footer>`
- [x] ARIA labels, roles, `aria-expanded`, `aria-live`, `aria-checked`
- [x] Crawlable text nodes, no content locked in pseudo-elements

### Performance
- [x] Loader exits at **380ms** (under 500ms TTI budget)
- [x] Micro-interactions: **150–200ms** ease-out
- [x] Layout reflows: **300–350ms** ease-in-out
- [x] Google Fonts via `preconnect` — zero render blocking
- [x] Hardware-accelerated CSS transitions only — no runtime CSS-in-JS
- [x] `prefers-reduced-motion` respected

---

## 🎨 Design System

| Token | Name | Value |
|-------|------|-------|
| Background | Oceanic Noir | `#172B36` |
| Surface | Nocturnal Expedition | `#114C5A` |
| Primary | Forsythia | `#FFC801` |
| Accent | Deep Saffron | `#FF9932` |
| Text Primary | Arctic Powder | `#F1F6F4` |
| Text Secondary | Mystic Mint | `#D9E8E2` |
| Display Font | JetBrains Mono | Headers, code, labels |
| Body Font | Inter | Body text, UI elements |

---

## 🗂️ Project Structure

```
nexusai-frontend-battle/
├── index.html               # Entire app — single file, zero build step
├── README.md
├── arrow-path.svg
├── arrow-trending-up.svg
├── chart-pie.svg
├── chevron-down.svg
├── chevron-left.svg
├── chevron-right.svg
├── chevron-up-solid.svg
├── chevron-up.svg
├── cog-8-tooth.svg
├── cube-16-solid.svg
├── link-solid.svg
├── link.svg
├── search.svg
└── x-mark.svg
```

---

## 🛠️ Running Locally

No build step. No npm install. No configuration needed.

```bash
# Clone the repo
git clone https://github.com/pandeylakshya207-max/nexusai-frontend-battle.git

# Enter the folder
cd nexusai-frontend-battle
```

**Option A — VS Code Live Server (recommended)**
1. Open folder in VS Code
2. Install **Live Server** extension by Ritwick Dey
3. Click **Go Live** at bottom right
4. Opens at `localhost:5500`

**Option B — Direct browser**
```bash
start index.html      # Windows
open index.html       # macOS
xdg-open index.html   # Linux
```

---

## 🔍 How to Test Each Feature

### Feature 1 — Pricing Engine
1. Scroll to the **Pricing** section
2. Click the **Annual** toggle → prices drop 20%, "was ₹X/mo" note appears below
3. Click **$ USD** → all values switch to dollar pricing
4. Click **€ EUR** → switches to euro pricing with regional tariff applied
5. **DevTools check**: `F12` → Performance → Record → toggle currency → stop → verify zero layout shifts in timeline

### Feature 2 — Bento ↔ Accordion
1. On desktop (>768px): scroll to **Features** → hover any card → golden glow appears
2. **Context Lock test**: hover over card #3 (Workflow Orchestration) → drag browser window narrower than 768px → accordion appears with panel #3 **already open**
3. On mobile (`F12` → `Ctrl+Shift+M`): tap any accordion item → smooth open, others close

---

## 🚫 Libraries Deliberately Excluded

Per competition rules, the following are **not present** in this codebase:

| Library | Status |
|---------|--------|
| Framer Motion | ❌ Not used |
| Radix UI | ❌ Not used |
| Shadcn/UI | ❌ Not used |
| Headless UI | ❌ Not used |
| Tailwind UI | ❌ Not used |
| Any CSS-in-JS engine | ❌ Not used |

All animations use native **CSS Transitions** and the **Web Animations API (WAAPI)**.

---

## 📦 Tech Stack

| Layer | Choice | Reason |
|-------|--------|--------|
| Architecture | Static Frontend only | Zero backend — all logic client-side |
| Framework | Vanilla HTML / CSS / JS | Zero build overhead, fastest TTI |
| Styling | Custom CSS Variables | Full control, no runtime cost |
| Fonts | Google Fonts via preconnect | JetBrains Mono + Inter |
| Animations | Native CSS Transitions | Hardware-accelerated, no dependencies |
| Deployment | Vercel | Zero-config static hosting |

---

## 📊 Scoring Self-Assessment

| Criteria | Max | Notes |
|----------|-----|-------|
| Feature 1 — Dynamic pricing matrix | 15 pts | Multi-dimensional object, zero hardcoded values |
| Re-render & state isolation | 15 pts | Text node only updates, DevTools clean |
| Feature 2 — Bento/Accordion + context transfer | 10 pts | Zero deps, pure CSS, resize context lock |
| Semantic DOM layout | 15 pts | Full semantic HTML throughout |
| SEO hygiene & metadata | 10 pts | OG, Twitter, meta, ARIA |
| Loading performance | 5 pts | Loader exits at 380ms |
| Asset compliance & design polish | 15 pts | All 14 SVGs used, full color palette, both fonts |
| Breakpoint fluidity | 10 pts | Mobile, tablet, desktop all clean |
| Motion accuracy | 5 pts | Easing curves match spec |
| **Total** | **100 pts** | |

---

## 👤 Author

**Lakshya Pandey**  
B.Tech CSE (AI & ML) — Dayananda Sagar University, Bengaluru  
AI Research Contributor — MIT CSAIL Kellis Lab  
GitHub: [@pandeylakshya207-max](https://github.com/pandeylakshya207-max)

---

*Built for Frontend Battle 3.0 · Web and Design Society · IIT Bhubaneswar · 2026*
