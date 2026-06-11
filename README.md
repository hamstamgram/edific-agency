# Edific — The Dental Intake Engine (edific.uk)

Single-page marketing site for the **Dental Intake Engine** — a premium vertical AI product for dental practices. Positioned as a product, not an agency: *"Not AI receptionists. AI for dentistry."*

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire site — markup, CSS, JS, and JSON-LD schemas inline. No build step. |
| `plan.md` | The design plan this build follows (design system, sections, motion, SEO). |
| `llms.txt` | AI-engine digest of the offer (AEO). Deploy at `/llms.txt`. |
| `robots.txt` | Allow-all crawl policy + sitemap pointer. Deploy at `/robots.txt`. |

## Design provenance

- **Structure & copy patterns**: CaseFlood / Hormozi 10-pattern blueprint (`../HORMOZI-PORTFOLIO-PATTERNS.md`) — one offer, one price (€997/mo), waitlist CTA, named case study, speed-led value prop, "most practices don't need more patients" twist.
- **Copy voice**: Vapi.ai — outcome-led, concrete numbers, short declaratives.
- **Hero treatment**: VectrFL.com — Three.js animated canvas under a gradient overlay.
- **Design system**: white `#ffffff`, Inter, text `#1e293b`, accent `#1e63d2`, pill buttons (radius 100px), cards `#f8fafc`/`#e2e8f0`, 1200px container, 128px section padding.

## Tech

- Pure HTML/CSS/JS — no frameworks, no build step.
- **Three.js 0.182.0** via CDN importmap: 400 particles on a jittered torus, slow rotation + mouse parallax. Renders only while the hero is on screen; static frame under `prefers-reduced-motion`; CSS gradient fallback when WebGL is unavailable (a looping video can be slotted into `.hero-fallback` later).
- **GSAP 3.13 + ScrollTrigger** via CDN: hero entrance sequence, fade-up reveals, card staggers, count-up metrics. All disabled under reduced motion; content is fully visible with JS off (`no-js` class).
- **SEO/AEO**: FAQPage, Product, HowTo, and LocalBusiness JSON-LD; OG + Twitter cards; canonical `https://edific.uk/`; semantic HTML5 with ARIA labels and a skip link.
- Authored payload ≈ 50 KB (libraries load from CDN). Lighthouse target: 90+.

## Develop

```bash
open index.html        # or any static server, e.g.:
python3 -m http.server 8000
```

Note: the Three.js importmap loads over HTTPS, so a local server (not `file://`) is needed in some browsers.

## Deploy

Copy `index.html`, `llms.txt`, and `robots.txt` to any static host (Cloudflare Pages, Netlify, Vercel, GitHub Pages) behind **edific.uk**.

Pre-launch checklist:

- [ ] Upload an OG image at `/og.png` (1200×630) — currently referenced but not created.
- [ ] Add `sitemap.xml` (single-URL sitemap for `/`).
- [ ] Wire the waitlist forms to the Supabase capture table (Phase 3 of `../BUILD-PLAN.md`). Until then, submissions open a prefilled `mailto:hello@edific.uk` — the handler is `handleWaitlist()` in `index.html`, marked with a `TODO`.
- [ ] Add analytics (Plausible or PostHog, per BUILD-PLAN).
- [ ] Replace the Praxis Dr. Weber metrics with the signed pilot's real numbers once available.
