# Ludora site

Public pages for the Ludora app, served by GitHub Pages:

- `index.html`: home and support contact
- `privacy.html`: privacy policy (the App Store and Play Console privacy URL)
- `terms.html`: terms of use
- `delete-account.html`: account deletion (the Play Console "delete account" URL). It signs in to the game server and calls `DELETE /api/me`, the same check the app uses.

Plain HTML and one stylesheet, no build step. Edit a page, push to `main`, and Pages republishes in a minute or two. When a policy changes, update its "Effective" date.

The game itself lives in the private `acem702/LudoPP` repo.
