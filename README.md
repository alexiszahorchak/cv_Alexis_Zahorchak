# Alexis Zahorchak - Personal Website

This repository hosts my personal website featuring my CV and technical blog, built with [Quarto](https://quarto.org) and deployed to GitHub Pages.

## About

- **CV/Home Page**: Professional background, research experience, and technical skills
- **Blog**: Technical notes on neuroscience research, data analysis, and engineering

## Building Locally

### Prerequisites

Install Quarto from [quarto.org](https://quarto.org/docs/get-started/)

### Commands

Preview the site locally:
```bash
quarto preview
```

Render the site (outputs to `docs/`):
```bash
quarto render
```

## Deployment

The site deploys automatically to GitHub Pages via GitHub Actions on every push to the `main` branch. The workflow:

1. Sets up Quarto
2. Renders the website to `docs/`
3. Deploys to GitHub Pages

View the workflow status in the [Actions](../../actions) tab.

## Adding Blog Posts

To add a new blog post:

1. Create a new directory in `posts/` with format `YYYY-MM-DD-post-title/`
2. Add an `index.qmd` file with front matter:
   ```yaml
   ---
   title: "Your Post Title"
   description: "Brief description"
   author: "Alexis Zahorchak"
   date: "YYYY-MM-DD"
   categories: [category1, category2]
   ---
   ```
3. Write your content using Markdown
4. Commit and push—the site will update automatically

## Structure

```
├── _quarto.yml              # Main configuration
├── index.qmd                # CV (home page)
├── blog.qmd                 # Blog listing page
├── posts/                   # Blog posts directory
│   ├── _metadata.yml        # Blog configuration
│   └── YYYY-MM-DD-title/
│       └── index.qmd        # Individual post
├── .github/workflows/
│   └── publish.yml          # GitHub Actions deployment
└── docs/                    # Generated output (Git ignored except on deploy)
```

## Technologies

- [Quarto](https://quarto.org) - Scientific and technical publishing system
- [GitHub Pages](https://pages.github.com) - Static site hosting
- [GitHub Actions](https://github.com/features/actions) - CI/CD automation
