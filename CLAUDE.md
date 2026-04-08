# 23a — Marcha por la Justicia Reproductiva

Landing page for the April 23, 2026 march for reproductive justice in Río Piedras, Puerto Rico. Static site — no JS, no build step, no backend.

## Tech stack

- HTML5 + CSS3, single page
- Custom fonts: Gotham Bold (sans), Handelson Two (script) — loaded locally via @font-face
- SVG hero lockup with event details baked in as vector text
- No JavaScript. No frameworks. No build tools.

## Directory structure

```
23a/
├── index.html                          # The page
├── marcha-justicia-reproductiva.css    # All styles
├── 23a justicia reproductiva.svg       # Hero/CTA lockup
├── 23a justicia reproductiva.png       # Raster fallback
├── fonts/
│   ├── gotham-bold.woff2
│   ├── Gotham-Bold.otf
│   ├── handelson-two.woff2
│   └── handelson-two.otf
├── docs/
│   ├── PRD.md
│   ├── MEMORY.md
│   └── DIARY.md
├── CLAUDE.md                           # You are here
├── .gitignore
└── README.md
```

## Brand

- **Verde**: `#288E2D` (primary, hero backgrounds, CTAs)
- **Púrpura**: `#3E074F` (secondary, text accents, alternating story bands)
- **Fonts**: `--font-sans: 'Gotham'` for headings/body, `--font-script: 'Handelson Two'` for accents
- Script accents use the `.script-accent` class — always green, always Handelson Two

## Hard constraints

- **All content in Spanish.** Gender-inclusive language throughout (todes, hijes, elles).
- **No JavaScript.** The page must work with JS disabled. CSS handles all interactivity (hover states, scroll behavior, animations via @keyframes).
- **Licensed fonts.** Gotham and Handelson Two are commercial typefaces. Do not redistribute. The CSS falls back to Montserrat → Helvetica Neue → Arial for sans, and generic cursive for script.
- **The SVG lockup is the source of truth** for event details (date, time, location). If event details change, the SVG needs to be regenerated — they're not editable in HTML.

## Things to avoid

- Don't add JavaScript. Seriously.
- Don't reorganize the CSS — it's structured by page section (Hero → Context → Qué Es → Quiénes → CTA → Footer) and that mapping is intentional.
- Don't change font paths without updating both woff2 and otf references.
- Don't use masculine generics in Spanish content.

## Patterns

- Alternating story bands in the "Quiénes" section use `.story--green` / `.story--purple` classes
- Design tokens are all in `:root` — use CSS custom properties, not hardcoded values
- The `.container` class caps content at 1100px with auto margins
- Print styles exist — the page is designed to be printable

## Development diary

See `docs/DIARY.md`. Update every session or after any substantial change. Write in Pablo's voice (first-person, direct, concrete — see the `pablo-voice` skill).
