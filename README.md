# Lumora — Independent Design & Engineering Studio

A single-page, light-palette landing site for a fictional design & engineering studio.
Built as a **single self-contained `index.html`** — no build step, no framework, no bundler.
Pure HTML, CSS, and vanilla JavaScript, with one CDN dependency for smooth scrolling.

🔗 **Live demo:** [lumora-three-alpha.vercel.app](https://lumora-three-alpha.vercel.app)

---

## ✨ Highlights

- **Full-screen intro loader** — animated `000 → 100` counter that slides away to reveal the page.
- **Liquid cursor reveal** — moving the pointer over the hero paints a soft brush trail of a second
  image over the first, rendered on a `<canvas>` with a custom rAF brush engine.
- **Scroll-driven motion** — line/word text reveals, entrance springs, and count-up statistics,
  all triggered via `IntersectionObserver` and scroll progress.
- **Smooth scrolling** powered by [Lenis](https://github.com/darkroomengineering/lenis).
- **rem-based adaptive grid** — the root font-size scales with the viewport so the layout stays
  proportional from mobile up to ultra-wide displays.
- **Fully interactive** — full-screen nav overlay, request modal with stubbed submit + success
  state, live local clock, and a hero card carousel.
- **Accessible & reduced-motion aware** — skip link, focus styles, `aria` attributes, and a
  `prefers-reduced-motion` fallback that disables animation.

## 🛠 Tech Stack

| Layer | Choice |
|-------|--------|
| Markup & styling | Hand-written HTML + CSS (custom properties, no framework) |
| Interactivity | Vanilla JavaScript (ES modules) |
| Smooth scroll | [Lenis](https://github.com/darkroomengineering/lenis) via CDN importmap |
| Typeface | [Onest](https://fonts.google.com/specimen/Onest) (Google Fonts) |
| Hosting | [Vercel](https://vercel.com) |

No build tooling required — the entire site is one HTML file.

## 🚀 Running locally

Because the site uses ES modules with an importmap, it must be served over **HTTP**
(opening the file directly via `file://` will block module loading). Any static server works:

```bash
# Option 1 — Node
npx serve .

# Option 2 — Python
python -m http.server 5173
```

Then open the printed `http://localhost:...` URL.

## 📦 Deployment

Deployed as a static site on Vercel:

```bash
vercel --prod
```

Vercel auto-detects the single `index.html` as a static deployment — no configuration needed.

## 📁 Structure

```
lumora/
├── index.html    # The entire site — markup, styles, and scripts
└── README.md
```

## 📄 License

Released under the MIT License. Demo imagery is used for portfolio purposes only.

---

<p align="center">Designed & built with care.</p>
