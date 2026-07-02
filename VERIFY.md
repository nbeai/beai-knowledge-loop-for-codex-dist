# Verification Record

Package:

```text
beai-knowledge-loop-for-codex-team-install-20260702-234218.zip
```

SHA-256:

```text
ee11d746ff2a4753121561fd13f560bf682ac0a6f67f38a64bdf7dab7ef312a9
```

## Source Project Verification

Command:

```bash
npm run verify
npm run package:hygiene
```

Result:

```text
passed
```

Covered:

- MCP tools/list
- knowledge.index
- weighted knowledge.search
- knowledge.set_review_state
- stale knowledge demotion
- knowledge.capture_draft
- knowledge.review_queue
- knowledge.promote_plan
- knowledge.evaluate
- knowledge.boundaries
- draft id path traversal rejection
- retrieval eval path containment
- source path handling with spaces
- smoke test in a temporary workspace

## Install-Root Verification

An unpacked copy was patched with `tools/patch-mcp-paths.mjs`, then verified with:

```bash
node scripts/verify-plugin-install-root.js <plugin-root>
```

Result:

```text
passed
```

This confirms the installed manifest points at an MCP server inside the actual plugin install root.

## Archive Integrity

Command:

```bash
zip -T beai-knowledge-loop-for-codex-team-install-20260702-234218.zip
```

Result:

```text
OK
```

## Package Hygiene

Checked that the archive does not include:

- `.beai-harness`
- `.codex/knowledge-loop`
- `review-queue`
- `drafts`
- `generated`
- developer-machine local absolute paths

Result:

```text
passed
```

## Remaining Validation

This is a production-candidate team install package. Stable release still requires real teammate install feedback and external user validation.
