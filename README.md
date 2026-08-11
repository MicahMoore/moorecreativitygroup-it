# Moore Creativity Group — IT Consulting

Single-page static site for the IT/systems consulting side of Moore Creativity Group. No build step, no dependencies — plain HTML/CSS.

## Deploy (GitHub Pages)

1. Push this repo to GitHub (e.g. `MicahMoore/moorecreativitygroup-it`).
2. In the repo's **Settings → Pages**, set source to `Deploy from a branch`, branch `main`, folder `/ (root)`.
3. In Cloudflare DNS for `moorecreativitygroup.com`, add:
   - Type: `CNAME`
   - Name: `it`
   - Target: `<username>.github.io`
   - Proxy status: **DNS only** (grey cloud) — GitHub Pages issues its own TLS cert and needs to see the real request.
4. Back in GitHub Pages settings, set the custom domain to `it.moorecreativitygroup.com` and enable "Enforce HTTPS" once the cert is issued (can take a few minutes).

The `CNAME` file in this repo already points to `it.moorecreativitygroup.com`, so step 4 should auto-fill.

## Editing

Everything lives in `index.html` — copy, styling, and layout are all inline. Update content directly and push to `main`; GitHub Pages redeploys automatically.
