# WRE-107 Homepage Promise-vs-Reality Audit

Date: 2026-03-19
Scope: `index.html` (no visual redesign; copy-only corrections)

## Copy corrections made

| Area | Previous claim | Updated claim | Why |
|---|---|---|---|
| Hero deploy CTA copy | "One-click deploy path. Private model routing ready." | "Documented deploy path with operator-controlled setup. Private model routing supported via Speakeasy integration." | Avoid over-claiming one-click automation not guaranteed across envs |
| Signal CTA label | "DEPLOY IN ONE CLICK" | "DEPLOY GUIDE" | Align wording with actual documented flow |
| Signal CTA body | "Launch on Railway with preconfigured profiles, connect Telegram..." | "Follow the Railway deploy guide... configure env vars, initialize a profile..." | Reflects explicit setup steps from deploy docs |
| Credibility inventory | `mcp_tools 310+`, `vendored_skills 17` | `default_mcp_servers 3 wired by init`, `core_skill_pack 13 skills audited` | Replaced unverifiable/volatile counts with stable repo-backed facts |
| Toolkit market intelligence | "Real-time ... live market context" | "Data freshness depends on upstream provider/update cadence" | Avoid absolute real-time implication |
| Skills card | duplicate paragraph | single paragraph | Remove accidental duplication/noise |

## Evidence mapping (claim → proof)

| Claim | Repo proof |
|---|---|
| 7 profile templates | `wrenOS/docs/profile-matrix.md`; `wrenOS/packages/cli/test/smoke.test.mjs` profile runtime validation |
| Paper-first behavior | `wrenOS/packages/cli/src/index.mjs` (`liveExecution` defaults / doctor checks) |
| Deploy workflow | `wrenOS/RAILWAY_DEPLOY.md`; `wrenOS/docs/railway-first-run-playbook.md`; `wrenOS/scripts/railway-*.mjs` |
| Core skill pack readiness | `wrenOS/packs/core-skills-pack/INDEX.md`; `wrenOS/docs/release-readiness/core-skills-pack-audit.md` |

## Layout/design constraint check

- No layout structure changes
- No CSS redesign
- Copy-only updates in existing blocks/cards
- Existing visual hierarchy preserved
