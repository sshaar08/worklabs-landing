# CLAUDE.md

Guidance for AI coding agents working in this repository.

## Project

Static marketing site for Worklabs HQ — plain **HTML + CSS**, no framework, no build step, no JS. Deployed via GitHub Pages to `worklabshq.com`.

## Key facts

- Entry point: `index.html` (single page, section anchors: `#services`, `#approach`, `#about`, `#contact`).
- All styling: `css/style.css`. Theme uses CSS variables in `:root` (`--primary`, `--accent`, `--bg`, etc.).
- `CNAME` — must stay `worklabshq.com`.
- `.nojekyll` — required; do not delete (Pages build fails without it).
- Deploys on push to `master` via GitHub Pages ("Deploy from a branch").

## Conventions

- Keep it dependency-free. Do not add a build tool, package manager, or framework unless explicitly requested.
- Edit content directly in `index.html`; keep semantic HTML and existing section ids.
- Reuse existing CSS classes/variables; avoid inline styles except trivial one-offs.
- Maintain responsive behavior (mobile breakpoint at `max-width: 768px`).
- Accessibility: every form field keeps an associated `<label>`; interactive elements are real `<a>`/`<button>`.

## Do not

- Do not rename `master` (Pages source is pinned to it).
- Do not remove/edit `CNAME` or `.nojekyll`.
- Do not commit `.DS_Store` (gitignored).

## Verify changes

```bash
python3 -m http.server 8080   # preview at http://localhost:8080
```
