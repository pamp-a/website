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

```bash
bun run deploy
```

The Worker is called `pampa-website` (see `wrangler.jsonc`). The first deploy
asks you to log in with `bunx wrangler login`.
