# Ludora site

Public pages for the Ludora app, served by GitHub Pages at <https://acem702.github.io/ludora/>:

- `index.html`: home, download link, features, FAQ and support contact
- `privacy.html`: privacy policy (the App Store and Play Console privacy URL)
- `terms.html`: terms of use
- `delete-account.html`: account deletion (the Play Console "delete account" URL). It signs in to the game server and calls `DELETE /api/me`, the same check the app uses.
- `robots.txt`, `sitemap.xml`: crawler directives and the URL list
- `og.jpg`: the 1200×630 social share card referenced by the Open Graph tags

Plain HTML and one stylesheet, no build step. Edit a page, push to `main`, and Pages republishes in a minute or two. When a policy changes, update its "Effective" date.

## Store link

Google Play: <https://play.google.com/store/apps/details?id=com.acem702.ludora>

It appears in the header nav, the hero (the official Google Play badge, hotlinked from
`play.google.com`, which falls back to a plain button if that image can't load), a second
button below the feature list, and the footer of every page.

## SEO

Each page carries a unique `<title>` and meta description, a `<link rel="canonical">`,
`robots`, Open Graph and Twitter card tags. The home page also carries JSON-LD
(`WebSite`, `Organization`, `MobileApplication`/`VideoGame` and `FAQPage`) whose claims
mirror the visible copy — keep the two in step when either changes.

**Absolute URLs are hardcoded** as `https://acem702.github.io/ludora/`. If the site ever
moves to a custom domain, update the canonical, `og:url`, `og:image`, `twitter:image` and
JSON-LD `@id`/`url` values in all four pages, plus `robots.txt` and `sitemap.xml`.

After deploying, submit `sitemap.xml` in Google Search Console and re-scrape the home page
with the Facebook Sharing Debugger and the X Card Validator so the new share card is cached.

The game itself lives in the private `acem702/LudoPP` repo.
