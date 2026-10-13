# Predecessor commercial website review (2026-10-13)

**Read-only predecessor:** [`takaven/teamframe-site`](https://github.com/takaven/teamframe-site), `main`. **Replacement marketing repository:** `takaven/takaven-web`. This record does not authorise deletion of the predecessor or alter the product application's source.

## What was inspected

The old website's `README.md`, `index.html`, `site.js`, `styles.css`, `package.json`, `scripts/build.mjs`, repository tree, marketing image list and `.env.example` were reviewed against the new site's `teamframe/index.html`, assets, privacy page and the current TeamFrame application's product/commercial authority. The predecessor was a functioning separate static build (generating `dist/`), **not** just a placeholder. Its README expressly named itself canonical; that statement must no longer control once reconciled.

## Material value retained

| Finding in predecessor | Treatment in new site |
| --- | --- |
| Per-customer dedicated installation, hosting and data control | Integrated into existing `Implemented for your company` copy and one-off commercial paragraph; supported by current TeamFrame access model |
| One-off purchase, provider costs separate, optional support | Integrated into existing offers follow-up. **No numeric price added to public marketing** because the current site intentionally does not publish figures |
| Role-separated salary and private-file access | Integrated as a concise evidence/control statement, consistent with the live access model |
| Evidence-backed actions, onboarding, policies and HR controls | Already covered by new Control Centre, product explorer and HR Setup Check |
| Authentic product screenshots | New site already contains accepted screenshots with broader coverage; old screenshots not copied, to avoid duplicate/out-of-date visual baselines |
| Simple configurable `mailto` walkthrough fallback | Already provided as `admin@takaven.com` on the new site. New online form remains disabled until an endpoint is tested |
| Direct control over the customer HR installation | Captured without promising legal compliance, payroll processing, or unapproved support service levels |

## Deliberately not copied

- Old hero `HR admin, owned once.`, old layout, duplicate CSS/JS/build scripts: superseded by the approved Claude Design website.
- Old `US$1,950` / `from US$3,450` on-page price blocks: commercial anchors appear in the older portfolio but do not automatically override the founder-approved new site with no public price figures. **No pricing change was approved by this consolidation.**
- Old reference to `NEXT_PUBLIC_TEAMFRAME_WALKTHROUGH_URL`: applies to the predecessor build, not to the new source. The new site uses the existing mailto fallback plus optional HTTPS `Component.FORM_ENDPOINT`.
- Old broad `Managed People Ops` terminology, universal compliance guarantees, payroll/WPS operation or unsupported performance-management claims: current TeamFrame product/commercial authority controls.

## Pre-deletion gate

Do **not** delete `takaven/teamframe-site` just because a new Vercel deployment exists. First ensure:
1. new website changes reviewed/merged and public deployment tested;
2. `takaven/teamframe` and `takaven/product-portfolio/PORTFOLIO.yaml` updated (including generated documents) to name `takaven/takaven-web` canonical;
3. any operational deployment references still pointing to the predecessor inspected;
4. owner confirms old repository is no longer needed; preserve any desired history/archive externally before explicit deletion.

No application database, Vercel product project, Supabase environment or DNS changes are included in this consolidation.
