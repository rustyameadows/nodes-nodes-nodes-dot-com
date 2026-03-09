# Nodes Nodes Nodes GitHub Pages Deploy Guide

## Goal
Publish a plain static marketing site for `nodesnodesnodes.com` from this dedicated site repo using GitHub Pages, with Cloudflare handling DNS.

## Assumptions
- this repo is the dedicated website repo
- the site is plain static HTML/CSS/JS with no build step
- GitHub Pages will publish from the repository root on the default branch
- Cloudflare is already the DNS provider for `nodesnodesnodes.com`
- no backend waitlist form or download gate exists yet

## Recommended Repo Layout

```text
/
  index.html
  product/index.html
  workflow/index.html
  download/index.html
  faq/index.html
  privacy/index.html
  styles/site.css
  scripts/site.js
  assets/
    images/
    icons/
  404.html
  CNAME
```

Notes:
- each public route is a real folder with an `index.html`
- `styles/site.css` should hold the shared light marketing design system
- `scripts/site.js` is optional and should stay minimal
- `CNAME` should contain only `nodesnodesnodes.com`

## Publishing Approach
Use GitHub Pages with:
- source branch: default branch
- publish directory: repository root

Reasoning:
- no build pipeline is needed
- the route structure stays transparent
- GitHub Pages can serve the custom apex domain directly once the repo and DNS are configured

## GitHub Pages Setup
1. Push the static site files to the default branch.
2. In the repository settings, open `Pages`.
3. Set the build and deployment source to deploy from a branch.
4. Select the default branch and the `/ (root)` folder.
5. Save the Pages configuration.
6. In the custom domain field, enter `nodesnodesnodes.com`.
7. Enable HTTPS after the domain is validated.
8. Commit a `CNAME` file at the repo root containing `nodesnodesnodes.com`.

Recommended safety step:
- verify the custom domain in GitHub before or alongside attaching it to Pages to reduce takeover risk

Reference:
- [GitHub Pages custom domains](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)
- [Managing a custom domain for GitHub Pages](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

## Cloudflare DNS Setup
Use the GitHub-documented apex records instead of relying on apex CNAME flattening.

Create these records for the apex domain `nodesnodesnodes.com`:

| Type | Name | Value |
| --- | --- | --- |
| `A` | `@` | `185.199.108.153` |
| `A` | `@` | `185.199.109.153` |
| `A` | `@` | `185.199.110.153` |
| `A` | `@` | `185.199.111.153` |
| `AAAA` | `@` | `2606:50c0:8000::153` |
| `AAAA` | `@` | `2606:50c0:8001::153` |
| `AAAA` | `@` | `2606:50c0:8002::153` |
| `AAAA` | `@` | `2606:50c0:8003::153` |

Create this record for the `www` variant:

| Type | Name | Value |
| --- | --- | --- |
| `CNAME` | `www` | `<github-pages-default-domain>` |

For the `www` target:
- use the GitHub Pages default domain for this repo, such as `<owner>.github.io`
- point the CNAME directly at the GitHub Pages host, not at the custom domain

Cloudflare notes:
- avoid wildcard DNS records
- keep the DNS setup simple and explicit for the first launch
- if Cloudflare proxying creates validation trouble during setup, temporarily switch the records to `DNS only` until the domain is live

Reference:
- [Cloudflare CNAME flattening docs](https://developers.cloudflare.com/dns/cname-flattening/)

## `CNAME` File
The root `CNAME` file should contain exactly:

```text
nodesnodesnodes.com
```

## Verification Checklist
After DNS and Pages are configured, verify:
- `https://nodesnodesnodes.com` resolves to the GitHub Pages site
- `https://www.nodesnodesnodes.com` redirects to the chosen canonical domain
- GitHub Pages shows the custom domain as attached
- HTTPS is enabled in the Pages settings
- the `CNAME` file remains committed at the repo root
- each public route resolves:
  - `/`
  - `/product/`
  - `/workflow/`
  - `/download/`
  - `/faq/`
  - `/privacy/`

## Placeholder CTA Handling
Because there is no waitlist backend yet and the alpha is still early:
- `Join the waitlist` should point to an internal placeholder section or page state, not a form submit
- `Download the alpha` should point to `/download/` once the site exists
- `/download/` should clearly hand users to the GitHub repo as the current early-alpha source of truth

## Future Upgrade Path
When the site grows beyond a few static pages, the next acceptable upgrade is a static generator. Until then, keep the site as plain files so GitHub Pages remains trivial to operate.
