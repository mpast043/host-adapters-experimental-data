# Capacity-of-Entanglement (κ₂) Analysis

**Date**: 2026-03-04
**Test**: Second cumulant of entanglement spectrum (variance)

## Executive Summary

Testing the TRUE capacity of entanglement (κ₂) as identified in literature
(de Boer, Järvelä, Keski-Vakkuri PRD 99, 066012, 2019).

## Results

### Ising (c = 1/2, Gapped)

| L | S (κ₁) | C (κ₂) | d_eff |
|---|--------|--------|-------|
| 6 | 0.693 | 0.048 | 2.00 |
| 8 | 0.699 | 0.045 | 2.01 |
| 10 | 0.699 | 0.043 | 2.01 |
| 12 | 0.699 | 0.042 | 2.01 |

**Scaling:**
- S = 0.691 + 0.004 × log(L) → **SATURATES**
- C = 0.072 - 0.012 × log(L) → **SATURATES**

### Heisenberg (c = 1, Critical)

| L | S (κ₁) | C (κ₂) | d_eff |
|---|--------|--------|-------|
| 6 | 0.96 | 0.76 | 2.61 |
| 8 | 1.05 | 0.99 | 2.86 |
| 10 | 1.12 | 1.04 | 3.07 |
| 12 | 1.18 | 1.10 | 3.27 |

**Scaling:**
- S = 0.376 + 0.325 × log(L) → **GROWS**
- C = -0.083 + 0.472 × log(L) → **GROWS**

## Key Discovery

**κ₂ (Capacity) grows FASTER than κ₁ (Entropy) for Heisenberg!**

| Model | S slope | C slope | C/S ratio |
|-------|---------|---------|-----------|
| Ising | 0.004 | -0.012 | ~0.06 |
| Heisenberg | 0.325 | 0.472 | ~1.45 |

The capacity-to-entropy ratio is **24× larger for Heisenberg** than Ising.

## Physical Interpretation

| Model | Gap | Entanglement Structure | Capacity Behavior |
|-------|-----|------------------------|-------------------|
| Ising | Gapped | Bounded | Both κ₁ and κ₂ bounded |
| Heisenberg | Gapless | Critical | Both κ₁ and κ₂ logarithmic |

## Literature Comparison

From de Boer et al. (PRD 2019):
> C ∝ c × (1/6) × log(L) for critical systems

CFT prediction for Heisenberg: C ≈ 0.17 × log(L)
Our measured slope: C ≈ 0.47 × log(L)

**Our capacity growth is ~2.8× faster than CFT prediction.**

This may indicate:
1. Finite-size corrections not yet converged
2. Additional non-CFT contributions
3. Measurement of a different quantity than literature

## Conclusion

1. **Ising**: Capacity framework fully applicable (both cumulants bounded)
2. **Heisenberg**: Capacity framework needs extension (both cumulants grow)
3. **Key insight**: P2 tested κ₁, but κ₂ shows same qualitative behavior

The Heisenberg "failure" of P2 is NOT due to testing the wrong cumulant.
Both entropy AND capacity grow logarithmically for critical systems.
