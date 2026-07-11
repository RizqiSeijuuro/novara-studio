# assets/

Shared JavaScript and design tokens used by the site's pages.

## Files

| File | Description |
|---|---|
| `support.js` | Generated runtime (do not edit by hand) that parses and renders the `<x-dc>` documents used by `index.html` and the case study pages. Rebuilt from `dc-runtime/src/*.ts` with `bun run build`. |
| `image-slot.js` | `<image-slot>` web component — a user-fillable image placeholder, imported by `index.html` for the founder photo. Dropped-in images persist via a `.image-slots.state.json` sidecar written next to the page that uses the slot (gitignored). |
| `novara-tokens.css` | **Novara Studio design tokens v1** — dark-first CSS custom properties for color (ink/porcelain/iris scales), typography, spacing, radii, and shadows. Canonical source for the studio's palette; intended to be droppable into any project. Not currently linked by the pages, which inline the resolved values. |
