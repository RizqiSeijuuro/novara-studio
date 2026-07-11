# case-studies/

Portfolio case study pages, linked from the "Selected Work" section of the main landing page ([../index.html](../index.html)). Each page walks through one fictional product concept — the brief, approach, and outcome — and embeds the finished concept page from [../concepts/](../concepts/) as a scaled iframe preview.

## Files

| File | Description |
|---|---|
| `meter.html` | **Meter** — usage-analytics SaaS concept. Dashboard-first hero with a live product demo above the fold. |
| `quill.html` | **Quill** — AI writing-editor concept. |
| `arbor.html` | **Arbor** — smart-planter hardware concept. |

## Notes

- These pages are `<x-dc>` documents rendered by [../assets/support.js](../assets/support.js); they are not plain static HTML and need the runtime to display.
- Each page links to the next case study in the cycle (meter → quill → arbor → meter) and back to the landing page, so renaming a file here requires updating its siblings and `index.html`.
