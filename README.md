# Prismatic Strategy — mesh SVG system

Generated mesh/pattern SVGs for the Prismatic Strategy website, plus preview pages.

## `upload/` — 65 SVGs
Six families. Numbers match the original Book of Shapes downloads.

- **rose-mesh** (8) — kept **grey / single-colour** (brief: roses are monochrome, no gradient). `rose-mesh-02` is the kept primary. `rose-mesh-0903-00` is a newer-date rose.
- **deformed-grid-mesh** (5), **wavy-fabric** (6), **nested-polygons** (12), **polar-mesh** (16), **spiral-mesh** (18) — **radial gradient baked in**.

### Gradient treatment (non-rose files)
Each non-rose SVG now paints a full-viewBox `<rect>` filled with a radial gradient,
masked by the original mesh strokes — so one coherent radial runs from the centre out:

`navy (#16233e) → olive (#6f7a3f) → gold (#c8a24a) → coral (#e0785d) → navy`

Colours are **placeholder hex** — to rebrand, change the stops (search `stop-color`)
or re-run the bake from the grey originals. Transparent background and `viewBox` preserved.
Grey originals remain in `extracted/` locally (not committed).

## `preview.html` — role-based colour preview
Rose trio (Diagnose/olive · Reframe/gold · Design/coral), wavy banner, grid field,
and an "additional families" explorer. Toggle warm-paper / navy backgrounds.

## `gallery.html` — plain grid
All 65 SVGs by family, with a background switcher (defaults to mid-grey so both the
grey roses and the navy-heavy gradients read well).

> Note: CSS masks / gradients only render when served over http (local server or
> GitHub Pages), not from a `file://` path.
