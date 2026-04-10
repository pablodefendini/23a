# Media Kit Page Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a `medios.html` downloads page with placeholder media kit assets, styled with the shared CSS and linked from the landing page footer.

**Architecture:** Static HTML page sharing the existing CSS file. New CSS section appended at the end of `marcha-justicia-reproductiva.css`. Cross-navigation added to both footers.

**Tech Stack:** HTML5, CSS3, no JS, no build tools.

---

## File Map

| File | Action | Responsibility |
|------|--------|----------------|
| `medios.html` | Create | Media kit downloads page — all HTML structure and placeholder content |
| `marcha-justicia-reproductiva.css` | Modify (append) | New `MEDIOS` section with styles for page header, category sections, download cards, responsive grid, and print |
| `index.html` | Modify | Add footer link to `medios.html` |

---

### Task 1: Create `medios.html` with page header and first category section

**Files:**
- Create: `medios.html`

- [ ] **Step 1: Create `medios.html` with boilerplate, page header, and "Logos y arte" section**

```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Materiales y Medios — Marcha por la Justicia Reproductiva</title>
  <meta name="description" content="Descarga logos, materiales impresos, gráficas para redes sociales y recursos de prensa para difundir la Marcha por la Justicia Reproductiva.">
  <link rel="stylesheet" href="marcha-justicia-reproductiva.css">
</head>
<body>

  <!-- MEDIOS: PAGE HEADER -->
  <section class="medios-header">
    <div class="container">
      <h1 class="medios-title">Materiales <span class="script-accent">y medios</span></h1>
      <p class="medios-description">Descarga logos, materiales impresos, gráficas para redes sociales y recursos de prensa para difundir la marcha.</p>
    </div>
  </section>

  <!-- MEDIOS: LOGOS Y ARTE -->
  <section class="medios-section">
    <div class="container">
      <h2 class="medios-category-title">Logos y arte</h2>
      <div class="medios-grid medios-grid--2">
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--green">SVG</div>
          <div class="medios-card-body">
            <p class="medios-card-name">Lockup principal</p>
            <p class="medios-card-meta">SVG · Vector</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--purple">PNG</div>
          <div class="medios-card-body">
            <p class="medios-card-name">Lockup principal</p>
            <p class="medios-card-meta">PNG · 2400×1200</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
      </div>
    </div>
  </section>

</body>
</html>
```

- [ ] **Step 2: Open in browser and verify basic structure renders**

Open `medios.html` in a browser. It will be unstyled (no CSS yet for medios classes) but the HTML structure should render: a title, a category heading, and two card blocks with text content.

- [ ] **Step 3: Commit**

```bash
git add medios.html
git commit -m "feat: add medios.html scaffold with page header and logos section"
```

---

### Task 2: Add remaining three category sections to `medios.html`

**Files:**
- Modify: `medios.html` (insert before `</body>`)

- [ ] **Step 1: Add Material impreso, Redes sociales, Prensa sections and footer**

Insert the following after the "Logos y arte" `</section>` closing tag and before `</body>`:

```html
  <!-- MEDIOS: MATERIAL IMPRESO -->
  <section class="medios-section">
    <div class="container">
      <h2 class="medios-category-title">Material impreso</h2>
      <div class="medios-grid medios-grid--2">
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--neutral">PDF</div>
          <div class="medios-card-body">
            <p class="medios-card-name">Flyer 8.5×11</p>
            <p class="medios-card-meta">PDF · Listo para imprimir</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--neutral">PDF</div>
          <div class="medios-card-body">
            <p class="medios-card-name">Póster 11×17</p>
            <p class="medios-card-meta">PDF · Listo para imprimir</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- MEDIOS: REDES SOCIALES -->
  <section class="medios-section">
    <div class="container">
      <h2 class="medios-category-title">Redes sociales</h2>
      <div class="medios-grid medios-grid--3">
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--green">1080×1080</div>
          <div class="medios-card-body">
            <p class="medios-card-name">Instagram Post</p>
            <p class="medios-card-meta">PNG · 1080×1080</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--purple" style="min-height: 120px;">1080×1920</div>
          <div class="medios-card-body">
            <p class="medios-card-name">IG Story</p>
            <p class="medios-card-meta">PNG · 1080×1920</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--green" style="min-height: 50px;">1500×500</div>
          <div class="medios-card-body">
            <p class="medios-card-name">Twitter/X Header</p>
            <p class="medios-card-meta">PNG · 1500×500</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- MEDIOS: PRENSA -->
  <section class="medios-section">
    <div class="container">
      <h2 class="medios-category-title">Prensa</h2>
      <div class="medios-grid medios-grid--2">
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--purple">PDF</div>
          <div class="medios-card-body">
            <p class="medios-card-name">Comunicado de prensa</p>
            <p class="medios-card-meta">PDF · 2 páginas</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
        <div class="medios-card">
          <div class="medios-card-preview medios-card-preview--purple">PDF</div>
          <div class="medios-card-body">
            <p class="medios-card-name">Hoja informativa</p>
            <p class="medios-card-meta">PDF · 1 página</p>
            <a href="#" class="medios-card-download">Descargar</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="site-footer">
    <div class="container">
      <p><a href="index.html" class="footer-link">← Volver a la página principal</a></p>
      <p>Marcha por la Justicia Reproductiva &mdash; Puerto Rico 2026</p>
    </div>
  </footer>
```

- [ ] **Step 2: Verify all four sections render in browser**

Open `medios.html`. Confirm you see five sections of text: page header, Logos y arte, Material impreso, Redes sociales, Prensa, and a footer.

- [ ] **Step 3: Commit**

```bash
git add medios.html
git commit -m "feat: add remaining media kit sections and footer to medios.html"
```

---

### Task 3: Add CSS for the media kit page

**Files:**
- Modify: `marcha-justicia-reproductiva.css` (append before the RESPONSIVE section)

- [ ] **Step 1: Append the MEDIOS CSS section**

Insert the following block **before** the `/* RESPONSIVE */` comment block (line 498 area) in `marcha-justicia-reproductiva.css`:

```css
/* ==========================================================================
   MEDIOS — Media kit downloads page
   ========================================================================== */
.medios-header {
  padding: var(--space-16) 0 var(--space-12);
  background: #fff;
  position: relative;
}

.medios-header::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--purple);
}

.medios-title {
  font-family: var(--font-sans);
  font-weight: 900;
  font-size: clamp(var(--text-2xl), 4vw, var(--text-3xl));
  line-height: 1.1;
  text-transform: uppercase;
  color: var(--purple);
  letter-spacing: -0.01em;
  margin-bottom: var(--space-4);
}

.medios-title .script-accent {
  font-size: 1.5em;
}

.medios-description {
  color: var(--color-text-muted);
  font-size: var(--text-base);
  max-width: 55ch;
}

.medios-section {
  padding: var(--space-8) 0;
  background: #fff;
}

.medios-category-title {
  font-family: var(--font-sans);
  font-weight: 900;
  font-size: var(--text-lg);
  text-transform: uppercase;
  color: var(--purple);
  letter-spacing: 0.04em;
  margin-bottom: var(--space-6);
  padding-bottom: var(--space-4);
  border-bottom: 2px solid #eee;
}

.medios-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: var(--space-6);
}

@media (min-width: 768px) {
  .medios-grid--2 {
    grid-template-columns: 1fr 1fr;
  }

  .medios-grid--3 {
    grid-template-columns: 1fr 1fr 1fr;
  }
}

.medios-card {
  background: #f7f7f7;
  border: 1px solid #e0e0e0;
  border-radius: var(--radius-lg);
  padding: var(--space-6);
  transition: border-color var(--duration) var(--ease);
}

.medios-card:hover {
  border-color: var(--green);
}

.medios-card-preview {
  border-radius: var(--radius);
  min-height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: var(--space-4);
  font-size: var(--text-xs);
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: rgba(255, 255, 255, 0.5);
}

.medios-card-preview--green {
  background: var(--green);
}

.medios-card-preview--purple {
  background: var(--purple);
}

.medios-card-preview--neutral {
  background: #ccc;
  color: rgba(0, 0, 0, 0.3);
}

.medios-card-name {
  font-family: var(--font-sans);
  font-weight: 700;
  font-size: var(--text-sm);
  color: var(--color-text);
  margin-bottom: var(--space-1);
}

.medios-card-meta {
  font-size: var(--text-xs);
  color: var(--color-text-muted);
  margin-bottom: var(--space-4);
}

.medios-card-download {
  display: inline-block;
  background: var(--green);
  color: #fff;
  font-family: var(--font-sans);
  font-size: var(--text-xs);
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  padding: var(--space-2) var(--space-4);
  border-radius: var(--radius);
  text-decoration: none;
  transition: background var(--duration) var(--ease);
}

.medios-card-download:hover {
  background: var(--green-dark);
}

.footer-link {
  color: rgba(255, 255, 255, 0.6);
  text-decoration: none;
  font-size: var(--text-xs);
  text-transform: uppercase;
  letter-spacing: 0.04em;
  transition: color var(--duration) var(--ease);
}

.footer-link:hover {
  color: #fff;
}
```

- [ ] **Step 2: Open `medios.html` in browser and verify styles apply**

Confirm: purple top border on header, script accent in green, category headings with bottom borders, card grid layout with colored preview blocks, green download buttons, hover states on cards and buttons.

- [ ] **Step 3: Commit**

```bash
git add marcha-justicia-reproductiva.css
git commit -m "feat: add CSS for media kit page"
```

---

### Task 4: Add print styles for the media kit page

**Files:**
- Modify: `marcha-justicia-reproductiva.css` (append inside the existing `@media print` block)

- [ ] **Step 1: Add print rules inside the existing `@media print` block**

Add the following rules inside the `@media print { }` block (before the closing `}`), after the existing `.story-content p` rule:

```css
  .medios-header::before {
    display: none;
  }

  .medios-card {
    border: 1px solid #ccc;
    break-inside: avoid;
  }

  .medios-card-preview {
    display: none;
  }

  .medios-card-download {
    background: none;
    color: var(--green);
    border: 1px solid var(--green);
  }
```

- [ ] **Step 2: Verify print preview**

Open `medios.html`, trigger Print Preview (Cmd+P). Confirm: no purple top bar, no colored preview blocks, download buttons show as outlined text.

- [ ] **Step 3: Commit**

```bash
git add marcha-justicia-reproductiva.css
git commit -m "feat: add print styles for media kit page"
```

---

### Task 5: Add footer cross-navigation to `index.html`

**Files:**
- Modify: `index.html:201-205` (footer section)

- [ ] **Step 1: Update the landing page footer to include a link to `medios.html`**

Replace the existing footer content in `index.html`:

```html
  <footer class="site-footer">
    <div class="container">
      <p>Marcha por la Justicia Reproductiva &mdash; Puerto Rico 2026</p>
    </div>
  </footer>
```

With:

```html
  <footer class="site-footer">
    <div class="container">
      <p><a href="medios.html" class="footer-link">Materiales y medios →</a></p>
      <p>Marcha por la Justicia Reproductiva &mdash; Puerto Rico 2026</p>
    </div>
  </footer>
```

- [ ] **Step 2: Verify navigation works both ways**

Open `index.html` in browser. Click "Materiales y medios →" in the footer — should navigate to `medios.html`. On `medios.html`, click "← Volver a la página principal" — should navigate back to `index.html`.

- [ ] **Step 3: Commit**

```bash
git add index.html
git commit -m "feat: add footer link to media kit page from landing page"
```

---

### Task 6: Responsive check and final verification

- [ ] **Step 1: Test responsive layout**

Open `medios.html` in browser. Resize to mobile width (< 480px). Verify:
- All grids collapse to single column
- Cards stack vertically
- Text remains readable, no horizontal overflow
- Download buttons are tappable size

- [ ] **Step 2: Test at tablet width (768px breakpoint)**

Resize to ~768px. Verify:
- 2-column grids show 2 columns
- 3-column grid (Redes sociales) shows 3 columns
- No layout overflow

- [ ] **Step 3: Cross-browser spot check**

Open in Safari and Firefox (if available). Verify no major layout differences.
