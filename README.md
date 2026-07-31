# Neko — support site

Static support site for the **Neko** iOS app, providing the two URLs App Store Connect requires:

| App Store Connect field | Page |
|---|---|
| Support URL | `index.html` |
| Privacy Policy URL | `privacy.html` |
| EULA / Terms (optional) | `terms.html` |

No build step, no dependencies — plain HTML + one stylesheet.

```
index.html      Support home: quick start, what's supported, FAQ, contact
privacy.html    Privacy Policy
terms.html      Terms of Use (custom EULA)
assets/
  style.css     Shared styles (light + dark, responsive)
  favicon.png   180px app icon
  neko-icon-256.png / neko-icon-1024.png
.nojekyll       Serve files as-is on GitHub Pages
```

## Current details

| Field | Value |
|---|---|
| Support address | `support@starhubinformation.info` (all three pages) |
| Developer name | **StarHub Information** (`privacy.html` §1) |
| Governing law | **Hong Kong SAR** (`terms.html` §12) |

No placeholders remain. Two things to confirm before submitting to App Store review:

1. The support mailbox is real and monitored — review checks the Support URL.
2. The developer name matches the seller name shown on your App Store listing.

**These documents are drafts written to describe what the app actually does — they are not legal
advice.** Have them reviewed before you rely on them, especially the liability and governing-law
clauses.

## Deploy with GitHub Pages

1. Push to `main`.
2. Repository **Settings → Pages** → *Source*: **Deploy from a branch** → branch `main`, folder `/ (root)`.
3. The site appears at `https://starhubinfo.github.io/neko/`.

All internal links are **relative**, so the site works from a project subpath as well as from a custom
domain. To use a custom domain, add a `CNAME` file containing the domain and configure DNS.

## Keeping it accurate

The FAQ and the privacy disclosures describe real app behaviour (supported protocols and subscription
formats, the connectivity-check endpoint, the DNS resolvers the bundled kernel uses, and what is stored
on device). If any of that changes in the app, update these pages to match.
