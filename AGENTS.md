# AGENTS.md

## Architecture
Single static page. Everything (markup, styles, scripts) lives in `index.html`; there is no build step, framework, or package.json. `netlify.toml` publishes the repo root.

## Conventions
- Content is in Brazilian Portuguese (`lang="pt-BR"`).
- Colors are CSS custom properties in `:root` (royal blue palette + yellow CTA).
- All purchase buttons use class `.cta` and point to the Mercado Livre affiliate link `https://meli.la/21jdUj8`; the inline script attaches Meta Pixel `InitiateCheckout` and Google Ads conversion events to them. Keep new purchase buttons on `.cta` so tracking applies.
- The countdown timer is visual only: a 15-minute loop persisted in `sessionStorage`, restarting when it hits zero.

## Non-obvious decisions
- Product images are hotlinked from `clarid.com.br`; if that host changes, update the three `<img>` tags.
- The page was provided verbatim by the owner; keep edits minimal and targeted.
