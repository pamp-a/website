# pamp.a website

Home page of pamp.a, architecture, paris.lausanne. One static page served by a
Cloudflare Worker with static assets. There is no Worker script.

The page is `public/index.html`: the contact block drifts like the old DVD
screensaver, bounces off the edges and takes a new colour at each hit. A click
on the block opens a mail to contact@pampatelier.eu.

## Run

```bash
bun install
bun run dev
```

## Deploy

Every push to `main` deploys through Workers Builds, to the Worker `website`
on the pamp.a Cloudflare account. The account is pinned in `wrangler.jsonc`.
The build installs Bun from the `BUN_VERSION` build variable in the dashboard
(Settings, Builds). Raise it when a newer Bun rewrites `bun.lock`.

To deploy by hand, log in to that account and run:

```bash
bun run deploy
```
