# OpenClaw Optimization Status

- Generated: 2026-02-28 02:22:09Z

## Memory
- Before: provider=none, files=0, chunks=0, searchMode=fts-only, sources=['memory']
- After: provider=openai, files=16, chunks=212, searchMode=hybrid, sources=['memory', 'sessions']
- Current config: local Ollama embedding route via OpenAI-compatible endpoint (`http://127.0.0.1:11434/v1`), model `nomic-embed-text`, fallback `none`.

## Compaction
- Mode: `safeguard` (kept for low-risk context trimming).

## Skills
- Eligible now: 16
- Disabled now: 1 (apple-notes)
- Missing requirements: 34

### Recommended active set for workflow-auto/governance
- coding-agent
- github
- gh-issues
- mcporter
- session-logs
- healthcheck
- nano-pdf
- model-usage
- clawhub
- summarize

### Optional installs (only if needed)
- notion (Notion API workflows)
- gemini (secondary model CLI)
- slack/discord channels (if channel automation required)
