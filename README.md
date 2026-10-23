# quietmatter.studio

The site of Quiet Matter. Static, no build. Everything that is published is in `site/`.

- `site/index.html` — the whole site (HTML, CSS, JS in one file)
- `site/legal.html` — legal notice (change only with Amaury's approval)
- `site/favicon.*`, `site/apple-touch-icon.png`

Every push to `main` publishes to https://quietmatter.studio through GitHub Actions (`.github/workflows/deploy.yml`).
A push to any other branch publishes a preview at `https://<branch>.quietmatter.pages.dev`.

Rollback: Cloudflare → Workers & Pages → quietmatter → Deployments → previous version → ⋯ → Rollback.
Or revert the commit on `main`.

Secrets needed in the repository (Settings → Secrets and variables → Actions):
- `CLOUDFLARE_API_TOKEN` — a token with *Account → Cloudflare Pages → Edit*
- `CLOUDFLARE_ACCOUNT_ID`
