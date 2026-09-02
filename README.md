# Prismatic Strategy — SVG assets

Generated mesh/pattern SVGs for the Prismatic Strategy website.

## `upload/`
24 themeable ("raw") SVGs across three designs:

- `deformed-grid-mesh-01..05`
- `rose-mesh-01..13`
- `wavy-fabric-01..06`

Each is the **raw** version: colours are driven by CSS variables in an inline
`<style>` block (`--stroke-color`, `--fill-color`, `--background-color`,
`--occlusion-color`), so they can be recoloured/themed by overriding those
variables, or inherit `currentColor`.

## `gallery.html`
Open in a browser for a grid overview of all 24 SVGs, grouped by design and
filtered by a Design dropdown.
