# Prismatic Strategy — design brief for Claude Design

## What I want from you
Two things, working from the assets and system below:

1. **Website visual design** — design the pages of prismaticstrategy.com (a rebuild of my consulting site) using the finished logo, the mesh graphic system, and the palette. I want real design work: an editorial, intelligent, calm, distinctive look for a senior behavioural-strategy consultancy. Not corporate-generic, not startup-loud.
2. **A brand / identity system** — a reusable set of rules so it all stays consistent: logo usage, palette, type, and how the mesh graphics are applied across the site (and later, decks and social).

Please propose 2–3 visual directions in words first, then design the one that best fits *"editorial, intelligent, prismatic."*

---

## Who this is for
**Prismatic Strategy** is the consultancy of **Elina Halonen**, a behavioural strategist (15+ yrs) in Amsterdam. She helps organisations untangle complex, human-centred challenges and turn insight into action.

- **Positioning line:** *Solving complex problems starts with understanding human behaviour.*
- **Magpie metaphor:** curious, observant, collects patterns and notices what others overlook — bringing together behavioural science, psychology, systems design and beyond.
- **Tone:** confident, calm, intelligent, a little distinctive.

## The site (context for the design)
A **static, hand-coded** multi-page site (plain HTML/CSS/JS, no framework, GitHub Pages). So designs need to translate to clean, hand-editable code — nothing that needs a build step or heavy libraries. Mobile-first, accessible, strong light-mode contrast; dark mode is a nice-to-have.

Pages (shared nav + footer): **Home · About · Services · Approach · Writing · Contact.**
- **Home** — hero with the positioning line, short intro, signposts.
- **About** — bio + magpie/prismatic story.
- **Services** — six areas (behavioural drivers; barriers; reframing; strategy/policy design; behavioural input to research; capability/training).
- **Approach** — the three-pillar model **Diagnose · Reframe · Design**.
- **Writing** — three newsletter/podcast properties.
- **Contact** — `mailto:` button, Amsterdam, business details, newsletter note.

---

## Finished asset: the logo
A **prism mark** is done — do not redesign it, design *around* it. It's three nested, evenly-rotated triangles (a "pinwheel prism") that reads as a faceted prism. It works from a 16px favicon up to a hero mark.

- **Master:** `logos/prism-logo.svg` (uses `currentColor`, so it takes whatever colour the page sets — use this on the site).
- **Slide/flat variants:** `prism-navy`, `prism-white`, `prism-paper`, `prism-gold`, plus gradient versions `prism-grad-brand`, `prism-grad-warm`, and `prism-grad-spectrum` (+ a paper-background spectrum). SVG + 1024px PNG of each.
- **Favicon set:** simplified 2-triangle version for small sizes — theme-aware `favicon.svg`, `favicon.ico`, PNGs, and navy-tile app icons.
- **Lockup:** mark + wordmark *"Prismatic Strategy"* (Prismatic bold, Strategy lighter). Please formalise clear-space, min sizes, and lockup spacing as part of the identity system.

---

## The mesh graphic system (the main visual language)
A family of generative **line-mesh SVGs** (transparent background, recolourable). These are the signature motif — "light through a prism." Use them with restraint and intention; never coat everything in saturated colour.

**Families and their intended roles:**
- **Rose meshes** — small, **monochrome** focal devices (one colour each, *no gradients through them*). Ideal for the **Diagnose / Reframe / Design** trio: e.g. Diagnose = olive, Reframe = gold, Design = coral. Also section markers / small topic devices. Primary file `rose-mesh-02`.
- **Wavy fabric** — connective material / horizontal banners. Meant to carry a **restrained colour progression** as an alpha-mask over a gradient, so colour appears to travel *through* the material (e.g. `navy → olive → gold → coral → navy`), with long calm passages between transitions. Preferred file `wavy-fabric-04`.
- **Deformed grid** — an **environmental field** behind short content / at section transitions / cropped edges (never behind long text). Keep it quiet; let colour appear only in a limited region or seam. File `deformed-grid-mesh-01`.
- **Extra families** (for exploration): `nested-polygons`, `polar-mesh`, `spiral-mesh`. *(The logo was derived from `spiral-mesh-12`.)*

**Implementation notes:**
- Use the **raw SVGs**; recolour via CSS variables (`--stroke-color`, `--fill-color`), SVG gradients, or as an alpha mask over a CSS gradient. Preserve `viewBox` and transparency.
- Keep a **consistent apparent line weight** across families; thicken the supplied hairlines where they're too faint at real size.
- Motion (if any): only very slow gradient shifts, subtle entry reveals, or scroll-linked movement. Respect `prefers-reduced-motion`. Don't animate individual lines.

---

## Palette (working placeholders — please refine)
Not yet finalised. These are the values everything is currently built on; you're invited to propose a more sophisticated version (the deep-navy base + prismatic accent is the intent).

| Role | Hex |
|---|---|
| Navy (site base / ink) | `#0b2138` |
| Warm paper (light bg) | `#f4efe6` |
| Gold | `#c8a24a` |
| Coral | `#e0785d` |
| Olive | `#6f7a3f` |

Use the spectrum (navy→olive→gold→coral) as **one tasteful signature gradient**, sparingly — a thin prismatic rule, a hero accent, hover states. Never a full rainbow.

## Typography
Serif display + clean sans: **Spectral** (headings) + **Inter** (body), via Google Fonts. Generous line-height, ~65–75 character measure. Propose a stronger pairing if you have one.

---

## Assets & where they live
GitHub repo: **github.com/elinahalonen/prismaticstrategy**
- `logos/` — the prism mark, all colour/gradient variants (SVG + `png/`), and `favicon/`.
- `upload/` — the 65 raw mesh SVGs (rose, wavy, grid, nested-polygons, polar, spiral).
- `gallery.html`, `preview.html` — reference viewers showing the meshes recoloured and in their roles.

## Constraints & notes
- Design must translate to **plain hand-coded HTML/CSS/JS** (no build step).
- **Licensing:** the mesh SVGs came from a generative tool ("Book of Shapes") and their commercial-use terms aren't yet confirmed. Treat them as exploration; if usage is unclear, a sufficiently distinct, simplified re-implementation of the chosen motif is fine. The **logo is bespoke** and cleared.
- Deliverables I'd love: the visual directions, designed page layouts (at least Home + one inner page + mobile), and the identity-system rules (logo usage, palette, type scale, mesh-usage do's/don'ts).
