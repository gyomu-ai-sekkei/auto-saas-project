# Crawl Delta — local SEO crawl CSV comparison examples

Compare two comparable crawl CSV exports, review the evidence, and keep an HTML or JSON change report.

**[Try the free worked example](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/?example=release-check#results)** · **[Get the same offline toolkit for $0+](https://gyomuuser.gumroad.com/l/vyxxt)**

This repository contains fictional CSVs, an actual generated JSON report, and a reproducible review workflow for technical SEOs and small agencies. It is published by the maker of Crawl Delta.

## See the workflow

[Watch the 16-second illustrated release check](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/assets/crawl-delta-404-to-200-en.mp4): the fictional `/about` page changes from HTTP 404 to 200, then the reviewer saves a portable report. This is an illustration, not a screen recording or customer result.


## When a status is unknown

A later export with an unknown HTTP status does not establish that an earlier error was fixed. Use this separate, fictional example to keep the next check explicit in a handoff.

1. [Watch the 18-second illustrated example and inspect its files](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/assets/crawl-delta-unknown-status.html). It is an illustration, not a screen recording or customer result.
2. Save the exact [before CSV](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/assets/crawl-delta-unknown-status-before.csv) and [after CSV](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/assets/crawl-delta-unknown-status-after.csv), then choose them in the [free browser tool](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/#workspace).
3. Compare the output with the generated [HTML report](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/assets/crawl-delta-unknown-status-report.html) or [JSON report](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/assets/crawl-delta-unknown-status-report.json).

Each file contains **one URL**, `https://example.test/about`: status `404` before and `0` after. The report contains **three change records for that same URL**: `not_evaluated` for the earlier HTTP-error check, `new_issue` for the unknown status, and `status_changed`. There is no `resolved_rule` record. Status 0 is treated as unknown here; confirm what it means in your own export.

Save the report to show what still needs follow-up, then recheck the URL using your usual workflow. Crawl Delta does not perform that live recheck or establish a successful deployment.

If this leaves a recurring handoff step manual, [describe the general workflow, current workaround and missing outcome](https://github.com/gyomu-ai-sekkei/auto-saas-project/issues/new?template=crawl-delta-workflow.yml). Posting requires GitHub sign-in and is public. Do not include CSVs, client URLs or other private information; reading the example and using the tool require no account.


## Prepare the next handoff

[Use the review-note template](HANDOFF.md) to keep input references, evaluation coverage, unresolved observations and the next reviewer/check together. It includes a blank note for your private review and filled context for the existing fictional three-URL/five-record example.

[Watch the 16-second illustrated handoff and inspect its exact samples](https://crawl-delta-lab-20261018.takahiro0328k.chatgpt.site/assets/crawl-delta-report-first). This is an illustration with actual core-generated findings from fictional CSVs, not a screen recording or customer result.

The note is manual: it does not verify a live fix, approve a release or prove delivery. Keep completed notes and client data private; use the existing public feedback form only for a general workflow.


## Reproduce a crawl-export comparison

1. Download [before.csv](examples/before.csv) and [after.csv](examples/after.csv). On a GitHub file page, choose **Download raw file**; a ZIP of this repository is also available from **Code → Download ZIP**.
2. Open the [free browser tool](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/#workspace).
3. Select the two downloaded CSV files and choose **Compare exports**.
4. Review the evidence and choose **Download HTML report** or **Download JSON**. Compare the JSON with [sample-report.json](examples/sample-report.json), or [open the rendered sample HTML](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/examples/sample-report.html).

These files contain three URLs per export and produce **five change records**, not five unique pages. [Read the expected result](WORKFLOW.md).

The tool's separate built-in worked example contains four URLs per export and seven change records. It also includes `/about` changing from 404 to 200, but it is a different fixture. The older multi-URL examples use `example.com`; the separate one-URL unknown-status example uses `example.test`. None are customer data.

## Bring your own exports

- Comma-separated UTF-8 CSV. Required English headers: `Address` and `Status Code`.
- Selected metadata checks also require `Content Type` and the corresponding `Title 1` or `Meta Description 1` column.
- Up to 2 MiB and 10,000 data rows per file. Duplicate URLs and malformed rows are rejected.
- Use comparable crawl scope, settings and URL formats. URLs match exactly after surrounding whitespace is stripped.
- Missing optional metadata is unevaluated, not empty or fixed. An absent URL is not proof of deletion.

[Full CSV guide](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/compare-crawl-csv/)

CSV contents and report labels stay in the tool's browser tab. The tool does not crawl live sites, measure rankings or compare every content edit. Hosting services may process ordinary page-access logs. Automated and DOM-simulation checks have passed; real-browser file-picker behavior and every native crawler export have not been independently verified.

## Tell us which repeated reporting step is hard

[Open the public workflow-feedback form](https://github.com/gyomu-ai-sekkei/auto-saas-project/issues/new?template=crawl-delta-workflow.yml). A GitHub account is needed to post an issue; reading these examples and trying the browser tool requires no account.

Say whether you used the tool or only reviewed the example, which task repeats, how often it occurs, and what outcome is missing. It is fine to say that the free tool is sufficient. Stated intentions or willingness to pay are not verified use or a purchase.

**Issues are public. Do not post CSV files, client or personal data, client URLs, passwords, keys, screenshots with private details, or other confidential information.** No private support, response time or future feature is promised.

## Download the same offline toolkit without checkout

**[Download the free ZIP](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/assets/crawl-delta-free-evaluation.zip)** · [Version0.2.2 release notes](https://github.com/gyomu-ai-sekkei/auto-saas-project/releases/tag/crawl-delta-evaluation-v0.2.2)

Unzip it, open `crawl-delta-offline.html`, and try the worked example or choose two comparable CSV files. No GitHub/Gumroad account, checkout, Python or API key is needed for this download or the tool. The file is the same11,050-byte evaluation ZIP provided on Gumroad; optional payment there adds no features. SHA-256: `00d636ffb3bf0757642c9d6a894473326002f09200f5e4bd8a90b423aa77008e`.

The ZIP includes the runnable HTML, its existing README and fictional CSVs. Hosting providers may process ordinary page/download requests. We do not have a central count of completed downloads or use. Reports stay on your device; review them before sharing.

## Free and optional payment

The [offline ZIP on Gumroad](https://gyomuuser.gumroad.com/l/vyxxt) starts at $0. Enter 0 to get it free; $9 is a suggested optional one-time payment. Paying adds no extra features, custom support or promised updates. There is no subscription. Optional payments have the stated 30-day refund-request policy.

The crawl-delta directory contains examples and workflow documents; the separately hosted offline ZIP contains the runnable HTML tool. Existing software-use terms remain in effect. There is no separate right to resell or redistribute the software. Mandatory consumer rights remain unaffected.
