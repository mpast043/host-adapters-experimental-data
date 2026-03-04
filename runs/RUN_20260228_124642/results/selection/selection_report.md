# Physics Selection Report

## Claims Summary

| Claim | Status | Evidence | Document Witness |
|-------|--------|----------|------------------|
| W01 | SUPPORTED | P1 exp1_verdict.json | chunk_0000 |
| W02 | REJECTED | P4 verdict.json | chunk_0019 |
| W03 | UNDERDETERMINED | None | chunk_0002 |

## Acceptance Rules Applied
- Document witness span required: ✅
- Evidence witness path required: ✅ (for SUPPORTED/REJECTED)

## Key Findings
- W01 (Capacity): SUPPORTED by spectral dimension P1
- W02 (MERA physical): REJECTED by P4 physical convergence tests
- W03 (Gluing stability): UNDERDETERMINED - no P3 runner available

## Rejected Claims Analysis
- W02 falsified by P4: MERA fidelity did not meet thresholds
  - best_fidelity: 0.218 (threshold: 0.95)
  - final_entropy_error: 0.456 (threshold: 0.15)
