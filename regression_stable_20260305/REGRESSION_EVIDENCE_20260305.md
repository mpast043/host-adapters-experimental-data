# Stable Regression Evidence (2026-03-05)

Runner: `experiments/physics/PHYS_BORDER_XXZ_ED_runner_v1.py`

## A) Solver Mismatch (degraded DMRG)
Overall: **SCOPE_INCONCLUSIVE**
- Δ=0.5: verdict=INCONCLUSIVE, reason=SOLVER_MISMATCH, calibration_pass=False, pooling_applied=False
- Δ=2.0: verdict=INCONCLUSIVE, reason=SOLVER_MISMATCH, calibration_pass=False, pooling_applied=False
- Source JSON: `outputs/regression_stable_20260305/A_solver_mismatch/run_ed_25c6c279/xxz_boundary_results.json`

## B) Solver Pass Bulk (pooled)
Overall: **SCOPE_VALIDATED**
- Δ=0.5: verdict=REJECT, ΔAICc=20.1325, calibration_pass=True, pooling_applied=True, parity=L_mod_4_eq_0
- Δ=2.0: verdict=ACCEPT, ΔAICc=-21.0588, calibration_pass=True, pooling_applied=True, parity=L_mod_4_eq_0
- Source JSON: `outputs/regression_stable_20260305/B_solver_pass_bulk/xxz_boundary_results.json`

## C) Mixed-Even Warning / Oscillation
Overall: **SCOPE_VALIDATED**
- Δ=0.5: verdict=REJECT, ΔAICc=24.9962, parity=mixed_even, fit_variant=oscillation_corrected
- Warning log: `outputs/regression_stable_20260305/C_mixed_even_warning/run.log`
- Source JSON: `outputs/regression_stable_20260305/C_mixed_even_warning/xxz_boundary_results.json`

## Policy Corrections (authoritative)
- Authoritative scope gate uses observed S(L/2,L) data with AICc comparison only.
- Literature benchmark is regression/interpretation aid and is not used for scope gating decisions.
- Do not model gapped phases with CFT central charge; gapped classification is based on saturation-vs-log model evidence in observed data.
- Decision metric is delta_aicc_sat_minus_log = AICc_sat - AICc_log (negative favors saturation/IN_SCOPE, positive favors log/OUT_OF_SCOPE).
