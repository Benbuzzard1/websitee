# Lucent General Contractors LLC — Website Source

Exported from Lovable on 2026-11-03. This is the complete application source,
ready to run and host anywhere.

## What's in it

- `src/routes/` — one file per page: home (`index.tsx`), services list and
  per-service detail pages, portfolio, about, service areas, contact.
- `src/components/site/` — the header, footer, estimate form, gallery and
  call-to-action bands.
- `src/lib/site.ts` — single source of truth for the business details
  (phone, email, owner), the 10 services, the three service cities, the
  navigation and the FAQ answers. Edit this file to change copy site-wide.
- `src/styles.css` — the design tokens: Cormorant Garamond + Jost fonts,
  black `#111111`, gold `#D4AF37`, ivory, `#F7F7F7` background, and the
  button/rule/eyebrow utilities used across the pages.
- `src/assets/` — the logo, your three project photos, and three generated
  placeholder images (painted room, house exterior, paint-roller close-up).
- `public/` — favicon and robots.txt.

## Run it locally

You need Node.js 20+ and either Bun (recommended, `bun.lock` is included) or npm.

```sh
bun install        # or: npm install
bun run dev        # or: npm run dev
```

Then open the printed local URL (usually http://localhost:8080).

Other commands: `bun run build` (production build), `bun run preview`
(serve the build), `bun run lint`, `bun run test`.

## Hosting it elsewhere

This is a TanStack Start app, so it renders pages on a server — it is not a
plain static folder. The build (`vite build`) uses Nitro and defaults to a
Cloudflare Workers target. To deploy on another host, install the matching
Nitro preset (for example Node, Vercel or Netlify) and set its build and
output settings to match, or ask for help wiring that up.

## Before you go live

- **Estimate form**: it opens the visitor's email app with the details
  pre-filled and sends to JamesF@LucentContractors.com. There is no database
  behind it, and uploaded photos are not attached automatically. To collect
  submissions in a database instead, a backend needs to be added.
- **Scheduling**: the "Schedule" buttons dial 517-525-6241. If you have a
  Calendly or similar link, that is where it should point.
- **Photos**: the three generated images are stand-ins. Swap them for real
  project photos in `src/assets/`.
- **"Licensed & insured"** appears in several places — confirm that wording
  is accurate for your licensing before publishing.
- **Service area**: the site says Grand Rapids, Lansing and Traverse City plus
  nearby communities. The map is a generic Michigan view, not a street address.

## Stack

TanStack Start v1 (React 19, Vite 8, Nitro), TypeScript, Tailwind CSS v4,
shadcn/ui + Radix primitives, lucide-react icons.
