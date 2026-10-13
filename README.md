# TAKAVEN marketing website — TeamFrame

**Canonical website source:** [`takaven/takaven-web`](https://github.com/takaven/takaven-web), branch `main`. **Not** the TeamFrame HR application source.

The current published deployment is the Vercel project `takaven-web` in the **Takaven** Vercel team under `admin@takaven.com` (project ID `prj_d0VTmOdVmnB6Di3S99fjPea7V5mz`). The TeamFrame public site is intended for `https://www.takaven.com/teamframe/`, served from the `teamframe/` directory. The Vercel-generated deployment URL `https://takaven-web-gamma.vercel.app/teamframe/` was checked in Chrome on 13 October 2026. **The custom-domain/DNS verification was still pending at this checkpoint**; do not equate a successful Vercel deploy with the custom domain being live.

The **product application** is `takaven/teamframe`, served separately from `https://app.takaven.com` on Vercel `teamframe-production`. Its code, authentication, Supabase, deployment and customer-data approval gates are distinct from this static marketing site. Do not connect this repository to the product application's Vercel project.

## What is in this repository

- `teamframe/index.html`: approved marketing landing page, product explorer, HR Setup Check and demo/enquiry UI.
- `teamframe/privacy.html`: website-enquiry privacy notice. **Not** the application/customer HR-data privacy policy.
- `teamframe/support.js`: the existing page runtime; do not replace it merely to make the documentation cleaner.
- `teamframe/uploads/`: local marketing images and logos.
- [`docs/WEBSITE-OPERATIONS.md`](docs/WEBSITE-OPERATIONS.md): hosting, configuration, verification and ownership.
- [`docs/LEGACY-CONSOLIDATION.md`](docs/LEGACY-CONSOLIDATION.md): reviewed predecessor website and what was retained or intentionally not copied.
- [`AGENTS.md`](AGENTS.md): short source-control and documentation discipline.

This is a static marketing site. It does not deploy the HR product and has no database of employee records.

## Commercial-content authority

The controlling current product and commercial scope is in [`takaven/teamframe/TEAMFRAME_MANAGED_PEOPLE_OPS_SCOPE.md`](https://github.com/takaven/teamframe/blob/main/TEAMFRAME_MANAGED_PEOPLE_OPS_SCOPE.md), [`TEAMFRAME_ACCESS_MODEL.md`](https://github.com/takaven/teamframe/blob/main/TEAMFRAME_ACCESS_MODEL.md) and its [`docs/launch/DECISIONS.md`](https://github.com/takaven/teamframe/blob/main/docs/launch/DECISIONS.md). **Verify the current versions before changing marketing claims.** The site's website privacy notice and marketing copy are not authority for actual product functionality, legal advice or customer deployment readiness.

Two customer starting points: TeamFrame tool/implementation, or TeamFrame + HR Foundation Setup, with optional TeamFrame HR Support separately scoped. The software is sold as a one-off purchase and the customer controls/pays for infrastructure. **No public price figure is displayed in this website release.** Historical price figures in the predecessor repository and portfolio need commercial validation before being republished; this source-consolidation does not change prices or contract terms.

The predecessor `takaven/teamframe-site` used to be documented as canonical. It is superseded **for current website code** by this repository once this reconciliation is merged. Retain it read-only until the website, product and portfolio references are reconciled and its removal is separately confirmed. Never delete the product application repository `takaven/teamframe`.

## Launch checkpoint (2026-10-13)

- Vercel-generated deployment: reported **Ready**, pages and HR Setup Check checked in Chrome.
- Custom `www.takaven.com` mapping: **verification/DNS cutover pending**. The old `www` record points to the apex; avoid changing DNS from source code or assuming the root website is disposable.
- `Component.FORM_ENDPOINT`: `null`; online form submission is deliberately inactive. **Direct email alternative:** `admin@takaven.com`. Do not claim submitted enquiries are delivered via the form until a real provider and end-to-end receipt test exist.
- Privacy notice: `/teamframe/privacy.html`.
- No pricing, production-application release, real-customer data, or GoDaddy DNS changes are authorised by documentation updates alone.

Review [operations](docs/WEBSITE-OPERATIONS.md) before deployment or domain changes.
