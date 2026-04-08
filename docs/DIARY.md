# 23a — Development Diary

A public log of the work behind the landing page for the Marcha por la Justicia Reproductiva on April 23, 2026 in Río Piedras, Puerto Rico. This is a record of decisions, pivots, and the thinking behind the build — partly for anyone who wants to follow along, partly for future-me when I inevitably forget why I did something three weeks from now.

---

## Entry 1 — April 8, 2026: Setting up the scaffold

The page itself already exists — I built it as a single HTML file on my Desktop with the CSS, fonts, and an SVG lockup. Today was about turning that into a proper project: getting it into a repo, organizing the files, and writing down the decisions before I forget them.

The site is deliberately simple. One HTML file, one CSS file, custom fonts (Gotham and Handelson Two), and an SVG poster lockup that carries the event details. No JavaScript. No build step. No frameworks. The march is on April 23rd — two weeks out — and the page needs to be shareable on WhatsApp and Instagram, which means it needs to load fast on mobile and look good when someone screenshots it.

I moved the fonts into a `fonts/` subdirectory because four font files sitting next to the HTML was making the root messy. Updated the `@font-face` paths in the CSS to match. Small thing, but it matters when you're scanning the project.

The content is all in Spanish with gender-inclusive language throughout — todes, hijes, elles. That's not a stylistic choice, it's a political one. You can't build a page about reproductive justice for all people and then default to masculine generics. The language has to match the politics.

The biggest design decision was baking the event details into the SVG lockup rather than making them editable HTML. The lockup is a designed composition — the typography and layout are intentional in ways that would be painful to replicate in CSS. Trade-off is that if the date or location changes, I need to regenerate the SVG. For a two-week-out event, that's a fine trade-off.

Still need to figure out hosting (leaning toward GitHub Pages or Netlify) and whether to add social sharing cards before the link starts circulating. Also need to decide if the page should include contact info for organizers or links to participating groups. For now, it's a clean call to action: here's what this is about, here's who it's for, here's when and where. Show up.
