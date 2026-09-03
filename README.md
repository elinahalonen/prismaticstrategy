# prismaticstrategy.com

Static, hand-coded site for Prismatic Strategy (Elina Halonen). Plain HTML/CSS/JS,
no build step — served from this repo's root via GitHub Pages at the custom domain
`prismaticstrategy.com`.

## Structure
- `index.html` — the site (one page, in-page nav).
- `styles.css` — entry point; `@import`s the token + component CSS.
- `tokens/` — design tokens: `colors`, `typography`, `space`, `motion`, `base`, `mesh`, `fonts`.
- `components/` — `site/` (layout) and `prose/` (long-form text).
- `assets/brand/` — portrait (`elina.webp` + `.png` fallback), `favicon.svg`/`.ico`,
  `apple-touch-icon.png`, and `prism-mark.svg` (the logo mark used in the header/footer).
- `assets/mesh/` — the themed mesh-graphic SVGs (optimised with SVGO).

## Editing
Edit the HTML/CSS directly — no tooling required. Fonts load from Google Fonts.

## Deploy (GitHub Pages)
1. Settings → Pages → deploy from `main`, root.
2. The `CNAME` file points at `prismaticstrategy.com`; set the DNS for that domain to
   GitHub Pages so the site resolves there. (The site uses absolute paths like
   `/styles.css`, so it is intended to serve from a domain root, not a project subpath.)

## `design-workshop/`
Logo exploration and brand assets built during design (mesh gallery/preview, the prism
logo studies, all colour/gradient logo variants and PNG/favicon exports, and the design
brief). Not part of the live site — kept for reference.
