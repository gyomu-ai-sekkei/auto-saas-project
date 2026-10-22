# Crawl Delta — local SEO crawl CSV comparison examples

Compare two comparable crawl CSV exports, review the evidence, and keep an HTML or JSON change report.

**[Try the free worked example](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/?example=release-check#results)** · **[Get the same offline toolkit for $0+](https://gyomuuser.gumroad.com/l/vyxxt)**

This repository contains fictional CSVs, an actual generated JSON report, and a reproducible review workflow for technical SEOs and small agencies. It is published by the maker of Crawl Delta.

## See the workflow

[Watch the 16-second illustrated release check](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/assets/crawl-delta-404-to-200-en.mp4): the fictional `/about` page changes from HTTP 404 to 200, then the reviewer saves a portable report. This is an illustration, not a screen recording or customer result.

## Reproduce a crawl-export comparison

1. Download [before.csv](examples/before.csv) and [after.csv](examples/after.csv). On a GitHub file page, choose **Download raw file**; a ZIP of this repository is also available from **Code → Download ZIP**.
2. Open the [free browser tool](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/#workspace).
3. Select the two downloaded CSV files and choose **Compare exports**.
4. Review the evidence and choose **Download HTML report** or **Download JSON**. Compare the JSON with [sample-report.json](examples/sample-report.json), or [open the rendered sample HTML](https://crawl-delta-lab-20261018.feyreed64.chatgpt.site/examples/sample-report.html).

These files contain three URLs per export and produce **five change records**, not five unique pages. [Read the expected result](WORKFLOW.md).

The tool's separate built-in worked example contains four URLs per export and seven change records. It also includes `/about` changing from 404 to 200, but it is a different fixture. All example URLs use `example.com`; none are customer data.

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

## Free and optional payment

The [offline ZIP on Gumroad](https://gyomuuser.gumroad.com/l/vyxxt) starts at $0. Enter 0 to get it free; $9 is a suggested optional one-time payment. Paying adds no extra features, custom support or promised updates. There is no subscription. Optional payments have the stated 30-day refund-request policy.

This examples repository does not contain the comparison tool's source or change its software-use terms. Use the published browser tool or obtain the offline ZIP through the links above. There is no separate right to resell or redistribute the software. Mandatory consumer rights remain unaffected.
