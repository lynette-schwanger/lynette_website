# Lynette Schwanger — Personal Quarto Website

## Structure

```
├── _quarto.yml         # Site configuration, navbar, theme
├── custom.scss         # Custom SCSS — colors, typography, component styles
├── index.qmd           # Home page (hero + about + competencies + education)
├── portfolio.qmd       # Portfolio page (add project cards here)
├── resume.qmd          # Resume page (inline + PDF download)
└── SchwangerLynette_Resume.pdf   # Place PDF here for download link to work
```

## Setup

1. **Install Quarto** — https://quarto.org/docs/get-started/
2. **Place your PDF** — Copy `SchwangerLynette_Resume.pdf` into the root of this project folder (same level as `_quarto.yml`).
3. **Preview locally:**
   ```bash
   quarto preview
   ```
4. **Build for deployment:**
   ```bash
   quarto render
   ```
   Output goes to the `_site/` folder.

## Deploy

- **GitHub Pages**: Push to a repo, enable GitHub Pages from the `_site` folder (or use `quarto publish gh-pages`).
- **Netlify**: Drag and drop the `_site/` folder to netlify.com/drop.
- **Quarto Pub**: Run `quarto publish quarto-pub`.

## Adding Portfolio Projects

Open `portfolio.qmd` and find the commented-out example cards. Copy and uncomment a block for each project:

```html
<div class="portfolio-card">
  <div class="card-type">GitHub Repo</div>   <!-- or: Quarto Report, Document, Policy Brief -->
  <h3>Your Project Title</h3>
  <p>Short description of the project.</p>
  <a class="card-link" href="YOUR_URL">View on GitHub →</a>
</div>
```

Once you have at least one card, remove the `.empty-state` block.

## Updating the Resume

- **PDF only**: Replace `SchwangerLynette_Resume.pdf` with the new version.
- **Inline content**: Edit `resume.qmd` directly — add new `.resume-entry` blocks following the existing pattern.

## Colors (edit in `custom.scss`)

| Variable    | Value     | Used for               |
|-------------|-----------|------------------------|
| `$primary`  | `#2e7d6e` | Links, headings, tags  |
| `$secondary`| `#4a9ebb` | Card type labels       |
| `$accent`   | `#a8d5c2` | Soft mint accents      |
| `$light-bg` | `#f5f9f7` | Tag/skill backgrounds  |
| `$muted`    | `#6b8f85` | Subtitles, dates       |
