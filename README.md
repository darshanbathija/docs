# Glide docs

The source for [glide.co/docs](https://glide.co/docs). Built on Mintlify; proxied from `glide.co/docs/*` to the Mintlify deployment via Next.js rewrites in the main `glide.co` repo.

## Structure

- `docs.json` &mdash; site config, navigation, branding.
- `index.mdx` &mdash; landing page.
- `quickstart.mdx` &mdash; "open your account in 10 minutes."
- `accounts/`, `money/`, `cards/`, `stablecoins/` &mdash; consumer-facing product docs.
- `agents/` &mdash; agent banking (skills, policy envelope, step-up, receipts).
- `business/` &mdash; multi-entity, team, payroll, treasury, vendor payments.
- `security/` &mdash; segregated banking, regulatory, KYC/AML, two-factor, privacy.

## Local preview

Install the Mintlify CLI:

```bash
npm install -g mint
```

Then from the repo root:

```bash
mint dev
```

The local preview runs at `http://localhost:3000`.

## Editing

- Mintlify uses MDX. Standard markdown plus components (`<Card>`, `<CardGroup>`, `<Steps>`, `<Step>`, `<Tip>`, `<Warning>`).
- Brand voice: confident, declarative, banker-clean. Not crypto-bro.
- Visual brand: dark-only, Mysteria Purple background, Lavender Glow accent. See `DESIGN.md` in the main repo.
- Cross-references use site-relative paths (`/agents/quickstart`, `/cards/overview`). Mintlify rewrites these correctly when proxied at `glide.co/docs/*`.

## Deploy

Auto-deployed by Mintlify on push to `main`. The proxy at `glide.co/docs/*` is configured in `apps/web/next.config.js` of the main repo.
