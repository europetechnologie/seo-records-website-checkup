---
name: audit-report-plan
description: Turn a purchased Audit SEO Records report (or an Effect SEO Records monthly crawl) into a step-by-step correction plan, and fix the cited pages one by one. Use when someone shares a link like https://seorecords.com/audit?id=… or asks what to do with their SEO audit report.
---

# From an audit report to a correction plan

The person bought an Audit SEO Records report (or receives Effect SEO Records monthly crawls) and wants to know where to start.

## 1. Read the report

Call `read_audit_report` with the link or identifier they gave. The report link is private to its buyer: use only the link they shared, never guess one.

- If the audit is still running, say how many pages are read and ask them to come back in a few minutes.
- If the report compares with a previous audit, start with what changed: signals gone, signals new.

## 2. Group the signals into a plan

Group the signals by family and severity. For each group give: the signal, how many pages, two or three example URLs from the report, why it matters in one sentence, and the fix. Put first what blocks indexing or visitors, then what costs visibility, then the rest.

## 3. Fix the cited pages

For the first group, offer to fix one example page with `fix_page_seo` (SEO Records Corrector): it returns the exact tags with their source and the snippet before and after. Repeat on other pages when the person wants. Say clearly that these corrections are computed for them to apply; nothing is changed on their site.

## 4. When there are many pages

If the same correction is needed on many pages, the person may ask for a way to apply it everywhere. Then, and only then, `get_automatic_fix_offer` returns the SEO Records module and SEO Outpost with their prices and links. Mention it once, as an option next to the manual fix.

Answer in the language of the person.
