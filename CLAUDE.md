# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal "about me" Jekyll site hosted on GitHub Pages using the `minima` theme. The site includes a homepage and a blog section with daily posts.

## Development Commands

```bash
# Install dependencies
bundle install

# Run local development server
bundle exec jekyll serve

# Build the site
bundle exec jekyll build
```

## Architecture

The site uses Jekyll's default structure:
- Pages are markdown files in the root directory with YAML front matter
- Blog posts go in `_posts/` directory following the naming convention `YYYY-MM-DD-title.md`
- The blog index at `main/blog.md` uses Jekyll's Liquid templating to iterate over `site.posts` and display them chronologically
- The `minima` theme provides layouts and styling (no custom layouts in this repo)
- Configured for GitHub Pages deployment using the `github-pages` gem

## Important Notes

- The `_config.yml` uses the `minima` theme (not `jekyll-theme-minimal`)
- Changes to `_config.yml` require server restart when using `bundle exec jekyll serve`
- The site uses an empty baseurl (deployed to root, not `/about-me` subpath)
