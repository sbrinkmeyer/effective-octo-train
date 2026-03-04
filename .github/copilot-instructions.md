# Copilot Instructions

This repository is a Hugo static site using `hugo-universal-theme` and is intended for Netlify deployment.

## Project context
- Hugo config lives in `hugo.toml`.
- Content pages are under `content/` and posts under `content/posts/`.
- Theme is tracked in `themes/hugo-universal-theme/`.

## Coding and editing guidelines
- Prefer minimal, focused changes.
- Keep front matter valid and consistent with existing content files.
- Preserve Hugo template compatibility; do not introduce unsupported functions.
- Avoid changing theme internals unless explicitly requested.
- For new pages, prefer content-first changes in `content/` before touching theme files.

## Netlify and deployment guidelines
- Prefer reproducible Hugo build settings for Netlify.
- If deployment setup is requested, use a clear `netlify.toml` and avoid hidden assumptions.
- Keep environment variable names explicit; never hardcode secrets.

## Validation
- Validate with local Hugo build commands when asked:
  - `hugo server -D` for local preview
  - `hugo --gc --minify` for production-style build
