# Jay's Home Page

Personal browser start page. Live at: **https://jmrphr.github.io/homepage/**

One page, one URL — every computer and phone pointed at it sees the same
shortcuts. The public page is read-only; changing it requires this GitHub
account's login (password + 2FA/passkey).

## How to change shortcuts

Each shortcut is one line in `index.html`:

```html
<a href="https://www.netflix.com">Netflix</a>
```

Groups are `<section>` blocks. Icons appear automatically from the site's
own favicon; no icon files to manage.

Two ways to edit:

1. **Ask Claude** on the home server — it edits, commits, and pushes.
   The live page updates about a minute after each push.
2. **On github.com** (any computer): open `index.html` in this repository,
   click the pencil icon, edit, and "Commit changes."

Rule for this page: links only — it is public, so nothing personal ever
goes in it (no URLs containing account numbers, no notes, no addresses).

## Setting up a new computer (Chrome)

1. Sign into Chrome with the Google account (syncs bookmarks/extensions).
2. **Home button:** Settings → Appearance → *Show home button* →
   enter `https://jmrphr.github.io/homepage/`
3. **Startup:** Settings → On startup → *Open a specific page* →
   add the same URL.
4. **New tabs & new windows:** install the extension **New Tab Redirect**
   *by Jim Schubert* (the ~700k-user one with the Featured badge —
   https://chromewebstore.google.com/detail/new-tab-redirect/icpgjfneehieebagbmdbhnlpiopdcmna ),
   then in its options set the redirect URL to the same address.
   At install, the only permission it should request is replacing the
   new-tab page — anything asking for "all your data on all websites"
   is the wrong extension.

## iPhone (Chrome)

- Open the URL → share icon → **Add to Bookmarks** (and optionally
  **Add to Home Screen** for a one-tap icon).
- The desktop bookmarks bar is also available on iPhone under
  ⋯ → Bookmarks → Bookmarks Bar.

## Plumbing (for future reference)

- Repo lives on the home server at `~/claude/homepage/` (branch `master`);
  GitHub Pages serves the branch root, deploys ~1 minute after each push.
- The server is logged into GitHub as `jmrphr` via the `gh` CLI
  (`~/bin/gh`), so pushes need no password.
- House Cam tile: UniFi Protect at the gateway; browser shows a one-time
  self-signed-certificate warning — Advanced → Proceed. Home-group tiles
  only connect from home Wi-Fi.
