# Worked example: review a site-release change report

Use the two fictional CSV files in `examples/`. Keep the earlier and later crawl scope and settings comparable before interpreting results.

## Expected output

Three URLs before and three URLs after produce five change records:

| URL | Record | Evidence |
| --- | --- | --- |
| `https://example.com/` | Title rule now clear | Blank → `Example`, on comparable HTTP 200 HTML rows |
| `https://example.com/about` | HTTP-error rule now clear | HTTP 404 → 200 |
| `https://example.com/about` | Status changed | HTTP 404 → 200; the same URL has a second record |
| `https://example.com/new` | Added to export | New in the later export; its blank description is included in this addition record |
| `https://example.com/old` | Absent from export | Missing from the later export; check crawl scope before inferring deletion |

The report has two `resolved_rule`, one `status_changed`, one `added_to_export`, and one `absent_from_export` record. It has no separate `new_issue` record for the added page's missing description.

Title and description coverage is 2/3 URLs before and 3/3 after. The earlier HTTP 404 row is not evaluated for blank HTML metadata. Counts are evaluated rows, not a promise that every SEO issue has been checked.

## Keep and share the evidence

After comparing the CSVs in the browser tool, save HTML or JSON. The HTML is standalone and can be reviewed or shared with a client. Review the supplied URLs and report label before sharing. A change report is a review aid; check the underlying evidence before acting.

This example does not establish that a site was crawled live, a fix was deployed, traffic improved, or rankings changed. It is fictional data demonstrating the report format. [Rendered sample report](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/examples/sample-report.html).

If this leaves a repeated step unresolved, use the public feedback form linked from the README. Describe the task without URLs, files or personal/client information.
