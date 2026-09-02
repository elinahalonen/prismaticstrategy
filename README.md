# Prismatic Strategy — mesh SVG system

Generated mesh/pattern SVGs for the Prismatic Strategy website, plus preview pages.

## `upload/` — 24 raw (themeable) SVGs
Numbers match the original Book of Shapes downloads, so brief references line up:

- `deformed-grid-mesh-00..04`
- `rose-mesh-00..12`  (brief's primary rose = **rose-mesh-11**, sharper alt = **rose-mesh-02**)
- `wavy-fabric-00..05`  (brief's preferred wave = **wavy-fabric-04**)

Colours are driven by CSS variables (`--stroke-color`, `--fill-color`,
`--background-color`); transparent background and `viewBox` preserved.

## `preview.html` — role-based colour preview
Shows each family doing its brief job:
- **Rose** as monochrome focal device (Diagnose/olive · Reframe/gold · Design/coral), tested at real sizes.
- **Wavy** as a banner: SVG alpha-mask over a CSS gradient (`navy → olive → gold → coral → navy`).
- **Deformed grid** as an environmental field with colour confined to a seam.
- Toggle warm-paper / navy page backgrounds; recolour roses live.

Palette in `preview.html` is **placeholder hex** — swap the `:root` variables for the real brand values.

## `gallery.html` — plain grid
All 24 SVGs as thumbnails, grouped by design, with a background switcher.
