# CONFIDENCE RUBRIC — EDC Email Validation

Both bots must score confidence the same way so the two outputs are comparable. Confidence is an integer 1–100. Compute it from three factors: evidence tier, source recency, and (for leadership email) whether the current officeholder is confirmed.

---

## 1. Base score by evidence tier

| Tier | Source | Base score |
|------|--------|------------|
| 1 | Official site (directory, contact, leadership page) | 90 |
| 2 | Official document (PDF, press release, signed letter, filing) | 82 |
| 3 | Reputable third party (LinkedIn, news, speaker page, gov directory off-domain) | 60 |
| 4 | Convention inference backed by 2+ real samples | 55 |
| 5 | Single-sample pattern / unsupported guess | 20 |
| — | Nothing found (UNVERIFIED) | 5 |

---

## 2. Recency adjustment (applied to base)

Based on the date of the strongest supporting source.

| Source age | Adjustment |
|------------|------------|
| 0–12 months | +5 |
| 13–24 months | 0 |
| 25–48 months | −10 |
| 49+ months or undated | −20 |

---

## 3. Officeholder factor (leadership email only)

| Condition | Adjustment |
|-----------|------------|
| Current officeholder confirmed (officeholder_confirmed = Y) within 18 months | +5 |
| Officeholder not confirmed, or last confirmation 19+ months old | −15 |
| Email belongs to a person who appears to have left the role | cap final score at 15 |

---

## 4. Convention confidence (column 13, set in P1)

This scores how reliable the naming pattern is. It feeds Tier 4 inferences.

| Situation | convention_confidence |
|-----------|----------------------|
| 3+ real samples all match one pattern | 90 |
| 2 real samples match one pattern | 75 |
| 2 samples but patterns differ | 40 + note the conflict |
| 1 real sample only | 35 |
| 0 samples found | 5, set naming_convention = NONE_FOUND |
| Domain appears catch-all (pattern unprovable) | 25, set CATCH_ALL_UNKNOWN |

A Tier 4 (inferred) email's confidence cannot exceed its domain's convention_confidence.

---

## 5. Final score

```
score = base (section 1)
      + recency adjustment (section 2)
      + officeholder factor (section 3, leadership only)
```
Clamp to the range 1–100. Apply any caps from sections 3 and 4 last.

Worked example (leadership email):
- Found on the agency's leadership page (Tier 1 → base 90)
- Page dated 4 months ago (+5)
- Current officeholder confirmed last month (+5)
- score = 90 + 5 + 5 = 100

Worked example (inferred org email):
- Not seen directly; domain confirmed; pattern proven by 2 samples (Tier 4 → base 55)
- convention_confidence = 75 → inferred score capped at 75
- Strongest sample dated 8 months ago (+5) → 60, then capped at 75 → 60
- score = 60, status = INFERRED

---

## 6. Score-to-meaning bands (for the end-of-phase summary)

| Band | Meaning |
|------|---------|
| 90–100 | Confirmed on a primary source, current. Safe to use. |
| 75–89 | Strong. Official document or tightly proven inference. |
| 50–74 | Moderate. Third-party source or standard inference. Verify before high-stakes use. |
| 25–49 | Weak. Thin evidence. Treat as a lead. |
| 1–24 | Not usable. Effectively unverified. |
