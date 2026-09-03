# The Loot Table — site

Static GitHub Pages site for the show. Three jobs:

- `index.html` — landing page with links to the show's accounts
- `privacy.html`, `terms.html` — the policy URLs required by the TikTok, Meta and Google developer consoles
- `callback.html` — a blank https landing page for OAuth redirects (TikTok's portal insists on https)

## Publish

```
gh repo create loot-table-site --public --source=. --push
gh api -X POST repos/OWNER/loot-table-site/pages -f "source[branch]=main" -f "source[path]=/"
```

Pages then serves at `https://OWNER.github.io/loot-table-site/`. Use these in the developer consoles:

| Field | URL |
|---|---|
| Terms of Service | `https://OWNER.github.io/loot-table-site/terms.html` |
| Privacy Policy | `https://OWNER.github.io/loot-table-site/privacy.html` |
| TikTok Login Kit redirect URI | `https://OWNER.github.io/loot-table-site/callback.html` |

Contact email on the policy pages is loottablepodcast@gmail.com. Fill the three account links in `index.html` once the handles exist.
