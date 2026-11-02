# Karatig Express — Public Landing Page

This repository is **only the static public website** for DZRS 96.5 Karatig Express. The full application stays in the existing **private** Apps Script/GitHub project. No Gemini key or private source files belong here.

## Activate the launch button

The website intentionally ships with an inactive launch button until the owner confirms which **LIVE** Google Apps Script deployment URL to use and its intended access permissions.

1. Obtain your existing LIVE web-app URL from **Google Apps Script → LIVE project → Deploy → Manage deployments → Web app URL**. Use the `/exec` URL, **not** the `/dev` testing URL.
2. In `index.html`, replace `const APP_URL = '';` with `const APP_URL = 'https://script.google.com/macros/s/YOUR_DEPLOYMENT_ID/exec';`.
3. Commit this one-file change in the **public landing-page repository**, not the private source-code repository.
4. If the existing Apps Script web app has access **Only myself**, this public page does not make it public. Other visitors will still need the appropriate permissions. Do **not** loosen production access without reviewing Gemini quotas, abuse protection, and security first.

A deployed `/exec` URL can be published as a launch link. **Never** put an API key, clasp credentials, or internal Script Properties in the public site.

## Publish with GitHub Pages

1. Create a **public** repository named `karatig-express-site` under `tchaikovskeith` (or another name, with matching URL).
2. Commit `index.html`, `.nojekyll`, and this `README.md` to its `main` branch.
3. Go to **Settings → Pages → Build and deployment** and choose **Deploy from a branch**, branch **main**, directory **/(root)**; save.
4. Your site will be published at `https://tchaikovskeith.github.io/karatig-express-site/` once GitHub Pages completes publishing.

The public landing site does not generate scripts, call Gemini, or export documents itself: those features remain in Google Apps Script.

## Site structure

- `index.html`: self-contained responsive landing page; no build tools or external libraries required.
- `.nojekyll`: bypass Jekyll processing.
- `README.md`: owner instructions.
