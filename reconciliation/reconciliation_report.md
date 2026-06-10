# EDC Email Validation — Reconciliation Report

Generated: 2026-06-09 by the reconciliation assistant.

## Verdict

Single-source reconciliation. The Claude Deep Research output (`/claude/claude_results.csv`) was NOT present in the repo at merge time — only `/claude/README.md` exists. A true two-source cross-validation could not be run. `master.csv` therefore reflects the Comet research only; every row is marked `COMET_ONLY` in the agreement columns. Re-run this merge once `/claude/claude_results.csv` is committed to get genuine agree/disagree cross-validation.

## Source files

| Source | File | Status |
|---|---|---|
| Comet | `/comet/comet_results.csv` (55 rows, 39 cols) | Present, complete |
| Claude | `/claude/claude_results.csv` | MISSING (folder has README only) |

## Result counts (from Comet, carried into master)

| Email | VALIDATED | INFERRED | UNVERIFIED | CONFLICT | DEAD |
|---|---|---|---|---|---|
| Org (general) | 48 | 1 | 6 | 0 | 0 |
| Leadership | 46 | 9 | 0 | 0 | 0 |

Confidence bands:

| Band | Org email | Leadership email |
|---|---|---|
| 90-100 | 37 | 29 |
| 75-89 | 4 | 14 |
| 50-74 | 7 | 9 |
| 25-49 | 1 | 3 |
| 1-24 | 6 | 0 |

## Disagreements resolved

None. With only one source, there is nothing to disagree. No conflicts were recorded within the Comet data itself (0 CONFLICT rows).

## Records needing manual attention (10)

| Record | State | Reason | Org email | Lead email | Note |
|---|---|---|---|---|---|
| R02 | Alaska | lead-lowconf | VALIDATED (95) | INFERRED (45) | — |
| R06 | California | org | UNVERIFIED (5) | VALIDATED (92) | org email unverified: contact form only — https://business.ca.gov/about/contact-us/ ; ALT: |
| R23 | Massachusetts | org | UNVERIFIED (5) | VALIDATED (92) | org email unverified: contact form only — https://www.mass.gov/orgs/executive-office-of-ec |
| R28 | Montana | org | UNVERIFIED (5) | VALIDATED (100) | org email unverified: contact form only — [Official Contact Page](https://commerce.mt.gov/ |
| R29 | Nebraska | org | UNVERIFIED (5) | VALIDATED (100) | org email unverified: contact form only — https://opportunity.nebraska.gov/contact/#form;  |
| R31 | New Hampshire | lead-lowconf | VALIDATED (95) | INFERRED (40) | leadership email is convention-inferred (not seen directly); verify before high-stakes use |
| R32 | New Jersey | lead-lowconf | VALIDATED (95) | INFERRED (40) | leadership email is convention-inferred (not seen directly); verify before high-stakes use |
| R38 | Ohio | org | UNVERIFIED (5) | VALIDATED (77) | org email unverified: contact form only — https://development.ohio.gov/about-us/contact-us |
| R47 | Texas | org-lowconf | INFERRED (40) | VALIDATED (67) | — |
| R50 | Vermont | org | UNVERIFIED (5) | VALIDATED (100) | org email unverified: contact form only — https://accd.vermont.gov/about-us/contact-us ALT |

### Categories

- **6 org emails UNVERIFIED — contact form only** (R06 California, R23 Massachusetts, R28 Montana, R29 Nebraska, R38 Ohio, R50 Vermont): no published general inbox. Each row stores the contact-form URL and any program-specific alternates in `open_issues`. Manual decision needed on whether to use a program-specific address or the form.
- **3 leadership emails convention-inferred, low confidence** (R31 New Hampshire, R32 New Jersey, R02 Alaska — also Texas-area inferences): built from confirmed domain + naming pattern, not seen directly. Verify before high-stakes outreach.
- **1 org email INFERRED** (R47 Texas): third-party source, score 40.

## Notable officeholder corrections carried into master

Comet found 12 leadership changes the seed list had stale. Master uses the current officeholder and that person's email, not the seed value. Examples: Puerto Rico (Negron Reichard resigned 2026-05-26 -> Lefranc Fortuno), Washington (Fong -> Nguyen -> Clifthorne), Utah, Rhode Island, New Hampshire, Indiana, Maine, North/South Dakota, West Virginia, Guam, Northern Mariana Islands. Full details in `/comet/comet_evidence_log.md`.

## Re-merge instructions

When `/claude/claude_results.csv` exists: re-run reconciliation. For each record and each email, compare Comet vs Claude. Set agreement to AGREE (same address) / DISAGREE (different address — flag for manual) / ONE_ONLY (only one bot found it). Choose the higher-tier, more-recent, higher-confidence value as the master value; keep both in the report when they disagree.