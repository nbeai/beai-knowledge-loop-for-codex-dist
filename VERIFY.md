# Verification Record

Package:

```text
beai-knowledge-loop-for-codex-team-install-20260701-2246.zip
```

## Archive Integrity

Command:

```bash
zip -T dist/beai-knowledge-loop-for-codex-team-install-20260701-2246.zip
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

Result:

```text
passed
```

## Local Path Hygiene

Checked staging package for local-only paths and diagnostic references:

- developer-machine absolute paths
- `codex-marketplace-release`
- `codex-marketplace`
- diagnostic direct MCP naming

Result:

```text
no matches
```

## Plugin Manifest Sanity

Checked:

- plugin name
- version
- defaultPrompt array shape
- `beaiKnowledgeLoop` MCP server presence

Result:

```text
passed
```

## Source Project Verification

Command:

```bash
npm --prefix work/beai-knowledge-loop-for-codex run verify
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

## BEAI Verification

Command:

```bash
beai verify --run --scenario --meaning
```

Result:

```text
passed
```

Command:

```bash
beai closeout --apply
```

Result:

```text
ready
```

## Remaining Validation

This is still an internal team install candidate. A teammate should perform a real install on their own Codex app and confirm:

- `설치.command` completes
- Codex app restart exposes the plugin
- a fresh Codex thread can call the BEAI Knowledge Loop MCP tools
