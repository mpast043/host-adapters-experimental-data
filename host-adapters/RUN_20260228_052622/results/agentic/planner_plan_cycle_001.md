# Framework Selection Test Plan

Generated: 2026-02-28T05:26:37.461027+00:00
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
| claim2_seed_perturbation | B | B | 4 |
| claim3_optionb_regime_check | B | B | 8 |

## Blocked
| Test | Tier | Reason |
|---|---|---|
| platform_openclaw_opt_check | A | FOCUS_OBJECTIVE_FILTER: B |
| platform_mcporter_health_snapshot | A | FOCUS_OBJECTIVE_FILTER: B |
| platform_openclaw_opt_check_relaxed | A | FOCUS_OBJECTIVE_FILTER: B |
| claim3p_ising_cyclic_l8 | C | FOCUS_OBJECTIVE_FILTER: B |
| claim3p_heisenberg_cyclic_l8 | C | FOCUS_OBJECTIVE_FILTER: B |
| claim3p_l16_gate | C | FOCUS_OBJECTIVE_FILTER: B |

## Stop Condition
- Triggered: `True`
- Note: Time remained while only Tier C work was queued. Budget reallocated to Tier A hardening tasks.

- Remaining budget minutes: `108`
