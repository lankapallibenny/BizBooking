# BizTrade Live Sessions

Static GitHub Pages deployment for the BizTrade Live Sessions page.

## GitHub Pages setup

1. Push this repository to GitHub.
2. In the repository, open **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions**.
3. The workflow in `.github/workflows/pages.yml` deploys the site on pushes to `main` (or run it manually from the Actions tab).

Because this repository is named `BizBooking`, its standard project-site address will be:

`https://<your-github-username>.github.io/BizBooking/`

To use the root `https://<your-github-username>.github.io/` address, GitHub requires a repository named exactly `<your-github-username>.github.io`. A project repo cannot claim that root username subdomain by itself.

## Booking functionality

The attached page is preserved as `index.html`. It expects Claude's embedded `window.claude` database and user APIs for listings, bookings, sign-in, and host controls. Those APIs are not supplied by GitHub Pages, so deploying the page alone will show its fallback state and interactive booking features will not work. To make those features live on GitHub Pages, connect a separate backend/auth provider and adapt the page to use it.
