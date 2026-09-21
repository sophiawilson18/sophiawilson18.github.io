# sophiawilson18.github.io

Personal academic website for Sophia N. Wilson, PhD student at the SAINTS Lab, University of Copenhagen. Built with Jekyll using the AcademicPages theme.

Live site: https://sophiawilson18.github.io

---

## Repo structure

```
_config.yml              # Site settings (title, author info, nav, collections)
_config.dev.yml          # Overrides for local development

_pages/                  # One file per page on the site
  about.md               # Homepage (permalink: /)
  cv.md                  # CV page, links to PDF download
  publications.md        # Publications listing
  teaching.md            # Teaching and outreach
  outreach.md            # Media coverage and talks
  projects.md            # Research projects
  files/                 # PDFs served from the site (CV, etc.)
  images/                # Images used in pages

_publications/           # One .md file per publication
  files/                 # PDFs of papers

_data/
  navigation.yml         # Top navigation bar links
  ui-text.yml            # Theme UI labels (no need to edit)

_layouts/                # Page templates (from theme, no need to edit)
_includes/               # Reusable HTML components (from theme, no need to edit)
_sass/                   # Stylesheets (from theme, no need to edit)
assets/                  # CSS, JS, fonts (from theme, no need to edit)
images/                  # Site-wide images (e.g. profile photo sw.png)
```

---

## How to add or edit content

### Edit a page
Open the relevant file in `_pages/` and edit the text below the front matter (the `---` block at the top).

### Add a new page
1. Create a new `.md` file in `_pages/` with this front matter:
   ```yaml
   ---
   layout: archive
   title: "Page Title"
   permalink: /your-url/
   author_profile: true
   ---
   ```
2. Add it to `_data/navigation.yml` to make it appear in the nav bar:
   ```yaml
   - title: "Page Title"
     url: /your-url/
   ```

### Add a publication
Create a new `.md` file in `_publications/` following the naming pattern `YYYY-MM-DD-short-title.md`. Use an existing file as a template for the front matter fields (`title`, `pubtype`, `venue`, `date`, etc.).

### Update the CV
Replace `_pages/files/CV.pdf` with the new version.

---

## Running locally

```bash
bundle exec jekyll serve
```

Then open http://localhost:4000 in your browser.
