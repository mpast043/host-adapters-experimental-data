# WORKFLOW_AUTO.md Execution Summary

## Run Information
- **Run ID**: RUN_20260228_123454
- **Objective**: PHYSICS_P
- **Status**: STOPPED (MCP_DOCS_UNAVAILABLE)
- **Compute Mode**: LOCAL_ONLY
- **Started**: 2026-02-28T17:34:54Z
- **Ended**: 2026-02-28T17:36:42Z

## What Ran

### Governance (Section 6)
- ✅ CGF server: Running on port 8000 (healthy)
- ⏭️ Repo hygiene: Not started (stopped before)
- ⏭️ Contract suite: Not started

### Document Parsing (Section 4)
- ✅ PDF located: /Users/meganpastore/Clawdbot/Repos/capacity-demo/Framework with selection.pdf
- ✅ PDF copied to RUN_DIR
- ✅ SHA256 computed: 972995a9ce94cde412d48c4cbef12cb072552baab32a1febd15ca5302ba4c0a1
- ❌ MCP markitdown: OFFLINE - SSE error: getaddrinfo ENOTFOUND microsoft
- ⏹️ **STOPPED per Section 3.1**: Required MCP server unavailable

### Physics (Sections 6-8)
- ⏹️ Not started - blocked by MCP_DOCS_UNAVAILABLE

### Selection (Section 9)
- ⏹️ Not started - blocked by MCP_DOCS_UNAVAILABLE

## MCP Inventory

| Server | Status | Tools |
|--------|--------|-------|
| microsoft/markitdown | ❌ OFFLINE | 1 tool unavailable |
| local-compute | ✅ HEALTHY | 7 tools |
| io.github.tavily-ai/tavily-mcp | ✅ HEALTHY | 4 tools |
| microsoft/playwright-mcp | ✅ HEALTHY | 22 tools |
| playwright | ✅ HEALTHY | 22 tools |

## Blockers

**Primary**: microsoft/markitdown MCP server is offline with SSE connectivity issues.

This is a required dependency per WORKFLOW_AUTO.md Section 3.1:
> "microsoft/markitdown must be healthy. If not healthy, stop with MCP_DOCS_UNAVAILABLE."

## Recovery Options

1. **Fix MCP server**: Restart the markitdown MCP server:
   ```bash
   mcporter daemon restart
   # or
   mcporter auth microsoft/markitdown --reset
   ```

2. **Use alternative MCP**: If available, configure alternative document parsing MCP server

3. **Manual markdown**: Convert PDF externally and place framework.md in RUN_DIR/results/docs/

## Rerun Command

```bash
cd /tmp/openclaws/Repos/host-adapters
# Ensure markitdown MCP is healthy first:
mcporter list microsoft/markitdown --schema

# Then resume (requires workflow modification for resume capability)
# Or start fresh after fixing MCP
```

## Artifacts Produced

| File | Path |
|------|------|
| VERDICT.json | RUN_DIR/results/VERDICT.json |
| manifest.json | RUN_DIR/manifest.json |
| PDF input | RUN_DIR/results/docs/framework.pdf |
| PDF hash | RUN_DIR/results/docs/framework.pdf.sha256 |
| MCP status | RUN_DIR/results/mcp_status.json |

## Evidence Gate

**Status**: FAILED
- ❌ results/VERDICT.json exists: ✅
- ❌ manifest.json exists: ✅
- ❌ results/docs/framework.md: MISSING (MCP dependency)
- ❌ results/docs/framework_chunks.jsonl: MISSING (MCP dependency)
- ⏹️ Other physics/selection artifacts: N/A (not reached)

## Conclusion

The PHYSICS_P objective cannot be completed without a functioning document parsing MCP server. The workflow correctly stopped per Section 3.1 requirements.
