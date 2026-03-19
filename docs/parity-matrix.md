# WRE-109 Docs Parity Matrix (wrenos.ai/docs vs wrensignal/wrenOS)

Date: 2026-03-19

## Section parity

| Live docs section (`wrenos.ai/docs`) | Source markdown/code path | Parity status | Notes |
|---|---|---|---|
| Overview | `docs/index.html` + links into repo docs | Updated | Inventory metrics normalized to stable, verifiable values |
| Quick Start | `wrenOS/docs/quickstart.md` | Aligned | Commands validated against current CLI names |
| Configuration | `wrenOS/packages/cli/src/index.mjs` + config keys | Updated | Replaced stale `execution.paperMode` snippet with `liveExecution` |
| Safety Posture | `wrenOS/docs/safety.md` | Aligned | Paper-first messaging retained |
| CLI Overview / init / doctor / status | `wrenOS/packages/cli/src/index.mjs` | Aligned | Command surface references current runtime |
| Speakeasy Integration | `wrenOS/docs/speakeasy-integration.md` | Aligned | Private model routing wording preserved |
| Railway Deploy | `wrenOS/RAILWAY_DEPLOY.md`, `wrenOS/docs/railway-first-run-playbook.md` | Aligned | Deploy language framed as documented flow, not one-click guarantee |
| Migration | `wrenOS/docs/migrating-from-0xclaw-to-wrenos.md` | Aligned | Naming remains WrenOS-first |
| Docs Parity Matrix | `0xClaw-site/docs/parity-matrix.md` (this file) | Added | Reviewer checklist included |

## Contradictions removed in this pass

1. **Inflated/unstable inventory numbers in docs overview**
   - Replaced `mcp_tools 310+` with `default_mcp_servers 3 wired by init`
   - Replaced generic `skills 17` with `core_skills_pack 13 audited`

2. **Stale config command in CLI Overview snippet**
   - Replaced `wrenos config set execution.paperMode true`
   - With `wrenos config set liveExecution false`

## Reviewer checklist

- [ ] Each major docs section has an explicit source-of-truth path
- [ ] No stale command/flag names remain
- [ ] No contradictory safety posture language remains
- [ ] Overview metrics are stable and verifiable from current repo state
- [ ] Docs sync marker references current source commit
