# Framework Selection Test Plan

Generated: 2026-02-28T03:05:43.171428+00:00
Mode: `FULL`
Compute target: `local-compute`

## Step 0 Gate
1. What decision changes if this test passes vs fails?
2. Which critical path objective does it serve?

Tier rules applied:
- Tier A: always allowed; highest priority.
- Tier B: allowed only when it protects a supported claim or prevents regression.
- Tier C: blocked unless `RUN_OVERRIDE_TIER_C=1` with one-line justification.

## Selected
| Test | Tier | Objective | Minutes |
|---|---|---|---:|
| platform_mcporter_health_snapshot | A | A | 2 |
| platform_openclaw_opt_check | A | A | 3 |
| claim2_seed_perturbation | B | B | 4 |
| claim3_optionb_regime_check | B | B | 8 |
| claim3p_ising_cyclic_l8 | C | C | 8 |
| claim3p_heisenberg_cyclic_l8 | C | C | 10 |
| claim3p_l16_gate | C | C | 20 |

## Blocked
| Test | Tier | Reason |
|---|---|---|
| none | - | - |

## Stop Condition
- Triggered: `False`
- Note: Not triggered

- Remaining budget minutes: `65`
