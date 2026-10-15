# le-gigi-playground

A static website served by [Cloudflare Workers static assets](https://developers.cloudflare.com/workers/static-assets/). Site files live in `public/`.

## Local development

```bash
npm install
npm run dev
```

Then open http://localhost:8787.

## Deployment

Every push to `main` deploys via GitHub Actions (`.github/workflows/deploy.yml`). It can also be run manually from the Actions tab.

Required repository secrets (Settings → Secrets and variables → Actions):

- `CLOUDFLARE_API_TOKEN` — create one from the "Edit Cloudflare Workers" template in the Cloudflare dashboard.
- `CLOUDFLARE_ACCOUNT_ID` — shown on the Workers & Pages overview page.

To deploy from your machine instead: `npx wrangler login` then `npm run deploy`.
