# EDC Email Validation Project

Goal: validate the default org emails (e.g. `info@...`) and the leadership emails for 55 U.S. state and territory economic development organizations, with linked proof and a confidence score for each. Low tolerance for failure: an email is only marked confirmed when it is seen on an official source.

## How it works

Two AI research tools each research all 55 records independently:
- **Claude Opus 4.8 Deep Research** → output goes to the **desktop** copy, folder `/claude/`.
- **Comet (Perplexity) Deep Research** → writes directly to the **GitHub** repo, folder `/comet/`.

Running both independently gives cross-validation: when the two agree on an email and a source, confidence is high; when they disagree, the record is flagged for manual attention. After both finish, the two copies are merged on GitHub and the reconciliation assistant (Claude) audits them into `/reconciliation/master.csv`.

## Two copies of this repo

The two tools have different access, so the project runs across two synced copies:
- **Desktop:** `C:\Users\mblin\OneDrive\Desktop\EDCs` — Claude's working copy. The scaffold is built here.
- **GitHub:** `github.com/blake-a11y/EDCs` — Comet's working copy (Comet has admin read/write; it cannot see the desktop).

The scaffold is pushed from desktop to GitHub once at setup, so both copies share the same contract, rubric, and input list. At the end, Claude's `/claude/` output is pushed from desktop to GitHub on a branch and merged. Because Claude's files live in `/claude/` and Comet's in `/comet/`, the merge does not collide.

## Folder map

```
EDCs/
  00_input/edc_input.csv          55 records to research (the seed list)
  01_contract/
    DATA_CONTRACT.md              exact output schema + rules (READ FIRST)
    CONFIDENCE_RUBRIC.md          how 1-100 confidence is scored
    output_template.csv           the 39-column header both bots fill
    evidence_log_template.md      the "show your math" template
  claude/                         Claude Deep Research output (filled on desktop)
  comet/                          Comet Deep Research output (filled on GitHub)
  reconciliation/                 final merged master.csv (built by Claude)
  prompts/                        the phased prompt docs for each bot
```

## The six phases (each gated by "Go")

| Phase | What it does |
|-------|--------------|
| P0 | Setup. Bot loads the data contract, rubric, and input. No research. |
| P1 | Confirm each org's canonical domain and naming convention, with 2 real sample emails as proof. |
| P2 | Validate the default org email (info@ etc.). |
| P3 | Confirm who currently holds the leadership role. |
| P4 | Validate the leadership email for the confirmed current person. |
| P5 | Retry every UNVERIFIED and CONFLICT record; finalize confidence scores. |

## File movement (how data gets into the repo)

**Claude Deep Research** cannot save files. Per phase: (1) Claude prints its results in its chat, (2) you paste that into the reconciliation Claude chat, (3) Claude writes the file into the desktop `/claude/` folder.

**Comet Deep Research** has read/write access to the GitHub repo. It commits its results file and evidence log directly to `/comet/` on GitHub. No paste step.

Each bot's reply ends with a 2-sentence data-quality summary, a 1–100 confidence rating, and `Ready for next phase? say "Go"`.

## Reconciliation

After both bots finish: push the desktop `/claude/` output to GitHub on a branch and merge, OR the assistant pulls Comet's `/comet/` files from GitHub (public raw URLs) and merges them with the desktop `/claude/` files. Output: `/reconciliation/master.csv` plus `reconciliation_report.md`.

## Status

- [x] Repo scaffolded
- [x] Input seed built (55 records)
- [x] Data contract + rubric locked
- [ ] Scaffold pushed to GitHub (run the one-time PowerShell at setup)
- [ ] Prompt docs written
- [ ] Claude Deep Research run
- [ ] Comet Deep Research run
- [ ] Reconciliation / master.csv
