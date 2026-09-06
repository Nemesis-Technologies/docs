# Nemesis Docs

Public customer docs for **Nemesis** (Mintlify). This repo is the Admin / ISSO / contractor DBA surface for [NMS-88](https://linear.app/nemesistech/issue/NMS-88/admin-and-isso-documentation-set).

It is **not** the internal engineer handbook (`docs-internal`). It is **not** the home for portal runbooks — those stay in `portal` and are cited by path.

## Honesty

- **Not production-ready.**
- **CUI never.**
- **Postgres-first** (STIG Postgres 16). Do not invent full multi-engine coverage.
- **Hub-pull compose ≠ air-gap.**
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
| Lab demo pack | `first-scan/demo-pack.mdx` |
| Waivers | `first-scan/waivers.mdx` |
| Architecture for reviewer | `architecture/for-reviewer.mdx` |
| Lab / closed-network path map | `self-hosted/overview.mdx` |
| Lab compose | `self-hosted/lab-compose.mdx` |
| Air-gap pack | `self-hosted/air-gap.mdx` |
| License | `self-hosted/license.mdx` |
| Tool family | `self-hosted/tool-family.mdx` |

## Branding

Favicon uses the same mark as the internal handbook (`docs-internal` `favicon.svg`), redrawn as SVG here. Site name in the navbar is the wordmark until a licensed marketing logo is published.

## Sources of truth

Cited against portal `main` after NMS-140 at `e11720843762a8a7c2be7f12e31ec0b44e3c0bda` (confirm HEAD if you are reading later):

- Lab compose install: `apps/self-hosted/LAB-INSTALL.md` (NMS-80 / ADR-0062)
- Helm / n-1 notes: `apps/self-hosted/HELM-INSTALL.md`
- Air-gap pack: `apps/self-hosted/AIR-GAP.md`, `pack-airgap.sh`, `compose.airgap.yaml` (NMS-81 / ADR-0063)
- License: `apps/self-hosted/nemesis-license.sh`, `airgap-license-gate.sh`, `airgap-license-validate.sh` (NMS-33 / ADR-0070)
- Least-priv classify role: `docs/runbooks/nms-classify-sample-lab-role.md` and `.sql`
- CKL export design: `docs/ADR-0035-ckl-portal-export.md`
- Waivers / POA&M: `docs/ADR-0014-poam-waiver.md`

Do not relocate those portal files here.
