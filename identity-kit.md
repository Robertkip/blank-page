# Identity Kit (Week 3) — foundation for the build week

This is the single source of truth for how the site looks. Keep every section I build consistent with it.

## Type
- Heading font: **Inter**, weight 600 — system fallback `ui-serif`.
- Body font: **Inter**, weight 400 — same family, fewer fonts, less to maintain.
- If Inter fails to load, the system-serif fallback still reads cleanly.

## Palette (hex)
| Role      | Hex     | Use          |
|-----------|---------|--------------|
| Text      | `#171717` | near-black, body & headings |
| Background| `#fafafa` | warm white page background |
| Accent    | `#0d9488` | teal — links, accents, CTA underline |
| Muted     | `#525252` | secondary text (subtle notes) |

## Logo / favicon
- `favicon.svg` — a single, flat initial ("K") mark. Tiny detail, feels finished.
- No animated gradients: the work must be the loudest thing on the page.

## Style note (the mood, one sentence)
Calm and confident: generous whitespace, a 24px grid, centered content, so the code and case studies read as the work — not the design.

## Contrast (checked)
- `#171717` on `#fafafa` — strong (7:1+). Readable in sunlit phone screens.
- Accent `#0d9488` — visible against `#fafaff`; safe for links.

## Placeholder for your real content
Where your actual identity kit goes (the one you generated with your own proof):
- Your real two fonts and their hex codes.
- Your real logo or favicon.
- Your real one-line claim (see content-map.md).

This file gets overwritten with your real kit; the CSS above already reads these values from `:root`.
