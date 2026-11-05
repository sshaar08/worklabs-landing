# Worklabs HQ — worklabshq.com

Marketing site for **Worklabs HQ**, a small-business consulting practice offering AI integration, infrastructure/DevOps, quality engineering, and local AI & hardware setup.

Static site (plain HTML + CSS), hosted on **GitHub Pages** at **[worklabshq.com](https://worklabshq.com)**.

## Structure

```
.
├── index.html      # Single-page site
├── css/style.css   # All styles (dark theme, CSS variables)
├── CNAME           # GitHub Pages custom domain
├── .nojekyll       # Bypass Jekyll processing (plain static files)
└── .gitignore
```

## Local preview

No build step. Serve the folder with any static server:

```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

## Deploy

Pushing to `master` triggers a GitHub Pages build automatically.

- Repo → **Settings → Pages**
- Source: **Deploy from a branch** → `master` → `/ (root)`
- Custom domain: `worklabshq.com` (handled by `CNAME` file)

## DNS (Cloudflare — records set to *DNS only / grey cloud*)

| Type | Name | Content |
|------|------|---------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `sshaar08.github.io` |

Do **not** place a CNAME on the apex (`@`) or modify MX/email records.

## Editing

- Content lives in `index.html`.
- Colors/theme are CSS variables in `css/style.css` under `:root`.
- The intake form (`#contact`) currently has a placeholder Formspree action — not yet wired to a backend.
