# anygit

Multi-forge source control for Muxy — GitHub, Forgejo, and Gitea. PR backend is
chosen per repository behind `src/lib/forge/` (gh.js + tea.js, index.js
dispatches by origin host). Based on the official Git extension by Saeed Vaziry;
see README credits.

## Stack

- NPM
- Tailwindcss
- Vanilla JavaScript

## Building & editing

Install deps with `npm install --ignore-scripts`, then `npm run build` to produce
the bundled files in `dist/`. After rebuilding, click "Reload" in the Muxy
Extensions modal to pick up the changes.

## Guides

- Never use code comments. if you see anywhere, remove
- Write less code, small components, re-usable code.
- Avoid large files
- Don't patch symptoms and fix the root cause
