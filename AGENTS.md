# AGENTS.md

## Architecture
Static single-page portfolio with no framework, package.json or build step. Netlify publishes the `public/` directory as it is (see `netlify.toml`).

## Key files
- `public/index.html`: the whole site, with markup, CSS in a `<style>` block (theme variables in `:root`) and a small inline script for the year and fade-in animations.
- `public/photo.jpeg`: the original 1280×1280 portrait.

## Conventions and decisions
- The portrait loads through Netlify Image CDN (`/.netlify/images?url=/photo.jpeg&w=600&fm=webp`) so visitors don't download the full-size original.
- Keep the site dependency-free. Edit content directly in the HTML and keep the existing section numbering ("01 / Featured work" and so on).
- Responsive breakpoints are at 760px and 430px.
