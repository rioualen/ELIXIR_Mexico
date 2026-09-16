# Personal site

A minimal, single-column Jekyll site for a portfolio + blog + contact form,
inspired by the layout style of clean personal-website themes. Free to use,
no license fee, deploys straight to GitHub Pages via GitHub Actions.

## Structure

```
.
├── _config.yml          # site settings — name, social links, formspree id, etc.
├── _layouts/             # default, home, post, portfolio-item
├── _includes/            # header, footer, social icons
├── _sass/main.scss       # all styling
├── _posts/                # blog posts (YYYY-MM-DD-title.md)
├── _portfolio/            # portfolio/case-study items (a Jekyll collection)
├── assets/                # css, images
├── index.md, about.md, work.md, blog.md, contact.md
└── .github/workflows/pages.yml   # builds & deploys on every push to main
```

## Quick start

1. **Use this repo as a template**, or clone it, then rename it to
   `yourusername.github.io` (for a user site) or keep any name for a
   project site.
2. Edit `_config.yml`:
   - `title`, `tagline`, `description`, `author`
   - `url` / `baseurl` — for a project site, set `baseurl: "/repo-name"`
   - `social` — fill in the handles you want shown, leave others blank
   - `formspree_id` — sign up free at [formspree.io](https://formspree.io) to enable the contact form
3. Replace the content in `about.md`, and add/remove posts in `_posts/`
   and portfolio items in `_portfolio/`.
4. Push to `main`. The included GitHub Actions workflow builds the site
   and deploys it automatically.

### Enable GitHub Pages (one-time)

In your repo: **Settings → Pages → Build and deployment → Source →
GitHub Actions**. The next push to `main` will publish the site.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`.

## Adding content

**Blog post** — add a file to `_posts/` named `YYYY-MM-DD-title.md`:

```yaml
---
title: "My post"
date: 2026-01-01
tags: [tag1, tag2]
---
Post content in Markdown.
```

**Portfolio item** — add a file to `_portfolio/`:

```yaml
---
title: "Project name"
summary: "One-line description"
image: /assets/images/your-image.jpg      # single hero image, or:
gallery:                                    # a list, for a grid gallery
  - /assets/images/one.jpg
  - /assets/images/two.jpg
url_live: "https://example.com"
url_repo: "https://github.com/you/project"
---
Project write-up in Markdown.
```

## License

Site code (layouts, includes, styles) is provided as-is — use, modify, and
reuse freely for your own site.
