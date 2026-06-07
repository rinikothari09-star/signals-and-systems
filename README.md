# Signals &amp; Systems

Marketing website for **Signals &amp; Systems**, a fractional operations practice helping
founders and leadership teams turn complexity into clarity.

Built as a single static HTML page — no build step, no framework, no dependencies to install.

## Structure

```
site/
├── index.html            # the whole page (nav, hero, case studies, about, contact…)
├── styles.css            # page styles
├── colors_and_type.css   # design tokens — colors, type, spacing (Signals design system)
├── image-slot.js         # drag-and-drop headshot placeholder web component
└── assets/
    ├── signals-mark.svg        # brand spark mark (dark surfaces use the -light variant)
    ├── signals-mark-light.svg
    └── illustration-orbital.svg
```

## Running locally

It's plain static files — just open `index.html` in a browser, or serve the folder:

```bash
# Python
python3 -m http.server 8000
# then visit http://localhost:8000

# or Node
npx serve .
```

## Deploying

Drop the contents of `site/` onto any static host:

- **GitHub Pages** — push this repo and enable Pages (serve from the folder containing `index.html`).
- **Netlify / Vercel / Cloudflare Pages** — point the project at this repo; no build command, publish directory = `site/`.

## Notes

- **Contact form** is an embedded [Tally](https://tally.so) form (`tally.so/r/RGjLgQ`).
  It loads from Tally's CDN and needs an internet connection. The auto-resize is handled by
  Tally's `embed.js`, loaded at the bottom of `index.html`.
- **Book-a-call buttons** link to Calendly (`calendly.com/rinikothari03/intro-call`).
- **Headshot** — the About section uses a drag-and-drop image slot. To ship a fixed photo
  instead, replace the `<image-slot>` element in `index.html` with a standard
  `<img src="assets/headshot.jpg" …>`.
- **Fonts** (Newsreader, Inter, JetBrains Mono) load from Google Fonts via `@import` in
  `colors_and_type.css`.

## Design system

Visual foundations (color, type, spacing, the cream + coral pairing) come from the
**Signals design system** and live in `colors_and_type.css` as CSS custom properties.
