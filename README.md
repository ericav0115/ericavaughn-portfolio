# Erica Vaughn: Portfolio

Personal portfolio site: data & platform engineering, cloud architecture, technical leadership, and speaking.
Plain HTML, CSS, and a little JavaScript. No build step, no dependencies.

## Structure

```
index.html                  Home: hero, work (12 case studies, filterable), about, speaking, ideas, contact
projects/*.html             One page per case study
case-study-template.html    Blank template for new case studies (noindex)
styles.css                  Visual system + responsive styles
script.js                   Mobile nav, reveal animations, project filters
favicon.svg
assets/images/              Optimized web images (hero, about, speaking)
.nojekyll                   Tells GitHub Pages to serve files as-is
```

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Deploy

**GitHub Pages:** Settings → Pages → Deploy from a branch → `main` / root. The site will be at
`https://ericav0115.github.io/ericavaughn-portfolio/`. To use a custom domain, add it under Pages settings
(GitHub creates a `CNAME` file) and point your DNS at GitHub Pages.

**Vercel / Netlify:** Import the repo, choose framework preset "Other" (static), leave the build command empty,
and set the output directory to the repo root.

## Adding a case study

1. Copy an existing page in `projects/` (or `case-study-template.html`) to `projects/your-project.html`.
2. Fix relative paths if you started from the template (`../styles.css`, `../index.html`).
3. Add a card to the `<!-- PROJECTS -->` block in `index.html`. Set `data-cats` to any of
   `platform`, `apps`, `ai`, `analytics` so the filters pick it up.
4. Update the previous/next links at the bottom of the neighboring project pages.

## Confidentiality

Every case study is a sanitized reconstruction. Organization, employer, client, and vendor names are left out
on purpose, along with proprietary code, data, internal table names, and architecture diagrams. Keep new
content to that standard: describe partners generically ("a major retailer", "a third-party planning
platform") and use synthetic examples for technical proof.

Full-size original photos live in `assets/images/originals/` locally and are git-ignored.
