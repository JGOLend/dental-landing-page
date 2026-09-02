# JGO Lending - dental equipment finance landing page

The Meta-traffic landing page for the JGO Lending dental equipment finance
campaign. Serves at `https://dental.jgolending.com.au`.

## Layout

```
dental/index.html    The page. One self-contained file, all CSS and JS inline.
dental/assets/        Images: JGO logo, James's portrait, the practice photo.
wrangler.jsonc         Cloudflare Worker config (static assets, custom domain).
```

No build step, no package manager, no framework - the page deploys as-is.

## Deploying

Connected to Cloudflare Workers Builds: every push to `main` redeploys
automatically. No manual `wrangler deploy` needed once the GitHub connection
is set up in the Cloudflare dashboard.

## Configuration

- Meta Pixel ID and the Web3Forms access key are both public-by-design and
  live directly in `dental/index.html` - shared with the veterans and dev
  finance landing pages.
- The custom domain (`dental.jgolending.com.au`) is added under the
  Worker's Settings > Domains & Routes in the Cloudflare dashboard, which
  also provisions DNS and the certificate automatically (the zone is
  already on this Cloudflare account).
