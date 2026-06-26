# ConnQ — QA Testing Report

**App:** ConnQ Smart Digital Card (com.cloudsathi.connq) v1.0.5
**Prepared for:** Cloud Sathi — QA Intern Assessment
**Date:** June 21, 2026
**Tester:** Amisha Jha

---

## Summary

| Total Scenarios | Bugs Logged | Pass | Fail | Partial | Not Tested |
|----------------|-------------|------|------|---------|------------|
| 30 | 8 | 21 (70%) | 5 (17%) | 2 (7%) | 2 (6%) |

| High | Medium | Low |
|------|--------|-----|
| 2 | 4 | 2 |

---

## Key Findings

**Bug #2 (High) — Silent data loss on save**
"Field of Interest/Work" failed to persist after saving, despite
a "Card updated successfully" confirmation. A success message that
contradicts actual behavior is a trust-breaking issue and was flagged
as the top fix priority.

**Bug #7 (High) — Emoji input crashes save flow**
Entering an emoji in the Full Name field blocked the entire save
operation with a generic error, pointing to missing input sanitization
on the backend.

**Bug #4 (Medium) — Analytics blind spot**
"Call" and "Save to Gallery" interactions were not tracked in the
Insights panel despite being core networking actions — especially
significant since an outbound call is arguably the highest-value
lead conversion for a business card app.

**Bug #6 (Medium) — Generic link previews**
Shared profile links generate Open Graph metadata with generic
"ConnQ" branding rather than the card owner's name and photo,
weakening the sharing experience that is central to the app's value.

---

## Testing Approach

Testing was conducted primarily on a physical Android device, with
iOS used for cross-platform QR scan and sharing verification.
Beyond the assigned scenario list, additional exploratory checks
were performed: dark mode persistence, settings screen completeness,
Open Graph metadata inspection via direct URL fetch, and a
billing/PRO trial flow.

Two scenarios (per-field privacy controls) could not be tested
because the feature referenced in the app's own marketing copy
was not locatable anywhere in the UI — flagged as a product-level
clarification item rather than a standard bug.

---

## Full Report

[Download PDF](./bug-report.pdf)

---

## Files
- `bug-report.pdf` — Full formatted report with all 30 scenarios and 8 bug entries
- `test-scenarios.md` — Test scenario table for quick reference
