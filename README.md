# BEAI Knowledge Loop for Codex

AI coding agents are getting stronger, but they are still LLM-based workers.

They can code, summarize, refactor, and investigate. But if their work history disappears after every session, the human team still has to carry the real operational memory.

**BEAI Knowledge Loop for Codex** is a review-first work memory layer for Codex.

It helps Codex search prior source-grounded decisions before work, then capture review-only draft knowledge after work. The human keeps authority over what becomes approved knowledge.

Core principle:

> Auto-capture, not auto-approve.

## What This Is

This is a public preview distribution package for people who want to test the BEAI Knowledge Loop pattern with Codex.

It helps Codex:

- search prior source-grounded decisions before work
- capture review-only draft knowledge after work
- keep reusable traps, decisions, evidence, and next actions from disappearing
- avoid uncontrolled durable memory writes

Think of it as an AI worker's worklog and handoff system, not just an AI-readable wiki.

## What This Is Not

This is not:

- a customer-ready commercial installer
- an automatic durable memory writer
- an external publishing or sending tool
- an automation/cron/hook activation package
- a legal, payment, contract, account, or deployment automation

Human approval is still required for approved knowledge promotion, external actions, public posting, release claims, and consequential operations.

## Why It Matters

Most AI memory discussions focus on giving the model more context.

BEAI Knowledge Loop focuses on a different question:

> How do humans keep ownership of judgment while AI work becomes reusable organizational knowledge?

That difference matters for Codex, Claude Code, Cursor, and any LLM-based work agent. Better agents do not remove the need for review boundaries. They make those boundaries more important.

## Package

Current package:

- `beai-knowledge-loop-for-codex-team-install-20260701-2246.zip`
- `beai-knowledge-loop-for-codex-team-install-20260701-2246.sha256`

SHA-256:

```text
1ee5799fae804c00d17a5fbf23f899966b1e7205698ca580d33becc5bf480e86
```

## Install

1. Download the zip file.
2. Unzip it into a normal local folder.
3. Run `설치.command` inside the unzipped folder.
4. Restart the Codex app.
5. Open Plugins and install `BEAI Knowledge Loop for Codex` from `BEAI Team Local`.
6. Start a fresh Codex thread.

See:

- `README-TEAM-INSTALL-ko.md`

## Verification

The package was checked before upload:

- `zip -T` passed
- package hygiene passed
- no developer-machine local absolute path was found in the staging package
- no `.beai-harness` internal work log was included
- no `.codex/knowledge-loop`, `drafts`, `review-queue`, or `generated` store folders were included
- MCP server syntax check passed
- plugin manifest sanity check passed
- source project `npm run verify` passed
- BEAI verify and closeout passed

## Current Status

Status: public preview / team install candidate.

Next validation: a teammate should install this package in their own Codex app and confirm that the plugin and MCP tools become visible in a fresh thread.

## Copyright

Created by BEAI.

Copyright (c) 2026 박종윤 / Jongyoon Park (@aigis0927). All rights reserved unless otherwise stated.

GitHub: https://github.com/nbeai
