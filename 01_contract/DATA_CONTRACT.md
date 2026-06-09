# DATA CONTRACT — EDC Email Validation

This file defines the exact output format both research bots (Claude Opus 4.8 Deep Research and Comet Deep Research) must follow. Both bots produce the SAME columns and the SAME controlled values so the two files can be compared and merged. Do not add, rename, or reorder columns.

---

## 1. Output files each bot produces

| File | Location | What it holds |
|------|----------|---------------|
| `<bot>_results.csv` | `/claude/` or `/comet/` | One row per record (55 rows). The structured result. Re-emitted complete at the end of every research phase. |
| `<bot>_evidence_log.md` | `/claude/` or `/comet/` | Human-readable proof: the "show your math" for each domain and email. Appended each phase, never overwritten. |

`<bot>` is literally `claude` or `comet`.

**Transport (where files physically go):** Claude's files are written to the desktop folder `C:\Users\mblin\OneDrive\Desktop\EDCs\claude\` (Blake pastes Claude's chat output to the reconciliation assistant, who writes the file). Comet writes its files directly to the GitHub repo `github.com/blake-a11y/EDCs` under `/comet/`. Both copies must match this contract exactly. The two are merged on GitHub at the end.

---

## 2. CSV rules (must follow exactly)

- Format: RFC 4180. Quote EVERY field with double quotes.
- No line breaks inside a field. Replace any newline with a single space.
- Encoding: UTF-8.
- `evidence_quote` fields: max 200 characters, copied verbatim from the page (the actual on-page text showing the email).
- Empty/unknown value = empty string `""`. NEVER write "N/A", "unknown", or a guess in place of empty.
- Row order = `record_id` ascending (R01–R55).

---

## 3. Column list (39 columns, exact order)

| # | Column | Filled in phase | Allowed values / format |
|---|--------|-----------------|-------------------------|
| 1 | record_id | carried from input | R01–R55 |
| 2 | state_territory | carried from input | text |
| 3 | organization | carried from input | text |
| 4 | official_website | P1 | confirmed official URL |
| 5 | canonical_domain | P1 | e.g. `azcommerce.com` |
| 6 | domain_confirmation_method | P1 | `SITE_PUBLISHED_EMAIL` / `DNS_MX` / `OFFICIAL_DOC` / `OTHER` |
| 7 | domain_evidence_url | P1 | URL actually opened |
| 8 | naming_convention | P1 | `first.last` / `firstlast` / `finitial.last` / `first_last` / `flast` / `last.first` / `firstname` / `NONE_FOUND` / `CATCH_ALL_UNKNOWN` |
| 9 | convention_sample1_email | P1 | a REAL published email at the domain |
| 10 | convention_sample1_url | P1 | URL where sample 1 was seen |
| 11 | convention_sample2_email | P1 | a second REAL published email |
| 12 | convention_sample2_url | P1 | URL where sample 2 was seen |
| 13 | convention_confidence | P1 | integer 1–100 (see rubric) |
| 14 | current_officeholder_name | P3 | text |
| 15 | current_officeholder_title | P3 | text |
| 16 | officeholder_confirmed | P3 | `Y` / `N` |
| 17 | officeholder_evidence_url | P3 | URL actually opened |
| 18 | officeholder_evidence_date | P3 | source date, `YYYY-MM-DD` |
| 19 | officeholder_note | P3 | text (e.g. "replaced X, appointed 2025-09") |
| 20 | org_email_final | P2 | the validated/best org email, or empty |
| 21 | org_email_status | P2 | `VALIDATED` / `INFERRED` / `UNVERIFIED` / `CONFLICT` / `DEAD` |
| 22 | org_email_evidence_tier | P2 | integer 1–5 (see section 5) |
| 23 | org_email_evidence_url | P2 | URL actually opened |
| 24 | org_email_evidence_quote | P2 | verbatim on-page text, ≤200 chars |
| 25 | org_email_conflict_note | P2 | text; list all competing values + sources |
| 26 | org_email_confidence | P2 | integer 1–100 |
| 27 | leadership_email_final | P4 | the validated/best leadership email, or empty |
| 28 | leadership_email_status | P4 | `VALIDATED` / `INFERRED` / `UNVERIFIED` / `CONFLICT` / `DEAD` |
| 29 | leadership_email_basis | P4 | `DIRECT_SOURCE` / `CONVENTION_INFERENCE` |
| 30 | leadership_email_evidence_tier | P4 | integer 1–5 |
| 31 | leadership_email_evidence_url | P4 | URL actually opened |
| 32 | leadership_email_evidence_quote | P4 | verbatim on-page text, ≤200 chars |
| 33 | leadership_email_conflict_note | P4 | text |
| 34 | leadership_email_confidence | P4 | integer 1–100 |
| 35 | final_org_email_confidence | P5 | integer 1–100 |
| 36 | final_leadership_email_confidence | P5 | integer 1–100 |
| 37 | open_issues | P5 | text; blank if none |
| 38 | researcher | all | `claude` or `comet` |
| 39 | last_verified_date | all | `YYYY-MM-DD` of the run |

---

## 4. Status definitions (controlled vocabulary)

- **VALIDATED** — The exact email was found on a Tier 1 or Tier 2 source (see section 5). `evidence_url` and `evidence_quote` MUST be present. This is the only status that means "confirmed real."
- **INFERRED** — Not seen directly. Built from a confirmed domain + a naming convention proven by 2+ real samples (Tier 4), or seen only on a Tier 3 source. Usable but not confirmed.
- **UNVERIFIED** — No acceptable evidence found. `*_email_final` is left empty. Do not guess.
- **CONFLICT** — Two or more credible sources disagree. Put every competing value and its source URL in the `conflict_note`. Choose the most recent + most authoritative as `*_email_final`, but keep status = CONFLICT.
- **DEAD** — Evidence the address or domain is defunct (decommissioned domain, page states the address is retired, documented bounce).

---

## 5. Evidence tiers

| Tier | Source type |
|------|-------------|
| 1 | The org's own official website — staff directory, contact page, leadership bio page, on the canonical domain. |
| 2 | An official document — agency PDF, press release, signed letter, government filing, official newsletter. |
| 3 | Reputable third party — LinkedIn, established news outlet, conference/speaker page, government personnel directory not on the org domain. |
| 4 | Convention inference — email not seen directly, but built from a confirmed domain and a naming pattern proven by 2+ real published emails at that domain. |
| 5 | Single-sample pattern or unsupported guess. Not acceptable as a final answer; use only to flag UNVERIFIED. |

---

## 6. Hard rules (low failure tolerance)

1. **No fabrication.** If you cannot find or properly infer an email, status = UNVERIFIED and leave the email empty. Never invent an address to fill a cell.
2. **Every evidence URL must be a page you actually opened in this session.** Do not cite a URL you did not retrieve. Do not construct a plausible URL from memory.
3. **Show the math for every domain.** Naming convention must be backed by 2 real sample emails with their URLs (columns 9–12). One sample = convention_confidence capped per rubric. Zero samples = `NONE_FOUND`.
4. **Confirm the domain independently.** Confirm `canonical_domain` from a published email on the official site, a DNS/MX lookup, or an official document — not from the guessed email in the input.
5. **Officeholder before leadership email.** Confirm who currently holds the role (P3) before validating their email (P4). If the person changed, validate the email for the CURRENT person.
6. **Conflict = record everything.** Never silently pick one of two disagreeing sources. List all in the conflict_note.
7. **Catch-all warning.** Many .gov domains accept any address (catch-all), so "the server accepted it" is NOT proof. Only on-page/document evidence counts. If a domain looks catch-all, set convention/status accordingly and note it.
8. **The input emails are unverified guesses.** Treat columns 8–9 of the input (`listed_org_email`, `listed_leadership_email`) as leads to check, not as truth.

---

## 7. STATE BLOCK (carry-forward, token saver)

At the end of every phase, emit a compact STATE BLOCK so the next phase does not re-derive prior work. Format, one line per record:

```
STATE v<phase>
R01 | dom=OK conv=first.last(92) | office=Y | org=VALIDATED(95) | lead=INFERRED(70) | flags=
R02 | ...
COUNTS: validated_org=NN inferred_org=NN unverified_org=NN conflict=NN | validated_lead=NN ...
```

The next phase prompt will tell the bot to read the STATE BLOCK already in the thread rather than re-paste the full data.
