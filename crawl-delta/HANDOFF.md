# Handoff note: evidence, unknowns and next checks

Use this optional note alongside a Crawl Delta HTML or JSON report to keep the supplied evidence and the next review step together.

[Watch the 16-second illustrated handoff and inspect the exact sample files](https://crawl-delta-lab-20261018.takahiro0328k.chatgpt.site/assets/crawl-delta-report-first). The video uses fictional CSVs and actual comparison-core findings; it is not a screen recording or a customer result.

The note is manual. It does not run checks, verify a live fix, approve a release or prove that a report was delivered.

## Blank note for a private review

Put this block in your own working document. Keep real project URLs, report labels, file references and assignees private. **Do not paste a completed note or client files into the public feedback form.** Leave unavailable information as unknown rather than zero or complete.

```text
Review label / date: [fill in privately]
Earlier export reference and date: [local reference / unknown]
Later export reference and date: [local reference / unknown]
Comparable crawl scope and settings: [checked / differs / unknown]
Basis for that scope assessment: [what was checked / not checked]

Evidence bundle: [local HTML/JSON report reference]
URLs before / after: [counts / unknown]
Change records: [count / unknown; not unique pages]
Evaluation coverage and missing fields: [report coverage / unknown]

Observation needing a decision: [supplied-export evidence]
What that observation does not establish: [boundary]
Next evidence to check: [specific check / undecided]
Next reviewer or assignee: [fill in privately / unassigned]
Follow-up status: [not checked / checked with evidence / unknown]
Evidence for a completed follow-up: [local reference / none yet]

Sharing decision: [share with stated caveats / hold for a check / not reviewed]
Reason and unresolved observations: [write explicitly]
```

## Filled context: the existing fictional example

This section uses the repository's [before CSV](examples/before.csv), [after CSV](examples/after.csv) and actual generated [JSON report](examples/sample-report.json). [Inspect the rendered HTML](https://crawl-delta-lab-20261018.takahiro0328k.chatgpt.site/examples/sample-report.html).

| Note field | Supplied example evidence |
| --- | --- |
| Input kind | Fictional CSV fixture; not an untouched native crawler export |
| Real crawl scope/settings | Not evaluated; the fixture does not establish a production crawl configuration |
| URLs before / after | 3 / 3 |
| Change records | 5: two `resolved_rule`, one `status_changed`, one `added_to_export`, one `absent_from_export` |
| HTTP-status coverage | 3/3 before and 3/3 after |
| Title / description coverage | Each 2/3 before and 3/3 after |
| Follow-up assignee | Unassigned in this fictional exercise |
| Review decision | Share the supplied evidence with its caveats; withhold a site-wide all-clear |

The two rule-now-clear records concern the supplied title and HTTP-error checks. They do not certify a release, a live fix or a ranking outcome. The `/about` URL has both a rule-now-clear record and a status-change record. Five records do not mean five distinct pages.

### Keep the remaining checks explicit

| Supplied observation | Next evidence to check | Handoff status |
| --- | --- | --- |
| `/new` appears only in the later export and its addition record includes a missing description | Confirm comparable crawl coverage, then check whether the blank description is intended in the relevant page context | Needs reviewer check |
| `/old` is absent from the later export | Check crawl scope/settings and the intended URL treatment; absence in a file is not proof of live deletion | Needs reviewer check |
| Metadata coverage differs between exports | Keep the evaluated-row counts with the report; an unevaluated row is not an issue proved clear | Context retained |

There is no separate `new_issue` record for the added page's missing description in this fixture. [Read the five-record walkthrough](WORKFLOW.md) instead of treating the note as another analysis result.

A later status of 0/unknown needs a different conclusion: retain the earlier check as **Cannot re-evaluate**, not fixed. See the [separate one-URL unknown-status example](https://crawl-delta-lab-20261018.takahiro0328k.chatgpt.site/assets/crawl-delta-unknown-status.html); do not merge its three records with this fixture's five.

## What still needs manual work?

If the note leaves a recurring task unresolved, [describe the general workflow, current workaround and missing outcome](https://github.com/gyomu-ai-sekkei/auto-saas-project/issues/new?template=crawl-delta-workflow.yml). Say whether you used your own CSVs or only read an example, and how often the task repeats. It is fine to say the free tool is sufficient.

Posting requires GitHub sign-in and creates a public issue. Do not include completed notes, CSVs, client URLs, personal/client information, credentials or private screenshots. Reading this note and [trying the browser tool](https://crawl-delta-lab-20261018.takahiro0328k.chatgpt.site/#workspace) require no account. A self-report is not independently verified use, time saved or a purchase. No private support, response time or future feature is promised.
