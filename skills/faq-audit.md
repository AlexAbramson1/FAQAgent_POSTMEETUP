# FAQ Audit: check FAQ content against live Align functionality

## Purpose
Check FAQ entries in knowledge/ against Align's actual, current functionality, and produce a pass/fail report with recommended fixes.

## When to use
Alex asks to run, resume, or check the FAQ audit, or references a specific FAQ entry or section by name.

## Steps
1. Read the target FAQ entry (or entries) from `knowledge/Align_Platform_Help_Doc.txt` (and `knowledge/FAQ Updates - 2026 - Sheet1.pdf` once it can be extracted).
2. Identify the entry's referenced live page URL and the specific claims it makes: navigation paths, feature names, button labels, steps.
3. Browse the live page read-only via the browser tool to verify those claims. If it hits a login wall, ask Alex to log in himself in that session; do not guess at what's behind the login.
4. Compare the FAQ's described steps and claims against what the live page actually shows.
5. Assign the entry a pass or fail.
6. On fail, draft the specific corrected wording, quoting what's wrong and what it should say instead.
7. Where a value-statement or benefit line would strengthen the entry, suggest one.
8. Note any formatting tightening, independent of pass/fail (redundant text, overlong steps).
9. Compile results into `deliverables/faq-audit-YYYY-MM-DD.md`: a markdown table with columns Entry | URL | Pass/Fail | Findings | Recommended Update | Value-Statement Suggestion. Append to the same day's file if run multiple times in one day.
10. Update `memory/working.md` with audit progress: entries done so far out of the total in the help doc.

## Output format
A markdown report in `deliverables/`, one table row per entry audited, plus a one-line note in working memory on progress.

## Keep current
When Alex corrects this output, update this file in the same session so the correction sticks.
