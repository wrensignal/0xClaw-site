# WRE-114 Site/Docs Regression Harness Report

Generated: 2026-03-20

## Automated checks
- Script: `scripts/site-regression-audit.mjs`
- Artifact: `docs/reports/site-regression-report.json`

Checks include:
- canonical + description meta tags (homepage/docs)
- primary homepage links (`/docs/`, GitHub repo)
- docs navigation anchors (`#quick-start`, `#configuration`, `#architecture`)
- route status code checks for `https://wrenos.ai/` and `https://wrenos.ai/docs`

## Baseline screenshots
- `docs/reports/screenshots/wre-114-homepage.jpg`
- `docs/reports/screenshots/wre-114-docs.png`

## Current result
- 11/11 checks passing
- No P0/P1 regressions detected in this baseline run

## CI integration
- Added `.github/workflows/site-regression.yml`
- Runs `node scripts/site-regression-audit.mjs` on PRs and main pushes
- Uploads `docs/reports/site-regression-report.json` as workflow artifact

## Hardening update
- Added redirect-following status checks (up to 5 hops).
- Added route checks for both apex and `www` host variants for `/` and `/docs`.
- Report now captures redirect count per checked route.

## Operator run command
- `./scripts/run-site-regression.sh`
