# Juggervault Partner API docs

Public documentation for `docs.juggervault.finance`. The site is Mintlify. Pages are MDX. Endpoint pages are generated from `openapi.yaml`.

Behavior follows `tokenization-backend` Partner API routes (`/api/partner/v1`). When those routes change, update this folder in the same change.

## Preview

Requires Node.js 20.17 or newer.

```bash
npm i -g mint
cd partner-docs
mint dev
```

Open `http://localhost:3000`.

## Publish

1. Create a Mintlify account and run `mint login`.
2. Connect this folder (or a repository that contains it) in the Mintlify dashboard. A push to the production branch deploys the site.
3. Add the custom domain `docs.juggervault.finance`.
4. At the DNS host for `juggervault.finance`, add the TXT records shown in the dashboard, then a CNAME from `docs` to `cname.mintlify.builders`.
5. After DNS resolves, confirm `https://docs.juggervault.finance` loads.

The API origin in examples is `https://api.juggervault.finance`. Use the origin issued with the broker API key if it differs. That hostname is separate from the docs domain.
