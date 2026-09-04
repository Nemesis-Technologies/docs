# Nemesis Docs

Public customer docs for **Nemesis** (Mintlify). This repo is the Admin / ISSO / contractor DBA surface for [NMS-88](https://linear.app/nemesistech/issue/NMS-88/admin-and-isso-documentation-set).

It is **not** the internal engineer handbook (`docs-internal`). It is **not** the home for portal runbooks — those stay in `portal` and are cited by path.

## Honesty

- **Not production-ready.**
- **CUI never.**
- **Postgres-first** (STIG Postgres 16). Do not invent full multi-engine coverage.
- No FedRAMP / CMMC PASS / certified claims.
- No DSN in examples. No passwords in SQL sketches.

## Preview locally

Install the [Mintlify CLI](https://www.mintlify.com/docs/installation), then from this repo root:

```bash
npx mint dev
```

Open the URL the CLI prints (usually `http://localhost:3000`).

Validate the site config and pages:

```bash
npx mint validate
```

Mintlify hosted preview (after this repo is connected in the Mintlify dashboard) is the intended customer check. A thin `mint validate` workflow may run on pull requests; a green check is **not** a product certification.

## Site map

| Page | Path |
| --- | --- |
| Start here | `index.mdx` |
| First-scan path map | `first-scan/overview.mdx` |
| Install | `first-scan/install.mdx` |
| Add target | `first-scan/add-target.mdx` |
| First scan | `first-scan/run-scan.mdx` |
| Export CKL | `first-scan/export-ckl.mdx` |
| Waivers | `first-scan/waivers.mdx` |
| Architecture for reviewer | `architecture/for-reviewer.mdx` |

## Branding

Favicon uses the same mark as the internal handbook (`docs-internal` `favicon.svg`), redrawn as SVG here. Site name in the navbar is the wordmark until a licensed marketing logo is published.

## Sources of truth

Cited against portal `main` tip `8daddb089a0785b3beead9b0dd309e053acfdbfd` (confirm HEAD if you are reading later):

- Lab compose install: `apps/self-hosted/LAB-INSTALL.md`
- Helm / n-1 notes: `apps/self-hosted/HELM-INSTALL.md`
- Least-priv classify role: `docs/runbooks/nms-classify-sample-lab-role.md` and `.sql`
- CKL export design: `docs/ADR-0035-ckl-portal-export.md`
- Waivers / POA&M: `docs/ADR-0014-poam-waiver.md`

Do not relocate those portal files here.
