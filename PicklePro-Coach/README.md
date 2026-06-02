# PicklePro Coach Platform

A React/Vite + Express/MongoDB marketplace for pickleball coaching video reviews.

Players can browse coaches, buy video-review packages, upload footage, and view completed feedback. Coaches can create profiles, connect payouts, create packages, review submitted videos, and add timestamped coaching notes. Admins can approve coaches, monitor submissions, and audit payment splits.

## Main routes

- `/` — Pickleball coaching landing page
- `/coaches` — Coach marketplace
- `/coaches/:id` — Coach profile and package booking
- `/coach-signup` — Coach onboarding/application
- `/dashboard/submissions` — Player video submissions
- `/dashboard/submissions/:id` — Player submission detail and completed review
- `/coach/dashboard` — Coach dashboard
- `/coach/submissions/:id/review` — Coach review workspace
- `/admin/coaching` — Admin coaching marketplace controls

## Setup

```bash
npm install
npm install --prefix server
```

Create `.env` from `.env.example` and `server/.env` from `server/.env.example`.

## Run locally

Terminal 1:

```bash
npm run dev
```

Terminal 2:

```bash
npm run dev --prefix server
```

## Build

```bash
npm run build
```

## Demo mode

The app works without Stripe or Cloudflare credentials. Without those keys, payment and video upload flows use local demo fallbacks so you can test the full workflow immediately.

## Production integrations

For real payments, set `STRIPE_SECRET_KEY` and connect coach accounts through `/coach/dashboard`.

For direct video uploads, set `CLOUDFLARE_ACCOUNT_ID` and `CLOUDFLARE_STREAM_TOKEN`.

See `PICKLEBALL_COACHING_UPDATES.md` for the full update list.
