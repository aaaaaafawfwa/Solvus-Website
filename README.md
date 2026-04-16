# Solvus site

Astro-based marketing site for Solvus, a web design agency for US realtors.

## Stack

- Astro 4.x (static site generator, minimal JS by default)
- No framework (no React, no Vue) — vanilla HTML/CSS/JS islands
- Fontsource for self-hosted fonts (Inter Variable, JetBrains Mono)
- Sitemap integration for SEO

## Local development

```bash
npm install
npm run dev
```

Opens at `http://localhost:4321`.

## Build

```bash
npm run build
npm run preview
```

Output goes to `./dist`. Static files, deployable anywhere.

## Deploying to Vercel

1. Push this repo to GitHub.
2. Import the repo at vercel.com/new.
3. Vercel auto-detects Astro. No config needed.
4. Set the production domain to `solvus.com` under Settings → Domains.

## Project structure

```
src/
  components/     Reusable .astro components
  layouts/        BaseLayout (meta, header, footer)
  pages/          Routes — each .astro file is a page
  styles/         global.css (design tokens, reset, utilities)
public/           Static assets served as-is (favicon, robots.txt)
astro.config.mjs  Astro config (site URL, integrations)
```

## Design tokens

All design values live in `src/styles/global.css` under the `:root` selector.
Change colours, type scale, spacing, or motion there — it propagates everywhere.

## What's done

- [x] Home page (/)
- [x] BaseLayout with meta tags, OG, structured data slot
- [x] SiteHeader with sticky scroll state + mobile menu
- [x] SiteFooter
- [x] Button, Eyebrow, FAQAccordion, CTABand components
- [x] HeroDemo — animated mini realtor site mockup
- [x] Design tokens + typography + motion system
- [x] Sitemap + robots.txt

## What's next

- [ ] /services
- [ ] /work (concept showcase overview)
- [ ] /work/[slug] dynamic concept detail pages
- [ ] /about
- [ ] /book (Cal.com embed)
- [ ] /contact (form + endpoint)
- [ ] /realtor-website-design (SEO landing)
- [ ] Real OG image (/public/og-default.png, 1200x630)
- [ ] Custom display font (currently using Inter only)
