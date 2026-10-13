# Website operations and source of truth

**Applies only to TAKAVEN's TeamFrame marketing website**, not the TeamFrame HR application. Last cross-checked against GitHub and Vercel reports: **2026-10-13**. All dates/SHAs and domain statuses below are checkpoints, not permanent facts.

## Authority / boundaries

| Subject | Controlling source |
| --- | --- |
| Marketing source and public assets | This repository `takaven/takaven-web`, `teamframe/` directory |
| Product features, legal/compliance boundaries and offer wording | `takaven/teamframe/TEAMFRAME_MANAGED_PEOPLE_OPS_SCOPE.md`, `TEAMFRAME_ACCESS_MODEL.md`, `docs/launch/DECISIONS.md` |
| Application production and customer-data activation | `takaven/teamframe/docs/operations/CURRENT-STATE.md`, `ENVIRONMENTS.md`, `MANUAL-ACTIONS.md` |
| Website hosting and domain | Verify live Vercel project and GoDaddy DNS; this document records only last-known checkpoints |
| Website enquiry privacy notice | `teamframe/privacy.html`; check wording against actual hosting/form vendors |

Do not transfer product source, customer records, credentials, or deployment settings here. Do not use the old `takaven/teamframe-site` README as active marketing or pricing authority.

## Hosting and routes

- Vercel account: `admin@takaven.com`; team: `takaven` (`team_cXj0JaXqYVDGppqmiqNXIxVg`).
- Vercel project: `takaven-web` (`prj_d0VTmOdVmnB6Di3S99fjPea7V5mz`).
- Git source: `takaven/takaven-web`, `main`.
- Folder: `teamframe/` (the marketing repository root has **no** company homepage yet).
- Preview/checkpoint: `https://takaven-web-gamma.vercel.app/teamframe/` and `/teamframe/privacy.html` reported working 2026-10-13.
- Intended public routes: `https://www.takaven.com/teamframe/` and `https://www.takaven.com/teamframe/privacy.html`.
- As of 2026-10-13, apex `takaven.com` was removed from this project, `www.takaven.com` required domain verification, and the old GoDaddy DNS had `CNAME www -> takaven.com`. **No claim is made here that DNS is switched.** Confirm current provider state before writing.

**Do not edit:** `app.takaven.com`, `teamframe-production`, the apex DNS, Microsoft 365 MX/SPF/DKIM/DMARC, Resend mail records, or unrelated services as part of a marketing deployment. Changing `www` may replace the existing apex-served/GoDaddy webpage; inspect the actual page and confirm disposition first.

## Marketing functionality

- The existing HR Setup Check is a self-guided, anonymous assessment; completing it need not reveal identity. Do not call its recommendation a legal or compliance determination.
- `Component.FORM_ENDPOINT = null` in `teamframe/index.html` at this checkpoint. The form is not a working lead-ingestion system until a real HTTPS endpoint and end-to-end test are verified. The displayed `admin@takaven.com` mailto fallback remains the supported customer contact path.
- `Component.PRIVACY_URL = '/teamframe/privacy.html'`. Footer and contact links must resolve.
- Static HTML carries title, description, Open Graph and canonical URL. The full page uses `support.js`/JavaScript runtime; the standalone offline bundle is **not** the SEO deployment source.
- Avoid editing the website's approved sections, images, HR Setup Check and 48-hour handover message unless a verified mismatch with the controlling product docs requires a bounded change.

## Release steps

1. Compare proposed changes against the current repository `main` and controlling product commercial/operations documents, **not** an old README or asset export.
2. Create a small PR; state changed routes, commercial copy, any assets and whether the change touches sensitive data or a provider. For public copy, review legal/product boundary carefully.
3. Test direct routes (`/teamframe/`, `/teamframe/privacy.html`), image/script paths, desktop/mobile, product explorer, assessment, privacy and email alternative. Check no secret or unsupported product claims.
4. Merge only after review. Vercel is Git-connected, so even an HTML/docs-only merge can trigger a new Production deployment; verify the resulting deployment and return-code/content.
5. Treat domain reassignment, live form service activation and any spend as separate, explicitly approved provider actions.
6. Update **both** this repo's dated checkpoint and `takaven/teamframe` website reference for material changes; update the portfolio registry `takaven/product-portfolio/PORTFOLIO.yaml` if canonical source changes. Do not mechanically overwrite application production statuses.
7. Retire a predecessor repository only after its latest content and history are reviewed, current references corrected, and final deletion is explicitly authorised.

When information differs across documents, trust live GitHub/Vercel/provider facts for deployments and the current product commercial authority for claims. Record a dated resolution; do not copy stale wording forward.
