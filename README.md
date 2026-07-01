# BEAI Knowledge Loop for Codex Distribution

Internal team-install package for BEAI Knowledge Loop for Codex.

This repository stores a verified zip package that a teammate can unzip and install into their own Codex app.

## What This Is

BEAI Knowledge Loop for Codex is a review-first knowledge loop for Codex work.

It helps Codex:

- search prior source-grounded decisions before work
- capture review-only draft knowledge after work
- keep reusable traps, decisions, evidence, and next actions from disappearing
- avoid uncontrolled durable memory writes

Core principle:

> Auto-capture, not auto-approve.

## What This Is Not

This is not:

- a public release
- a customer-ready installer
- an automatic durable memory writer
- an external publishing or sending tool
- an automation/cron/hook activation package
- a legal, payment, contract, account, or deployment automation

Human approval is still required for approved knowledge promotion, external actions, public posting, release claims, and consequential operations.

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

Status: internal team install candidate.

Next validation: a teammate should install this package in their own Codex app and confirm that the plugin and MCP tools become visible in a fresh thread.
