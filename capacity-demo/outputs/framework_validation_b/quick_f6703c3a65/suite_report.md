# Framework v4.5 Option B — Validation Report

**Suite ID:** quick_f6703c3a65
**Date:** 2026-02-27T18:04:14
**Elapsed:** 0.0s
**Configs:** 5

## Summary

- Monotone d_s(C): 5/5 runs
- Dimension reduction observed: 4/5 runs

## Results by Run

| Config | Substrate | Filter | |V| | d_s(C_min) | d_s(C_max) | Reduction | Mono | R^2 |
|--------|-----------|--------|-----|------------|------------|-----------|------|-----|
| lattice_D2_N16__hard_cutoff | periodic_lattice_D2_N16 | hard_cutoff | 256 | 1.72 | 2.01 | 0.30 | PASS | 0.998 |
| lattice_D2_N16__soft_cutoff | periodic_lattice_D2_N16 | soft_cutoff | 256 | 1.87 | 2.01 | 0.14 | PASS | 0.998 |
| lattice_D2_N16__powerlaw | periodic_lattice_D2_N16 | powerlaw_reweight | 256 | 1.95 | 2.01 | 0.06 | PASS | 0.998 |
| rgg_D2_n200__powerlaw | rgg_D2_n200_r0.350_s42 | powerlaw_reweight | 200 | 2.60 | 2.81 | 0.21 | PASS | 0.966 |
| sw_n200__powerlaw | smallworld_n200_k6_p0.30_s42 | powerlaw_reweight | 200 | 0.86 | 0.97 | 0.11 | PASS | 0.867 |

## Interpretation

**What is proved:** For any substrate with known Laplacian eigenvalues,
the monotone spectral filter family g_C produces a filtered return probability
P_C(sigma) whose spectral dimension d_s^C(sigma) varies with C.

**What is empirically validated:**
- d_s(C) is approximately monotone non-decreasing in C
- Dimension reduction is observed: d_s at low C < d_s at high C
- The power-law scaling assumption (ln P ~ linear in ln sigma)
  holds reasonably well in the declared scaling window (R^2 values above)

**What is NOT claimed:**
- The exact value of d_s at a given C is not predicted by the theorem
  (it depends on the substrate's spectral density and the filter form)
- The scaling window bounds are set heuristically, not derived
- The monotonicity tolerance (0.15) is empirical
