# Independent audit handoff — TeamFrame website

**Purpose:** navigation and evidence map for an independent reviewer. This file does **not** replace the canonical documents named below and must not be used as a second status tracker.

**Snapshot date:** 2026-10-14.

## Review scope

The TeamFrame commercial website and the TeamFrame HR application are separate systems:

| Area | Canonical source | Operational authority |
| --- | --- | --- |
| Public marketing website | `takaven/takaven-web` | This repo's `README.md` and `docs/WEBSITE-OPERATIONS.md` |
| HR product application | `takaven/teamframe` | `docs/operations/CURRENT-STATE.md`, `ENVIRONMENTS.md`, `MANUAL-ACTIONS.md`, `DEPLOYMENT.md` |
| Product/commercial claims | `takaven/teamframe` | `TEAMFRAME_MANAGED_PEOPLE_OPS_SCOPE.md`, `TEAMFRAME_ACCESS_MODEL.md`, `docs/launch/DECISIONS.md` |
| Portfolio/source governance | `takaven/product-portfolio` | `PORTFOLIO.yaml` |

Do not infer application readiness, customer-data authority or legal/compliance coverage from marketing copy.

## Website evidence checkpoint

- GitHub repository: `takaven/takaven-web`, protected/current branch `main`.
- Current verified Vercel Production deployment at preparation time: `69b9e16685bf21e66db89d1636f6636ad7952583`, state `READY`.
- Last behaviour-changing website baseline: `56f9184b04caf5a816718a8f1318b8fbfbf99d62` (root redirect to `/teamframe/`).
- Vercel project: `takaven-web`, ID `prj_d0VTmOdVmnB6Di3S99fjPea7V5mz`, Takaven team under `admin@takaven.com`.
- Canonical public URL: `https://www.takaven.com/teamframe/`.
- `https://www.takaven.com/` redirects to `/teamframe/`.
- Vercel reports `www.takaven.com` verified.
- Privacy route: `/teamframe/privacy.html`.
- `Component.FORM_ENDPOINT = null`: the web form is intentionally not a live lead-ingestion endpoint. The supported contact fallback is `admin@takaven.com`.
- The bare apex `takaven.com` is **not** part of the `takaven-web` Vercel project; do not use it as evidence for the `www` deployment.
- The predecessor repository `takaven/teamframe-site` was deleted after source reconciliation; GitHub now returns 404 for it. Its reviewed value is preserved in `docs/LEGACY-CONSOLIDATION.md`.

## Application evidence checkpoint

The website does not change the application release boundary. At this snapshot, the TeamFrame application correction workstream for the six independently identified defects was closed through application PRs #30 and #31. The application repository remains feature-frozen except for production defects, first-customer blockers, repeated customer evidence or separately approved bounded work.

An auditor should read the current `takaven/teamframe` `main` rather than rely on a SHA copied here, then start with `docs/operations/CURRENT-STATE.md`.

## What to verify independently

1. Source ownership and separation among website, application and portfolio repositories.
2. Live `www` route, root redirect, privacy route, assets, navigation and HR Setup Check.
3. Whether public claims match the controlling TeamFrame commercial/product documents.
4. Form truthfulness: no false successful online submission while `FORM_ENDPOINT` is unset.
5. Domain separation: `www.takaven.com` versus apex `takaven.com`; no impact to `app.takaven.com` or email DNS.
6. No secrets, customer records or employee data in the public marketing repository.
7. Historical source references are clearly labelled as provenance and cannot override current authorities.

## Known intentional limitations

- No live online enquiry backend; email fallback only.
- No public numeric pricing on this website release.
- The marketing website is not the HR application and contains no employee/customer HR database.
- Real-customer data activation for the HR application remains separately gated.

If live provider state differs from this dated snapshot, treat the live provider state plus the canonical operational document as authoritative and report the discrepancy rather than silently reconciling it.
