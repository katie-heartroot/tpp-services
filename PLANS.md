# TT&P Services Marketing Site — Project Plan

## Vision
Single-page marketing site for Telecom Tower & Power Services (TT&P) — nationwide emergency power backup installation, maintenance, and emergency response for the telecom sector. Goal: **instant credibility, lead capture, search visibility.**

---

## Completed ✓
- [x] **Core HTML scaffold** — 11 sections: hero, impact, power services (6 cards), emergency, process (4 steps), FCC compliance, about, contact, footer
- [x] **OG tags + favicon + Schema.org** — Full OpenGraph (LinkedIn/Facebook/Twitter), JSON-LD Organization, favicon  
- [x] **Mobile hamburger nav** — .responsive, animated 3-bar → X, closes on link click, accessible
- [x] **Git init** — repo established, `.gitignore` excludes .psd/.zip

---

## In Progress 🔨

### Gallery Section ([DOING NOW](01-gallery))
**What:** 5-image gallery of real job site work — organized cable runs, DC power plants, professional installations. Builds instant credibility.

**Where:** New section between **About → Contact**, before footer. Uses existing `ttp-work/` images:
- IMG_0683.jpeg.jpg (5712×4284)
- IMG_3592.JPG (3264×2448)
- IMG_3593.JPG (3264×2448)
- IMG_3597.JPG (3264×2448)
- IMG_6844.jpeg.jpg (4032×3024)

**How:**
- 2×2 grid on desktop, fallback to 1-col on mobile
- Each image has a **caption label** (e.g., "DC Power Plant Installation — 48V Rectifier System")
- Optional: lightbox modal on click (vanilla JS, no deps)
- Lazy-load images for performance

**Implementation:**
1. HTML: `<section id="gallery">` with grid + captions
2. CSS: Responsive grid, image styling, lazy-load ([loading="lazy"](loading="lazy"))
3. JS: Optional lightbox modal (click image → full-screen overlay)
4. Git commit: `feat: gallery section with real work photography`

---

## Backlog (Not Started) 📋

### 02 — Contact Form Backend
**What:** Replace `mailto:` with real backend (Formspree or custom endpoint).

**Why:** Current form action="mailto:" doesn't work reliably. Need actual email delivery + confirmation.

**Options:**
- Formspree: Free tier (50/mo) — easiest, zero backend
- Custom Node/Python endpoint on Fly.io or similar
- AWS SES + Lambda

**Decision:** TBD pending budget/preference

### 03 — Testimonials Block
**What:** 3–4 short testimonials from carrier/tower company clients.

**Why:** Social proof — "XYZ Carrier: 'TT&P completed our 200-site DC plant upgrade in 6 weeks.'"

**Format:** Card grid, client name/title/company, 1–2 sentence quote

**Status:** Awaiting client quotes from TT&P

### 04 — Client Logos
**What:** 6–8 carrier/tower company logos (Verizon, AT&T, tower operators, etc.)

**Why:** Credibility signal

**Format:** Light gray logos on white bg, grouped section

**Status:** Awaiting logo assets from TT&P

### 05 — Real Address + Hours in Footer
**What:** Street address, business hours, service coverage map

**Why:** Local SEO, trust signal

**Format:** Footer address block + optional embedded Google Map

**Status:** Awaiting details from TT&P

### 06 — Search Optimization
**What:** Blog post / FAQ section, improved headings/metadata for SEO keywords ("FCC backup power", "telecom battery systems", "emergency generator service")

**Why:** Organic search visibility

**Format:** Optional `/blog/` or `/faq/` pages, or expand FAQ into existing sections

**Status:** TBD

### 07 — Deployment
**What:** Deploy to ttpservices.com or similar domain

**How:** GitHub Pages (static) or Netlify/Vercel (with form handling)

**Status:** Awaiting domain + hosting decision

---

## Tech Stack
- **Frontend:** Vanilla HTML/CSS/JS — no build tooling, zero dependencies
- **Hosting:** Static (GitHub Pages, Netlify) — costs ~$0
- **Forms:** TBD (Formspree, custom backend, or hidden for now)
- **Icons:** Inline SVG (no icon library)
- **Fonts:** Google Fonts (Inter, Barlow Condensed) via CDN

---

## Design Tokens
```css
--blue:      #1558B0;
--cyan:      #00AADC;  /* accent */
--navy:      #050D1A;  /* dark bg hero */
--surface:   #F4F7FB;  /* light bg */
--text:      #1A2642;
```

---

## Next Steps
1. ✅ Gallery section implementation (01) **[NOW]**
2. Contact form routing (02)
3. Client approval on testimonials / logos
4. Real footer details (address, hours)
5. Deploy to domain

---

**Last Updated:** March 21, 2026  
**Owner:** TT&P Services  
**Status:** Active Development
