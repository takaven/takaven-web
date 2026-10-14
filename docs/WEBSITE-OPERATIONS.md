# Website operations and source of truth

**Applies only to TAKAVEN's TeamFrame marketing website**, not the TeamFrame HR application. Last cross-checked against GitHub, Vercel deployment records, authoritative/public DNS and the live website: **2026-10-14**. All dates/SHAs and domain statuses below are checkpoints, not permanent facts.

## Authority / boundaries

| Subject | Controlling source |
| --- | --- |
| Marketing source and public assets | This repository `takaven/takaven-web`, `teamframe/` directory |
| Product features, legal/compliance boundaries and offer wording | `takaven/teamframe/TEAMFRAME_MANAGED_PEOPLE_OPS_SCOPE.md`, `TEAMFRAME_ACCESS_MODEL.md`, `docs/launch/DECISIONS.md` |
| Application production and customer-data activation | `takaven/teamframe/docs/operations/CURRENT-STATE.md`, `ENVIRONMENTS.md`, `MANUAL-ACTIONS.md` |
| Website hosting and domain | Verify live Vercel project and GoDaddy DNS; this document records only last-known checkpoints |
| Website enquiry privacy notice | `teamframe/privacy.html`; check wording against actual hosting/form vendors |

Do not transfer product source, customer records, credentials, or deployment settings here. The deleted predecessor `takaven/teamframe-site` is historical provenance only; do not recreate it or use its former README as active marketing or pricing authority.

## Hosting and routes

- Vercel account: `admin@takaven.com`; team: `takaven` (`team_cXj0JaXqYVDGppqmiqNXIxVg`).
- Vercel project: `takaven-web` (`prj_d0VTmOdVmnB6Di3S99fjPea7V5mz`).
- Git source: `takaven/takaven-web`, `main`.
- Folder: `teamframe/`; `vercel.json` redirects the marketing root `/` to `/teamframe/` with HTTP 307 rather than serving a separate company homepage.
- Current Production deployment checkpoint: `main` commit `69b9e16685bf21e66db89d1636f6636ad7952583`, Vercel state `READY` (documentation-only reconciliation). Last behaviour-changing website baseline: `56f9184b04caf5a816718a8f1318b8fbfbf99d62`.
- Live public routes: `https://www.takaven.com/teamframe/` and `https://www.takaven.com/teamframe/privacy.html`; `https://www.takaven.com/` redirects to `/teamframe/`.
- Domain checkpoint: Vercel reports `www.takaven.com` verified. Authoritative GoDaddy nameservers, Google DNS, Cloudflare DNS and the local resolver returned `www.takaven.com CNAME 10074f97bb5aebf8.vercel-dns-017.com` on 2026-10-13. The `_vercel.takaven.com` ownership TXT record and a valid HTTPS certificate for `www.takaven.com` were present.
- Apex boundary: `takaven.com` is not attached to `takaven-web`; it remains on the separate GoDaddy apex configuration. An auditor must evaluate the TeamFrame marketing site at `www.takaven.com`, not assume apex and `www` are the same deployment.
- The apex `takaven.com` remains outside this Vercel project and continued serving its separate GoDaddy-hosted page at the publication check.

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

## Retired predecessor

The founder confirmed deletion of `takaven/teamframe-site` after the website, application and portfolio source references were reconciled. The review and retained-value record remains in [LEGACY-CONSOLIDATION.md](LEGACY-CONSOLIDATION.md); the deleted repository is not a fallback deployment or source.
