# Zixi (Charlie) Chen - Personal Website

Personal academic website for Zixi (Charlie) Chen, a Computer Science PhD student at NYU Courant.

**Website:** [charliezchen.github.io](https://charliezchen.github.io)

## About

This website showcases my research, publications, and projects. I am currently working with Prof. Andrew Gordon Wilson on efficiently training large neural networks.

## Built With

This site is built using [Jekyll](https://jekyllrb.com/) with the [al-folio](https://github.com/alshedivat/al-folio) theme, hosted on [GitHub Pages](https://pages.github.com/).

---

## Repository Structure

```
.
├── _bibliography/        # BibTeX files for publications
│   └── papers.bib        # Main bibliography file
├── _data/                # YAML data files
│   ├── cv.yml            # CV/resume content
│   ├── repositories.yml  # Featured GitHub repos
│   ├── coauthors.yml     # Coauthor info for linking
│   └── venues.yml        # Publication venue abbreviations
├── _includes/            # Reusable HTML components
├── _layouts/             # Page layout templates
├── _news/                # News/announcement items
├── _pages/               # Main site pages (about, publications, etc.)
├── _posts/               # Blog posts
├── _projects/            # Project pages
├── _sass/                # SCSS stylesheets
├── assets/
│   ├── img/              # Images (profile pic, publication previews)
│   ├── pdf/              # PDF files (papers, slides)
│   ├── json/             # JSON data (resume.json for CV)
│   └── html/             # Standalone HTML artifacts
├── _config.yml           # Main site configuration
└── _site/                # Generated site (do not edit)
```

---

## Adding Content

### Publications

Edit `_bibliography/papers.bib` to add new publications in BibTeX format:

```bibtex
@inproceedings{lastname2024title,
  title={Your Paper Title},
  author={LastName, FirstName and Coauthor, Name},
  booktitle={Conference Name (Abbrev)},
  year={2024},
  arxiv={2401.12345},                    # arXiv ID (optional)
  url={https://arxiv.org/abs/2401.12345},
  preview={paper_preview.png},           # Thumbnail in assets/img/
  pdf={paper.pdf},                       # PDF in assets/pdf/
  code={https://github.com/...},         # Code repository (optional)
  selected={true}                        # Show on homepage
}
```

Supported fields: `abstract`, `arxiv`, `code`, `pdf`, `slides`, `poster`, `video`, `website`, `blog`, `preview`, `selected`.

### CV / Experience

**Option 1:** Edit `_data/cv.yml` for YAML-based CV:

```yaml
- title: Experience
  type: time_table
  contents:
    - title: Position Title
      institution: Institution Name
      year: 2023 - Present
      description:
        - Description point 1
        - Description point 2
```

**Option 2:** Edit `assets/json/resume.json` for JSON Resume format (takes precedence if present).

### Blog Posts

Create a new file in `_posts/` with naming convention `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: Your Post Title
date: 2024-01-15 10:00:00
description: Brief description for previews
tags: tag1 tag2
categories: category-name
---

Your content here in Markdown...
```

### News / Announcements

Create a file in `_news/` (e.g., `announcement_4.md`):

```markdown
---
layout: post
date: 2024-01-15 12:00:00
inline: true
related_posts: false
---

Your announcement text here.
```

### Standalone HTML Artifacts

Place HTML files in `assets/html/` and link to them directly:

```markdown
[View Demo](/assets/html/my-demo.html)
```

For interactive visualizations, you can also use:
- `assets/jupyter/` for Jupyter notebooks
- `assets/plotly/` for Plotly figures

### Projects

Create a file in `_projects/` (e.g., `my_project.md`):

```markdown
---
layout: page
title: Project Name
description: Brief project description
img: assets/img/project_thumbnail.jpg
importance: 1
category: work
---

Project details in Markdown...
```

### Pages

Main pages live in `_pages/`. Edit existing ones or create new pages:
- `about.md` - Homepage content
- `publications.md` - Publications page
- `misc.md` - Miscellaneous page

---

## Configuration

Key settings in `_config.yml`:

| Setting | Description |
|---------|-------------|
| `first_name`, `last_name` | Your name |
| `email` | Contact email |
| `github_username` | GitHub profile |
| `scholar.last_name` | Name highlighting in publications |
| `announcements.enabled` | Show news on homepage |
| `latest_posts.enabled` | Show blog posts on homepage |

---

## Local Development

### Prerequisites

- Ruby and Bundler
- ImageMagick (for responsive images)

### Setup

```bash
bundle install
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

### Docker Alternative

```bash
docker-compose up
```

---

## Deployment

The site auto-deploys to GitHub Pages on push to `master`. See `.github/workflows/` for CI configuration.

## License

The theme is available under the [MIT License](LICENSE).
