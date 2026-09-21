# ehsan-mahmoodi.github.io

Personal site. Static HTML, no build step, served by GitHub Pages.

## Layout

```
index.html                  single page: about, expertise, projects, publications, contact
projects/biodiesel.html     design case study, linked from the projects section
assets/diagrams/*.svg       one diagram per project, theme-aware
assets/*.png|gif            screenshots and recordings
```

## Conventions

- Diagrams are hand-written SVG at `400x180` for project cards, wider for case-study figures.
  Each carries its own `prefers-color-scheme` block so it follows the reader's theme.
- Colours come from the GitHub palette: `#58a6ff` accent, `#161b22` panel, `#0d1117` background,
  with a light-mode override at the bottom of each `<style>`.
- No simulation model files are published. Projects are described by problem, method and diagram.

## Editing

Open `index.html` and edit directly. Project cards follow one pattern:

```html
<div class="project-card">
  <img src="assets/diagrams/NAME.svg" alt="..." class="project-card-image" loading="lazy">
  <div class="card-header"><h3>Title</h3><span class="card-icon">&#9881;</span></div>
  <div class="card-meta">Year - client</div>
  <p>What the problem was and what was done.</p>
  <div class="card-tags"><span class="card-tag">Tag</span></div>
  <div class="card-links"><a href="#" class="card-link">Link</a></div>
</div>
```

## To do

- Add video links for the simulation recordings (assembly line balancing, acid plant).
  Cards carrying a `media-note` div are the placeholders.
