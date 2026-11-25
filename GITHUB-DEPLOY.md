# Quick GitHub + Netlify deployment checklist

1. Create an empty GitHub repository.
2. Upload the **contents** of this project directory to the repository root.
3. Confirm `package.json`, `index.html`, `src/`, and `netlify.toml` are at the top level.
4. On Netlify: Add new site → Import from Git → choose the repository.
5. Build command: `npm run build`; publish directory: `dist`; base directory: blank.
6. Deploy and open the resulting site URL.

The repository's `netlify.toml` already contains the build/publish settings and SPA redirect. Do not commit `node_modules/` or `dist/` (they are ignored).

To build locally before deployment, run `npm install`, then `npm run build`.
