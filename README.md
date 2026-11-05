# <FWD> — Horde, WoW Forever

Static World of Warcraft guild recruitment site for [Nyte-fyre/FWD](https://github.com/Nyte-fyre/FWD).

**Live URL (after Pages is on):** https://nyte-fyre.github.io/FWD/

## Fill in your guild

Edit [`js/config.js`](js/config.js) — guild name, realm, raid teams and times (Eastern), values, rules, loot, recruitment, officers, Discord invite, and the apply-form webhook. Then commit and push. You do not need to edit `index.html` for those fields.

The apply form posts to the guild bot Worker set in `applyEndpoint` (a separate project, which also runs the Discord `/apply` command). The Worker holds the Discord webhook as a secret and posts the application. While `applyEndpoint` is empty, the form is disabled and points people to #apply-here.

## Local preview

Open `index.html` in a browser, or from this folder:

```powershell
python -m http.server 8080
```

Then visit http://localhost:8080/

## GitHub Pages

Pushes to `main` run a GitHub Action that publishes the repo root. First deploy can take a minute.
