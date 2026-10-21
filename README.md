# findingnami.com

Static site for GitHub Pages. No build step.

## Pages

| URL | File |
| --- | --- |
| `/` (includes About and Contact) | `index.html` |
| `/apps/` | `apps/index.html` |
| `/apps/readfully/` | `apps/readfully/index.html` |
| `/apps/privacy/` | `apps/privacy/index.html` |
| `/apps/support/` | `apps/support/index.html` |
| `/photography/` redirects to the Adobe Portfolio | `photography/index.html` |
| `/podcast/` redirects to Spotify | `podcast/index.html` |
| `/youtube/` redirects to YouTube | `youtube/index.html` |
| `/about/` and `/contact/` redirect to the home sections | `about/`, `contact/` |

Shared styles and animation: `assets/style.css`, `assets/site.js`.

## Deploy

1. Before pointing the domain here, remove `findingnami.com` as the custom domain in Adobe Portfolio's settings. Your portfolio's own address, `findingnami.myportfolio.com`, then works on its own, and `/photography/` can redirect to it without looping.
2. Create a GitHub repository and push these files to the `main` branch, with `index.html` at the repository root.
3. In the repository, open Settings > Pages. Set Source to "Deploy from a branch", branch `main`, folder `/ (root)`.
4. The `CNAME` file already sets the custom domain to `findingnami.com`. Check it appears under Settings > Pages > Custom domain.
5. At your domain registrar, add the DNS records GitHub documents for an apex domain (A records for the apex, and a CNAME for `www` pointing to `<your-username>.github.io`). Confirm the current values in GitHub's "Managing a custom domain for your GitHub Pages site" documentation.
6. Once DNS settles, tick "Enforce HTTPS" in Settings > Pages.

## Notes

- Links are root-relative (`/apps/`). They work on the custom domain `findingnami.com`. If you preview at `username.github.io/repo-name/`, they will not.
- Update your App Store Connect privacy policy and support URLs to `https://findingnami.com/apps/privacy/` and `https://findingnami.com/apps/support/` when these pages go live.
- Replace the privacy policy and support text with the exact wording from your existing pages if you need it verbatim.
