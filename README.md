# Novara Studio

Static marketing site for **Novara Studio** — a one-person "Landing Page as a Service" studio. The site consists of a main landing page and three portfolio case studies, each showcasing a fictional product concept (Meter, Quill, Arbor).

## Viewing the site

Everything is static HTML — no build step or dependencies to install. Serve the repo root with any static file server so the iframe previews and JS runtime load correctly:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` directly via `file://` may block the iframe previews and runtime fetches in some browsers, so prefer a local server.

## Structure

| Path | Description |
|---|---|
| `index.html` | The main landing page. |
| `case-studies/` | Portfolio case study pages for Meter, Quill, and Arbor. See [case-studies/README.md](case-studies/README.md). |
| `concepts/` | The standalone concept landing pages, embedded as scaled iframe previews on the main page and linked from the case studies. See [concepts/README.md](concepts/README.md). |
| `assets/` | Shared JavaScript runtime, components, and the design token stylesheet. See [assets/README.md](assets/README.md). |
| `archive/` | Retired page variants kept for reference. See [archive/README.md](archive/README.md). |

## How the pages work

`index.html` and the case study pages wrap their content in an `<x-dc>` element that [assets/support.js](assets/support.js) parses and renders at load time (using React from the page context). Styling is inline per element, with hover states expressed through `style-hover` attributes handled by the runtime. The landing page pulls its portfolio thumbnails from `concepts/` via `<iframe>` elements scaled down with a CSS container-query transform.

## Design

- **Fonts:** Fraunces (display), Instrument Sans (body), Spline Sans Mono (labels), loaded from Google Fonts.
- **Tokens:** the canonical color/type/spacing token set lives in [assets/novara-tokens.css](assets/novara-tokens.css); the pages currently inline the resolved values.
- **Palette:** porcelain light background (`#F6F5F0`), ink text (`#12141F`), iris accent (`#5A62C9`).
