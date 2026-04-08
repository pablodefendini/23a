# 23a — Decision Log

## 2026-04-08: Initial project scaffold

### Static site, no build step
**Chose:** Single HTML file + single CSS file, no bundler, no JS.
**Alternative:** Could have used a static site generator (Astro, 11ty) or even a React SPA.
**Why:** This is a single-page site for a specific event. Adding a build step would be overhead for zero benefit. The page needs to load fast on mobile over Puerto Rico's sometimes-spotty connections. A raw HTML/CSS file served from a CDN is as fast as it gets. Also means anyone can edit it — no toolchain knowledge required.

### Fonts in a subdirectory
**Chose:** `fonts/` subdirectory with woff2 + otf for each typeface.
**Alternative:** Fonts flat at root alongside HTML/CSS (how they were originally on the Desktop).
**Why:** Four font files cluttering the root alongside the HTML and CSS made the project harder to scan. The `fonts/` directory is a minor organizational win. Updated `@font-face` paths in CSS accordingly.

### SVG lockup as hero graphic
**Chose:** Event details (date, time, location) baked into an SVG as vector text.
**Alternative:** Event details as live HTML text overlaid on a background.
**Why:** The lockup is a designed poster composition — the typography, layout, and visual weight are all intentional. Making those editable HTML elements would mean reimplementing the design in CSS, which would be fragile and wouldn't look as good. Trade-off: if the event details change, the SVG needs to be regenerated.

### Gender-inclusive Spanish throughout
**Chose:** Consistent use of -e endings (todes, hijes, elles) and inclusive framing.
**Why:** The march is explicitly about reproductive justice for all people — using masculine generics would contradict the message. This is a political choice that matches the political content.

### No JavaScript at all
**Chose:** Zero JS. CSS-only animations, no analytics, no interactivity beyond CSS hover/scroll.
**Alternative:** Could add scroll-triggered animations, analytics, social share buttons.
**Why:** The page doesn't need any of it. Every script is a potential breakage point, a performance cost, and a privacy concern. The CSS handles fade-in animation and hover states. Analytics can come later if needed (and should be privacy-respecting when they do).

## Decisions still pending

- **Hosting**: GitHub Pages? Netlify? Custom domain? Needs to be decided before launch.
- **Social sharing assets**: OG image, Twitter card — probably needed before the page starts circulating on social media.
- **Organizing group links / contact info**: The page currently has no way for people to connect with organizers. Might need a section or at least a footer link.
