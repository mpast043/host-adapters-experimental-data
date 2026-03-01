# Framework Selection Test Plan

Generated: 2026-02-28T18:43:24.029829+00:00
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
| platform_openclaw_opt_check_relaxed | A | A | 3 |

## Blocked
| Test | Tier | Reason |
|---|---|---|
| claim3_optionb_regime_check | B | FOCUS_OBJECTIVE_FILTER: A |
| claim2_seed_perturbation | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w02_poset_infimum | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w06_depth_vector_monotonicity | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w08_class_splitting_monotonicity | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w13_cobs_decomposition_compat | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w14_ejection_expands_core | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w16_time_consistency_monotone | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w09_delta_t_well_defined | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w10_observer_non_influence | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w12_observer_triad_mapping | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w03_memory_excision_consistency | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w04_self_reference_consistency | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w07_cross_axis_isolation | B | FOCUS_OBJECTIVE_FILTER: A |
| claim3p_ising_cyclic_l8 | C | FOCUS_OBJECTIVE_FILTER: A |
| claim3p_heisenberg_cyclic_l8 | C | FOCUS_OBJECTIVE_FILTER: A |
| claim3p_l16_gate | C | FOCUS_OBJECTIVE_FILTER: A |
| claim_w11_cpmt_annex_t_conformance | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w15_pointer_accuracy_orthogonality | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w17_local_global_fixed_point_compat | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w18_compression_governance_t7 | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w19_meta_limitation_acknowledged | B | FOCUS_OBJECTIVE_FILTER: A |
| claim_w20_non_negotiability_self_application | B | FOCUS_OBJECTIVE_FILTER: A |

## Stop Condition
- Triggered: `True`
- Note: Time remained while only Tier C work was queued. Budget reallocated to Tier A hardening tasks.

- Remaining budget minutes: `112`
