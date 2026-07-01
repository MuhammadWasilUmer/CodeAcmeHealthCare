# CodeAcme — AI agents for healthcare

Marketing site for **CodeAcme**, a voice-AI agency focused on healthcare.

This repository is a **single self-contained static page**: [`index.html`](./index.html).
Everything the site needs — the React runtime, the in-browser compiler, all images,
the four call recordings, and the case-study PDFs — is embedded in that one file as
base64 and rebuilt into `blob:` URLs at runtime. There are **no external network
dependencies** and nothing else to upload.

The browser tab icon (favicon) is the CodeAcme logo mark, inlined as a data URI.

## Deploying

The site is served straight from `index.html` at the repository root.

### GitHub Pages (automatic)
`.github/workflows/deploy.yml` publishes the site on every push to `main`.
One-time setup: **Settings → Pages → Build and deployment → Source: GitHub Actions**.

### GitHub Pages (deploy from branch)
Alternatively: **Settings → Pages → Source: Deploy from a branch → `main` / `root`**.

### Any static host
Because it is a single file, you can also drop `index.html` onto Netlify, Vercel,
S3, or any web server — no build step required.

## Note
`index.html` is ~27 MB (everything is inlined). It loads with a single request and
then runs fully offline. The source design bundle it was exported from lives outside
this repo.
