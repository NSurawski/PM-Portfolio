---
name: page-structure
description: Enforce consistent page structure and navigation for portfolio detail pages
autoInvoke:
  - keyword: "new page"
  - keyword: "new prd"
  - keyword: "case study"
  - keyword: "add page"
  - pattern: "prd-*.html"
  - pattern: "case-studies.html"
  - pattern: "teardown-*.html"
  - pattern: "metrics-*.html"
  - pattern: "research-*.html"
---

# Portfolio Page Structure

All detail pages (PRDs, case studies, teardowns, metrics, research) follow the same structural pattern.

## Required structure for detail pages

```html
<div class="page">
  <a href="index.html" class="back-link">&larr; Back to Portfolio</a>
  <div class="prd-header">
    <span class="prd-label">PAGE TYPE</span>
    <h1>Page Title</h1>
    <p class="subtitle">Subtitle text</p>
  </div>
  <div class="meta-grid">
    <div class="meta-item"><span class="meta-label">Label</span>Value</div>
    <!-- more meta items -->
  </div>
  <!-- Content sections -->
</div>
```

## Required elements
1. **Back link** — always links to `index.html` with `class="back-link"` and `&larr;` arrow
2. **Header** — `.prd-header` with `.prd-label`, `<h1>`, and `.subtitle`
3. **Meta grid** — `.meta-grid` with `.meta-item` entries showing metadata
4. **Self-contained CSS** — each page includes its own `<style>` block (no shared stylesheet)

## When adding a new page
1. Copy the structure from an existing page of the same type
2. Include the full `:root` CSS variable block
3. Include all shared CSS classes (`.page`, `.back-link`, `.prd-header`, `.meta-grid`, etc.)
4. Add a link to the new page from the relevant project card in `index.html`
5. Add the page to `sitemap.xml`

## Navigation
- Detail pages link back to index via `.back-link`
- Index.html links to detail pages via relative hrefs in project cards
- All links use relative paths (no absolute URLs)
