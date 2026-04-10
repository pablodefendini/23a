# Media Kit Page — Design Spec

## Overview

A second HTML page (`medios.html`) for downloading media kits, artwork, social media graphics, and press materials related to the Marcha por la Justicia Reproductiva. Linked from the landing page footer.

## Decisions

- **Layout:** Option B — grid with category headers. White background, no colored hero. Functional downloads-page feel.
- **CSS:** Shared stylesheet (`marcha-justicia-reproductiva.css`), new section appended at the end following existing comment-block pattern.
- **Navigation:** Footer link on `index.html` points to `medios.html`; footer on `medios.html` links back to `index.html`.
- **Content:** All placeholder — file cards with dummy names, formats, and download links (`href="#"`).
- **Language:** Spanish, gender-inclusive, consistent with the landing page.

## Page Structure

### 1. Page Header

White section with a purple top border (4px, matching the context section pattern). Contains:
- Title: "Materiales *y medios*" (script accent on "y medios")
- One-line description of the page's purpose

### 2. Category Sections

Four sections, each with an uppercase purple heading and a bottom-bordered separator:

**Logos y arte** (2-column grid)
- Lockup principal — SVG, vector
- Lockup principal — PNG, 2400×1200

**Material impreso** (2-column grid)
- Flyer 8.5×11 — PDF
- Póster 11×17 — PDF

**Redes sociales** (3-column grid on desktop, 1-column on mobile)
- Instagram Post — PNG, 1080×1080
- IG Story — PNG, 1080×1920
- Twitter/X Header — PNG, 1500×500

**Prensa** (2-column grid)
- Comunicado de prensa — PDF, 2 páginas
- Hoja informativa — PDF, 1 página

### 3. Download Cards

Each card contains:
- Preview area (colored placeholder block — green or purple)
- File name (bold)
- Format and size label (muted text)
- "Descargar" button (green background, white text, uppercase)

### 4. Footer

Same as landing page footer, with added cross-navigation links between `index.html` and `medios.html`.

## Files to Create

- `medios.html` — the media kit page

## Files to Modify

- `marcha-justicia-reproductiva.css` — append new section for media page styles
- `index.html` — add footer link to `medios.html`

## Constraints

- No JavaScript
- No build tools
- All content in Spanish with gender-inclusive language
- Uses existing CSS custom properties from `:root`
- Responsive: 2–3 column grids collapse to 1 column on mobile
- Print styles for the new page
