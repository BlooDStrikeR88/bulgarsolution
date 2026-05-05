# CLAUDE.md — Bulgar Solution Project Guide
> Read this file at the start of every session. Do NOT rescan the full project.

---

## 🌐 Live Site
**GitHub Pages:** https://bloodstriker88.github.io/bulgarsolution/index.html  
**Repo:** https://github.com/bloodstriker88/bulgarsolution  
**Branch:** main  
**Language:** Bulgarian (BG), with English version stub (`/en/`)

---

## ✅ ACTIVE PAGES (touch these)
These are the real, live, customized pages:

| File | Purpose |
|------|---------|
| `index.html` | Homepage — hero slider, services, portfolio, blog preview, testimonials |
| `about-bs.html` | About us page |
| `services-2-bs.html` | Services page |
| `contact-5-recaptcha-bs.html` | Contact page with reCAPTCHA |
| `rs-demo-particles-effects.html` | Design/showcase page (linked as "Дизайн" in nav) |
| `blog.html` | Blog listing page |
| `blog-single.html` | Single blog post template |
| `faqs.html` | FAQ page |
| `portfolio-single.html` | Single portfolio item template |

---

## 🧭 Navigation Structure
```
Начало        → index.html
За Нас        → about-bs.html
Услуги        → services-2-bs.html
Портфолио     → index.html#proektite-homepage
Дизайн        → rs-demo-particles-effects.html
Контакт       → contact-5-recaptcha-bs.html
EN flag       → /en/ (stub, not fully built)
```

---

## 📁 ACTIVE ASSET FOLDERS (used by live pages)

### CSS
- `css/` — main stylesheet folder
- `dist/` — compiled/minified CSS (likely from SASS)

### JS
- `dist/` — compiled JS

### SASS
- `sass/` — source SASS files (compile to dist/)

### Images (active)
- `images/bs/` — logo, team, portfolio thumbnails, partner logos, frontpage UI images
- `images/bs/logos-partners/` — client/partner logos
- `images/bs/frontpage/` — imac.webp, ipad3.webp, fbrowser.webp, fmobile.webp, fbrowser2.png
- `images/slider/rev/main/` — Revolution Slider images (s2-bg.jpg, s2-1.png … s2-8.png, s3.jpg)
- `images/parallax/` — parallax section backgrounds (7.jpg used on homepage)
- `images/testimonials/` — client testimonial photos (1.jpg, 3.jpg, 7.jpg, 8.jpg)
- `images/magazine/thumb/` — blog thumbnail images (11.webp, 14.webp)
- `images/services/` — chrome.webp, fbrowser2.png
- `images/videos/` — explore-poster.webp, explore-new-old.mp4
- `images/bs/resized/` — resized portfolio thumbnails

### Includes
- `include/` — likely PHP/HTML partials (header, footer, nav)

---

## ⚠️ DO NOT TOUCH — Template Leftovers
These exist in the folder but are **not linked from the live site**:

- `preview/` folder — template demo previews, ignore entirely
- `demos/` folder — template demo pages, ignore entirely
- `rs-demo-premium-holiday.html` — unused template demo
- `rs-demo-streams-*.php` — unused social stream demos (Facebook, Flickr, Instagram, Twitter)
- Any HTML files not listed in the ACTIVE PAGES table above

---

## 🔧 Template Info
- **Base template:** Canvas by SemiColonWeb (premium HTML template)
- **Slider:** Revolution Slider (RevSlider) — complex, has its own JS/CSS
- **CSS framework:** Bootstrap-based (custom Canvas build)
- **Key JS plugins used on homepage:** RevSlider, parallax, counter animations, GDPR cookie consent, testimonial carousel
- **GDPR cookie popup:** Custom implementation at top of pages — controls YouTube, Google Ads, Facebook/Instagram

---

## ⚡ Conflict Warnings for New Pages

1. **RevSlider** — only include its CSS/JS if the page uses a slider. Adding it unnecessarily slows the page.
2. **Bootstrap grid** — use existing column classes (`col-md-4` etc.), don't add a second Bootstrap version.
3. **SASS → dist** — if you edit raw CSS in `css/` directly AND in `sass/`, they will conflict. Pick one workflow.
4. **`include/` partials** — if header/footer are in `include/`, new pages must reference them the same way or they'll break nav/footer consistency.
5. **Image paths** — always use relative paths (`images/bs/...`), not absolute, since the site is hosted on GitHub Pages under a subfolder (`/bulgarsolution/`).
6. **`/en/` folder** — English version is a stub. Don't assume files there are complete mirrors of BG pages.

---

## 🚀 Git Workflow
```bash
# Check status
git status

# Stage all changes
git add .

# Commit
git commit -m "describe what changed"

# Push to GitHub (auto-deploys to GitHub Pages)
git push origin main
```

---

## 📌 Session Rules
- Always read this file first — do NOT scan the full project
- Only modify files listed under ACTIVE PAGES or their direct assets
- When building a new page: copy the structure of `services-2-bs.html` or `about-bs.html` as the safest base
- Ask Plamen before touching anything in `preview/`, `demos/`, or any rs-demo-* files
