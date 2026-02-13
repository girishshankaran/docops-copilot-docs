# Audit Record: Home UI docs sync

- Date: 2026-02-13
- Repository: `girishshankaran/docops-copilot-docs`
- Direct-to-main docs commit: `2c7d21c`
- Related code repo fix: `girishshankaran/docops-copilot` commit `0aa23ed`

## Why this record exists
The docs update for `ui/home1.html` did not auto-sync when the code PR merged because the workflow gate checked `env.DOCS_PAT` instead of `secrets.DOCS_PAT`.

A manual backfill was applied to keep `docs/ui/home1.md` aligned with code behavior:
- Removed outdated Shout Out flow
- Added Call modal behavior

This file provides PR-visible traceability for that manual backfill.
