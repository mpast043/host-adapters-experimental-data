# WORKFLOW_AUTO Summary

Run: `RUN_20260228_054918`
Mode: `COMPLETE`

## 1. What ran
- Baseline suite: claim2/claim3/claim3p (local deterministic commands)
- Exploration subset executed under budget constraints

## 2. What was learned and what changed
- Contract status: `LINT_DEBT`
- Science status: `PARTIAL`
- Selection status: `ACCEPTED`

## 3. Current conclusions
- Evidence is retained under `results/` and selected claims are classified in `results/selection/ledger.jsonl`.

## 4. Underdetermined items and next tests
- See underdetermined entries in `results/selection/ledger.jsonl` with `next_test` recommendations.

## 5. Troubleshooting and fixes applied
- Port rotation used for CGF startup: [8080, 18080, 28080, 38080]
- LOCAL_ONLY downscoping auto-applied when compute MCP target is unavailable.

## 6. Rerun commands
- `python3 tools/run_workflow_auto.py --repo-root /private/tmp/openclaws/Repos/host-adapters --artifacts-root /private/tmp/openclaws/Repos/host-adapters-experimental-data/host-adapters --run-id RUN_20260228_054918 --resume`
- `python3 tools/validate_workflow_auto_run.py --run-dir /private/tmp/openclaws/Repos/host-adapters-experimental-data/host-adapters/RUN_20260228_054918`
