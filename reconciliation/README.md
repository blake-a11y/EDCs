# /reconciliation

Claude (the reconciliation assistant) writes the audited, merged output here after both bots finish.

Claude's `/claude/` files are on the desktop. Comet's `/comet/` files are on GitHub. To merge, Claude either reads Comet's files from the public GitHub raw URLs, or you push the desktop `/claude/` output to GitHub on a branch and merge first.

- `master.csv` — final merged result. One row per record: chosen email, winning source, agreement status between the two bots, and final confidence.
- `reconciliation_report.md` — what disagreed, how it was resolved, and which records still need manual attention.

Do not edit by hand during the run.
