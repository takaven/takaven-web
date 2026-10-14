# TAKAVEN marketing website — TeamFrame

**Canonical website source:** [`takaven/takaven-web`](https://github.com/takaven/takaven-web), branch `main`. **Not** the TeamFrame HR application source.

The current published deployment is the Vercel project `takaven-web` in the **Takaven** Vercel team under `admin@takaven.com` (project ID `prj_d0VTmOdVmnB6Di3S99fjPea7V5mz`). The TeamFrame public site is live at `https://www.takaven.com/teamframe/`, served from the `teamframe/` directory. Production is Git-connected to this repository's `main`. Vercel Production was re-verified `READY` on 14 October 2026 after documentation reconciliation. The last behaviour-changing publication baseline is `56f9184b04caf5a816718a8f1318b8fbfbf99d62`, verified for the root redirect, HTTPS, privacy page, navigation and HR Setup Check. Read the live `main` head rather than treating a documentation-only SHA as permanent state.

The **product application** is `takaven/teamframe`, served separately from `https://app.takaven.com` on Vercel `teamframe-production`. Its code, authentication, Supabase, deployment and customer-data approval gates are distinct from this static marketing site. Do not connect this repository to the product application's Vercel project.

## What is in this repository

- `teamframe/index.html`: approved marketing landing page, product explorer, HR Setup Check and demo/enquiry UI.
- `teamframe/privacy.html`: website-enquiry privacy notice. **Not** the application/customer HR-data privacy policy.
- `teamframe/support.js`: the existing page runtime; do not replace it merely to make the documentation cleaner.
- `teamframe/uploads/`: local marketing images and logos.
- [`docs/WEBSITE-OPERATIONS.md`](docs/WEBSITE-OPERATIONS.md): hosting, configuration, verification and ownership.
- [`docs/AUDIT-HANDOFF.md`](docs/AUDIT-HANDOFF.md): independent-review entry point and evidence map; navigation only, not a competing source of truth.
- [`docs/LEGACY-CONSOLIDATION.md`](docs/LEGACY-CONSOLIDATION.md): reviewed predecessor website and what was retained or intentionally not copied.
- [`AGENTS.md`](AGENTS.md): short source-control and documentation discipline.

This is a static marketing site. It does not deploy the HR product and has no database of employee records.

## Commercial-content authority

The controlling current product and commercial scope is in [`takaven/teamframe/TEAMFRAME_MANAGED_PEOPLE_OPS_SCOPE.md`](https://github.com/takaven/teamframe/blob/main/TEAMFRAME_MANAGED_PEOPLE_OPS_SCOPE.md), [`TEAMFRAME_ACCESS_MODEL.md`](https://github.com/takaven/teamframe/blob/main/TEAMFRAME_ACCESS_MODEL.md) and its [`docs/launch/DECISIONS.md`](https://github.com/takaven/teamframe/blob/main/docs/launch/DECISIONS.md). **Verify the current versions before changing marketing claims.** The site's website privacy notice and marketing copy are not authority for actual product functionality, legal advice or customer deployment readiness.

Two customer starting points: TeamFrame tool/implementation, or TeamFrame + HR Foundation Setup, with optional TeamFrame HR Support separately scoped. The software is sold as a one-off purchase and the customer controls/pays for infrastructure. **No public price figure is displayed in this website release.** Historical price figures in the predecessor repository and portfolio need commercial validation before being republished; this source-consolidation does not change prices or contract terms.

The predecessor `takaven/teamframe-site` used to be documented as canonical. The website, application and portfolio source references were reconciled, and the founder subsequently deleted that predecessor repository. Its reviewed history is summarised in [`docs/LEGACY-CONSOLIDATION.md`](docs/LEGACY-CONSOLIDATION.md); it is not an active or recoverable source. Never confuse it with or delete the product application repository `takaven/teamframe`.

## Publication checkpoint (verified 2026-10-13; reconciled 2026-10-14)

- Production source: `takaven/takaven-web` `main`; Vercel Production verified `READY` on 2026-10-14. Behaviour-changing website baseline: `56f9184b04caf5a816718a8f1318b8fbfbf99d62`. Re-read current `main` for the latest documentation-only head.
- Public routes: `https://www.takaven.com/` redirects with HTTP 307 to `/teamframe/`; `/teamframe/` and `/teamframe/privacy.html` return successfully.
- Custom domain: Vercel reports `www.takaven.com` verified; authoritative GoDaddy DNS/public resolver verification recorded `www.takaven.com CNAME 10074f97bb5aebf8.vercel-dns-017.com`, with the Vercel ownership TXT record and HTTPS active. The bare apex `takaven.com` is intentionally not attached to this Vercel project and remains outside the TeamFrame marketing deployment.
- Browser verification: navigation, product-area interaction and the complete seven-question HR Setup Check passed; required images and scripts loaded without page console errors.
- `Component.FORM_ENDPOINT`: `null`; online form submission is deliberately inactive. **Direct email alternative:** `admin@takaven.com`. Do not claim submitted enquiries are delivered via the form until a real provider and end-to-end receipt test exist.
- Privacy notice: `/teamframe/privacy.html`.
- Predecessor repository: `takaven/teamframe-site` was deleted by the founder after reconciliation completed.
- No pricing, production-application release, real-customer data, or GoDaddy DNS changes are authorised by documentation updates alone.

Review [operations](docs/WEBSITE-OPERATIONS.md) before deployment or domain changes.
