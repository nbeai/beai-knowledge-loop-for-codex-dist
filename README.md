# BEAI Knowledge Loop for Codex

AI coding agents are getting stronger, but they are still LLM-based workers.

They can code, summarize, refactor, and investigate. But if their work history disappears after every session, the human team still has to carry the real operational memory.

**BEAI Knowledge Loop for Codex** is a review-first work memory layer for Codex.

It helps Codex search prior source-grounded decisions before work, then capture review-only draft knowledge after work. The human keeps authority over what becomes approved knowledge.

Core principle:

> Auto-capture, not auto-approve.

## What This Is

This is a production-candidate distribution package for people who want to test the BEAI Knowledge Loop pattern with Codex.

It helps Codex:

- search prior source-grounded decisions before work
- capture review-only draft knowledge after work
- keep reusable traps, decisions, evidence, and next actions from disappearing
- avoid uncontrolled durable memory writes
- verify plugin install-root MCP paths before use

Think of it as an AI worker’s worklog and handoff system, not just an AI-readable wiki.

## What This Is Not

This is not:

- an automatic durable memory writer
- an external publishing or sending tool
- an automation/cron/hook activation package
- a legal, payment, contract, account, or deployment automation
- a replacement for human review before approved knowledge promotion

Human approval is still required for approved knowledge promotion, external actions, public posting, release claims, and consequential operations.

## Production Hardening in 0.1.1

This candidate adds:

- draft id path traversal rejection
- workspace/store containment checks
- retrieval eval path containment
- smoke tests that run in temporary workspaces instead of polluting source
- install-root MCP path verification
- self-contained package hygiene command
- local absolute path cleanup in packaged docs

## Package

Current package:

- `beai-knowledge-loop-for-codex-team-install-20260702-234218.zip`
- `beai-knowledge-loop-for-codex-team-install-20260702-234218.sha256`

SHA-256:

```text
ee11d746ff2a4753121561fd13f560bf682ac0a6f67f38a64bdf7dab7ef312a9
```

## Install

1. Download the zip file.
2. Unzip it into a normal local folder.
3. Run `설치.command` inside the unzipped folder.
4. Restart the Codex app completely.
5. Open Plugins and install `BEAI Knowledge Loop for Codex` from `BEAI Team Local`.
6. Start a fresh Codex thread.

See:

- `README-TEAM-INSTALL-ko.md`

## Verification

The package was checked before upload:

- `npm run verify` passed
- Node scenario tests: 6 passed
- path traversal hardening test passed
- eval path containment test passed
- smoke test passed in temporary workspace
- install-root MCP path verification passed on an unpacked copy
- `zip -T` passed
- package hygiene passed
- no developer-machine local absolute path was found in the staging package
- no `.beai-harness` internal work log was included
- no `.codex/knowledge-loop`, `drafts`, `review-queue`, or `generated` store folders were included

## Current Status

Status: production-candidate / team install package.

Stable release still requires real teammate install feedback and external user validation.

## Copyright

Created by BEAI.

Copyright (c) 2026 박종윤 / Jongyoon Park (@aigis0927). All rights reserved unless otherwise stated.

GitHub: https://github.com/nbeai
