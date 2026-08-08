# winter-page.github.io

Personal blog, built with Jekyll (`jekyll-theme-clean-blog`) and published on GitHub Pages.

## Publishing a new post

1. Add a Markdown file to `_posts/` named `YYYY-MM-DD-slug.md`:
   ```yaml
   ---
   layout: post
   title:  "Post Title"
   date:   2026-08-08 10:00:00 +0200
   background: '/images/frost.jpg'
   tags: [python, learning]
   ---
   Regular **Markdown** content goes here.
   ```
2. Commit and push to `master`.

That's it — a GitHub Actions workflow (`.github/workflows/jekyll.yml`) builds the site and deploys it to GitHub Pages automatically on every push. There is no local build step and nothing else to copy or commit.

- Posts sharing a `tags:` value automatically show up under each other as "Related posts", and are listed on `/tags/`.
- To draft a post without publishing it yet, put it in `_drafts/` (no date prefix needed) instead of `_posts/`.

## Local development (optional)

```
bundle install
bundle exec jekyll serve
```
