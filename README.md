# LocalExposure Sites

Monorepo for all LocalExposure web properties. One folder per site.

## Structure

```
agency-site/     -> localexposure.co.za (this agency's own marketing site)
clients/
  <client-slug>/  -> one folder per client lead-gen site
```

## Adding a new client site

1. `mkdir clients/<client-slug>`
2. Add the client's `index.html` (and any assets) into that folder
3. `git add clients/<client-slug>`
4. `git commit -m "Add <client-slug> site"`
5. `git push`
6. In Cloudflare Pages, create a new Pages project pointing at this repo,
   set "Root directory" to `clients/<client-slug>`, deploy.

Each site is its own Cloudflare Pages project even though they share this repo.
Cloudflare only rebuilds/redeploys the project whose root directory had files change.
