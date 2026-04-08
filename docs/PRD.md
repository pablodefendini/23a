# 23a — Marcha por la Justicia Reproductiva

## Problem

On April 23, 2026, a march for reproductive justice is happening in Río Piedras, Puerto Rico. The march needs a public-facing landing page that communicates what the movement is about, who it's for, and when/where to show up — in clear, accessible Spanish that doesn't sanitize the political stakes.

## Goals

- Communicate the date, time, and location of the march (April 23, 5PM, Edificio Darlington, Río Piedras)
- Frame reproductive justice broadly — not just abortion access, but labor rights, healthcare, obstetric violence, trans health, elder autonomy, family formation
- Speak directly to multiple constituencies (gestating people, trans folks, queer families, adolescents, men, elders, survivors, psychiatrized people) with specific, concrete language
- Be fast, accessible, and mobile-first — people will share this on WhatsApp and Instagram
- Look sharp: bold green/purple brand, custom typography (Gotham + Handelson Two), poster-style SVG lockup

## Non-goals

- No backend, no CMS, no forms, no analytics (at least for v1)
- No English version (this is a Puerto Rico march; the audience reads Spanish)
- No event registration or RSVP — just show up
- No social media embeds or third-party scripts

## Key constraints

- **Static site only** — single HTML file, one CSS file, fonts, and an SVG. No build step, no JS.
- **Custom fonts**: Gotham Bold (sans) and Handelson Two (script). Both loaded locally via @font-face with woff2 + otf fallbacks. These are licensed fonts — do not redistribute outside this project.
- **Brand colors**: verde `#288E2D`, púrpura `#3E074F`
- **Content is in Spanish** with gender-inclusive language (todes, hijes, elles)
- **The SVG lockup** (`23a justicia reproductiva.svg`) is the hero graphic and contains the key event details as vector text

## Open questions

- [ ] Where will this be hosted? (GitHub Pages? Netlify? A custom domain?)
- [ ] Will there be a second phase with social sharing cards, OG images, or print assets?
- [ ] Should the page include links to organizing groups or a contact method?
