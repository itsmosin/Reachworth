# Reachworth — The business behind influence

Static site built from the Gaply Media implementation brief: an Index-first homepage (Creators / Companies), company and creator profiles, Stories, Tools ("How much is your reach worth?"), Events, the Reachworth Weekly newsletter page, and About, Methodology, Contact and Privacy pages.

## Deploy on Vercel
1. Push this folder to a GitHub repo.
2. Vercel → Add New → Project → Import the repo. Framework preset: **Other**. No build command; output directory `./`.
3. Deploy. Every push to `main` redeploys.

## Before launch
- **Data:** replace the `COMPANIES`, `CREATORS`, `PEOPLE`, `STORIES`, `ISSUES` and `EVENTS` arrays with verified records, then set `SAMPLE_DATA = false`.
- **Tool rates:** replace `RATES` and `NICHE_MULT` with sourced benchmark ranges.
- **Forms:** all forms are handled in the `submit` listener; connect them to your email platform, CMS review queue and the separate Gaply CRM.
- **Analytics:** `track()` pushes events (with UTM tags) to `window.dataLayer`; wire it to your analytics.
- **Domain:** `BASE_URL` is set to the pending `reachworth.com`.
- **Routing:** pages use hash URLs (`#company-crumbwell`). For SEO, move to real paths (`/companies/crumbwell`) when you put this into a CMS or framework.
