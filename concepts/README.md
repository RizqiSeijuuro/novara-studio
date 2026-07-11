# concepts/

Standalone concept landing pages — the actual "work" shown in the portfolio. The main page ([../index.html](../index.html)) embeds them as iframe thumbnails at a fixed 1280×720 viewport, scaled to fit their card via a container-query transform, and the case studies in [../case-studies/](../case-studies/) embed and link to them full-size.

## Files

| File | Description |
|---|---|
| `meter.html` | **Meter — Usage analytics for modern billing.** SaaS concept page. |
| `quill.html` | **Quill — The editor that edits with you.** AI writing-product concept page. |
| `arbor.html` | **Arbor — The planter that speaks plant.** Smart-planter hardware concept page. |

## Notes

- Each page is a complete, self-contained HTML document — open any of them directly in a browser, no runtime or build step required.
- Renaming files here breaks the iframe embeds on the main page and the links in the case studies.
