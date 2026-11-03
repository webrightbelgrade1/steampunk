# Project memory

## Product intent & audience

- Single-page site (`index.html`) with a motto/closing section; likely personal or brand landing page emphasizing typographic hierarchy

## Brand personality & voice

- Warm, soft, refined; typographic elegance via serif fonts (Cormorant Garamond)

## Visual design & UX direction

- Serif-driven typography; display vs. body font distinction via CSS variables
- Fluid responsive type using `clamp()`
- `.motto blockquote`: `font-family:var(--f-body);font-weight:600;font-size:clamp(1.6rem,3.6vw,2.5rem);line-height:1.3`
- `.closing .m`: `font-family:var(--f-body);font-weight:600;font-size:1.45rem`
- Prefers exact value matching; avoid leftover properties (e.g., stale `line-height`) when updating rules

## Decisions, constraints & rationale

- User requires surgical CSS edits with no collateral changes
- Switching motto/closing from display serif to body serif for warmth
- Build verification step confirms changes are valid

## Open questions & assumptions

- Assuming `--f-body` resolves to Cormorant Garamond and `--f-display` is the prior display serif
- Full page structure, sections beyond motto/closing, and color/layout system not yet seen