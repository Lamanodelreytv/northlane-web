# Northlane Digital Co. — Website

Single-file static website for Northlane Digital Co., a boutique digital advisory offering single-session services.

## Stack

- Pure HTML/CSS/JavaScript — no build step, no framework
- Single `index.html` file contains all pages, routing, translations (EN/ES), and logic
- Stripe integration pre-wired (placeholder keys, ready to swap)
- ~216 KB, gzipped ~50 KB

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire website |
| `robots.txt` | Search engine crawl rules |
| `sitemap.xml` | Sitemap for Google Search Console |

## Pages

**Public nav:** Home · Services · Pricing · About · FAQ · Contact

**Secondary (footer):** Process · Work · Payments · Refunds · Terms · Privacy · Legal

## Deploy

### Option 1 — Netlify Drop (fastest)
1. Go to https://app.netlify.com/drop
2. Drag the whole folder (or just `index.html`)
3. Instant public URL

### Option 2 — Cloudflare Pages / Vercel / GitHub Pages
Drop the files in a repo and connect to any static host.

## Before going live

1. **Update entity data** — search for `[XX-XXXXXXX]`, `[Full fiscal address]`, `[Registered Agent]` in `index.html` and replace with real LLC data.
2. **Stripe integration** — search for `pk_live_YOUR_KEY` and `data-stripe-price-id` attributes. See the comment block in the `<script>` tag for the 5-step activation guide.
3. **Contact form** — currently dummy (simulates success). Wire it to Formspree, Resend, or a custom webhook.
4. **Newsletter form** — same as contact form, dummy. Connect to ConvertKit, Buttondown, etc.
5. **Legal review** — Privacy, Terms, Refund pages are templates. Have qualified counsel review them for your jurisdiction (GDPR if EU clients, CCPA if California, etc.).
6. **OG image** — create a 1200x630 PNG at `/og-image.png` (currently referenced but not present).
7. **Domain** — update `https://northlane.co` references throughout `index.html`, `robots.txt`, and `sitemap.xml` if using a different domain.

## Features

- Fully bilingual (EN/ES) with auto-detection from browser language
- Cookie banner with consent persistence (localStorage)
- Accessible: skip-to-content, focus states, prefers-reduced-motion support, ARIA labels
- SEO-ready: Open Graph, Twitter Cards, Schema.org ProfessionalService JSON-LD, canonical URL
- Stripe-ready checkout modal with success state
- Animated counters on stats (IntersectionObserver)
- Scroll progress bar
- Responsive down to 375px

## License

All rights reserved. Northlane Digital Co., LLC.
