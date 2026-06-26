# NexusAI — Intelligent Data Automation Platform

> **Frontend Battle 3.0 · IIT Bhubaneswar · Round 1 Submission**  
> Built by Lakshya Pandey · 26 June 2026

---

## 🚀 Live Demo

🔗 **[nexusai.vercel.app](https://nexusai.vercel.app)** ← replace with your Vercel URL after deploy

---

## 📋 Overview

A premium, high-converting, responsive landing page for a next-generation AI-driven data automation platform. Built under a strict 4-hour countdown as part of Frontend Battle 3.0 — the flagship event of the Web and Design Society, IIT Bhubaneswar.

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
- [x] Desktop (>768px): Modern **Bento Grid** layout with hover active state
- [x] Mobile (≤768px): Touch-optimized **Accordion** list
- [x] **Context Lock**: active hover index on desktop transfers to accordion on window resize past breakpoint
- [x] Smooth panel open via `requestAnimationFrame` on layout transition
- [x] **Zero external libraries** — no Framer Motion, no Radix, no Headless UI
- [x] Pure CSS Transitions with hardware-accelerated transforms

### SEO & Semantic HTML
- [x] Full `<meta>` tags, Open Graph (OG), Twitter Card
- [x] Semantic structure: `<header>`, `<main>`, `<section>`, `<article>`, `<nav>`, `<footer>`
- [x] ARIA labels, roles, `aria-expanded`, `aria-live`, `aria-checked`
- [x] Crawlable text nodes, no content in pseudo-elements

### Performance
- [x] Loader exits at **380ms** (under 500ms TTI budget)
- [x] Micro-interactions: **150–200ms** ease-out
- [x] Layout reflows: **300–350ms** ease-in-out
- [x] Google Fonts via `preconnect` — no render blocking
- [x] Hardware-accelerated CSS transitions only (no runtime CSS-in-JS)
- [x] `prefers-reduced-motion` respected

---

## 🎨 Design System

| Token | Value |
|-------|-------|
| Arctic Powder | `#F1F6F4` |
| Mystic Mint | `#D9E8E2` |
| Forsythia | `#FFC801` |
| Deep Saffron | `#FF9932` |
| Nocturnal Expedition | `#114C5A` |
| Oceanic Noir | `#172B36` |
| Display Font | JetBrains Mono |
| Body Font | Inter |

---

## 🗂️ Project Structure

```
nexusai-frontend-battle/
├── index.html          # Entire app — single file, zero build step
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
├── x-mark.svg
└── README.md
```

---

## 🛠️ Running Locally

No build step. No npm install. No config.

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/nexusai-frontend-battle.git

# Enter the folder
cd nexusai-frontend-battle

# Open in browser — any of these work:
open index.html                        # macOS
start index.html                       # Windows
xdg-open index.html                    # Linux

# OR serve locally with VS Code Live Server (recommended)
# Install "Live Server" extension → right-click index.html → Open with Live Server
```

> **Recommended**: Use VS Code + Live Server extension for hot reload during development.

---

## 🔍 How to Test Each Feature

### Feature 1 — Pricing Engine
1. Open the **Pricing** section (scroll down or click nav)
2. Click **Annual** toggle → all prices update with 20% discount, "was ₹X/mo" note appears
3. Click **$ USD** → all symbols and values update to USD pricing
4. Click **€ EUR** → all symbols and values update to EUR pricing with tariff applied
5. Open **Chrome DevTools → Performance tab → Record** while toggling → verify zero layout shifts

### Feature 2 — Bento ↔ Accordion
1. On desktop (>768px): hover over any feature card → active glow state
2. **While hovering** card #3 (Workflow Orchestration): drag browser window width below 768px
3. Accordion appears with panel #3 **already open** — context transferred
4. On mobile: tap any accordion item → panel opens smoothly, others close

---

## 🚫 Libraries Deliberately Excluded

Per competition rules, the following are **not used**:

- ❌ Framer Motion
- ❌ Radix UI
- ❌ Shadcn/UI
- ❌ Headless UI
- ❌ Tailwind UI components
- ❌ Any runtime CSS-in-JS engine

All animations are native **CSS Transitions** and **Web Animations API (WAAPI)**.

---

## 📦 Tech Stack

| Layer | Choice | Reason |
|-------|--------|--------|
| Framework | Vanilla HTML/CSS/JS | Zero build overhead, fastest TTI |
| Styling | Custom CSS with variables | Full control, no runtime cost |
| Fonts | Google Fonts (preconnect) | JetBrains Mono + Inter |
| Deployment | Vercel | Zero-config static hosting |
| Animations | Native CSS Transitions | Hardware-accelerated, no deps |

---

## 📄 License

Built for Frontend Battle 3.0 · IIT Bhubaneswar · 2026
