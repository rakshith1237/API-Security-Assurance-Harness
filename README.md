Security Assurance Harness (Swagger Petstore)

An end-to-end API security workflow that produces **repeatable evidence**: spec scan (KICS) → runtime tests (Postman) → automation (Newman) → manual validation (Burp) → final report.

## Scenario (why this exists)
A common failure mode in real security assessments is not “missing tools.” It is **missing repeatability**:
- Findings cannot be reproduced.
- Fixes cannot be verified over time.
- Evidence is scattered across screenshots and terminals.

This repo acts as an **audit-friendly case file**: commands, artifacts, and notes are stored in predictable locations and tracked in Git.

## Target
- Base URL: https://petstore3.swagger.io/api/v3
- OpenAPI spec: https://petstore3.swagger.io/api/v3/openapi.json

## Repository structure
- `spec/` — OpenAPI contract used for scanning and test planning
- `reports/kics/` — KICS outputs (HTML/JSON)
- `postman/` — Postman collection + environment exports
- `reports/newman/` — Newman run reports
- `scripts/` — one-command runners (`run_kics.sh`, `run_newman.sh`)
- `burp/` — manual validation notes and proof snippets
- `inventory/` — endpoint inventory and discovery notes
- `docs/` — runbook and final report
- `evidence/` — screenshots and terminal logs

## Quickstart (will be filled as we build)
- KICS scan: `scripts/run_kics.sh`
- Newman run: `scripts/run_newman.sh`

## Evidence
- KICS: `reports/kics/`
- Newman: `reports/newman/`
- Manual notes: `burp/notes.md`
- Final writeup: `docs/final-report.md`

## Notes / constraints
- GitHub may display HTML reports as raw source. Open HTML reports locally in a browser, or publish them separately if needed.
- Terminal hygiene: avoid pasting Markdown-style links into commands. Use plain filenames and plain URLs.
