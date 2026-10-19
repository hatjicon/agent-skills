---
name: competitive-intelligence-analyzer
description: Research any competitors in any industry, track recent product developments and content, assess customer sentiment, and maintain a sourced competitive intelligence report.
---

# Competitive Intelligence Analyzer

## Purpose

Build an evidence-based, actionable competitive intelligence report for **any industry, market, product, service, or competitor set**. Never assume a particular sector or hard-code vendors.

## Inputs

Accept whatever the user provides, including:
- **Competitors:** names, product names, websites, documentation, release notes, blogs, social profiles
- **Industry and market context:** optional; infer cautiously from supplied sources and verify
- **Research goals:** product positioning, capabilities, pricing, distribution, partnerships, customer sentiment, etc.
- **Sentiment sources/search terms:** optional Reddit queries, review sites, forums, social communities, or other appropriate public channels
- **Time horizon and counts:** default 90-day lookback, up to 10 latest product developments and 5 latest official posts per competitor; user overrides take precedence

If competitor names or websites are provided, use them directly; do not replace them with a fixed competitor list. If no competitors are supplied, identify relevant candidates only if the user requests discovery; otherwise ask for the essential competitor/market scope.

## Research methodology

### 1. Recent product and business developments (default: 10 per competitor)

Use the most appropriate primary sources: official release notes, changelogs, documentation, product pages, app store updates, newsroom, filings, press releases, and launch posts. Depending on industry, developments may be **features, products, services, pricing changes, integrations, partnerships, geographic launches, or business-model changes**.

For each development capture:
- **Name**
- **Description:** what changed and why it matters to customers
- **Date:** verified release/announcement date or `Not disclosed`
- **Status:** Released / Announced / Highlighted (not necessarily new)
- **Direct source URL**

Sort confirmed dates newest first; undated highlights last. Never label an evergreen capability a recent release. If fewer than the requested number are verifiable, report the actual number and evidence gap. Do not fabricate.

### 2. Recent official content (default: 5 posts per competitor)

Find the most recent substantive content from official blogs, newsrooms, LinkedIn pages, video channels, or industry-appropriate owned channels. Capture:
- **Title**
- **Author:** named author or `Not listed`
- **Publication date:** verified or `Not disclosed`
- **Channel**
- **Summary:** 2–3 sentences covering key message and strategic significance
- **Direct URL**

Distinguish thought leadership and marketing claims from product evidence. Sort by verified date descending; note access gaps.

### 3. Customer/user sentiment

Choose channels relevant to the **industry and audience**. Search Reddit where relevant, plus suitable product review sites, app store reviews, professional communities, forums, developer discussions, or public social posts. User-specified sources take priority. Do not force Reddit when meaningful conversations happen elsewhere.

Capture search terms, sources, search date, lookback, and approximate count of relevant independent discussions/reviews. Exclude unrelated name matches, duplicate threads, spam, paid promotions, and vendor-authored posts masquerading as user feedback.

Report:
- **Sentiment:** Predominantly positive / Mixed / Predominantly negative / Insufficient evidence
- **Positive themes:** recurring patterns with direct evidence links
- **Negative themes:** recurring patterns with direct evidence links
- **Emerging topics:** novel or growing topics with dates and links
- **Evidence quality:** distinguish firsthand experience from hearsay, and explain sampling bias

Do not invent numeric sentiment scores or claim representative consensus from a handful of posts. If no meaningful user discourse is available, say `Insufficient evidence`.

### 4. Apparent competitor strategy (150–250 words per competitor by default)

Synthesize **product/service focus, target segments, go-to-market and content themes, market positioning, strengths and weaknesses in public discourse, and plausible future directions**. Adapt to the sector: e.g., distribution and merchandising for retail, compliance for financial services, developer experience for software, or clinical workflow for healthcare.

Separate verified facts, third-party opinions, and your own hypotheses. Support material claims with direct links. Label forward-looking inferences and confidence.

### 5. Actionable implications

For each competitor:
- **Moves to watch** (up to 3)
- **Differentiation opportunities or strategic hypotheses** (up to 3), each with evidence and confidence
- **Customer discovery questions** (up to 3)
- **Changes since previous report** when available

Close with cross-competitor patterns, risks, opportunities, and an executive summary tailored to the user's stated goals.

## Workflow

1. Open the existing output file if available. Preserve useful previous findings and update history; otherwise create it from the template.
2. Establish competitor scope, industry, research date, time horizon, requested counts, and relevant evidence channels.
3. Verify official developments and content with direct sources; avoid assuming websites are current or comprehensive.
4. Research independent user discussions in channels suited to the industry; verify relevance and deduplicate.
5. Compare competitors consistently while acknowledging differences in source coverage.
6. Write each competitor section and cross-competitor synthesis with links for factual claims.
7. Update `competitors-status.md` (or requested path) when write access exists. If write access is unavailable, provide the full Markdown without claiming an update.
8. Explicitly document missing sources, uncertainty, incomplete counts, and research limitations.

## Output template

```markdown
# Competitive Intelligence Report
**Last researched:** YYYY-MM-DD
**Industry / market:** ...
**Coverage window:** ...
**Competitors:** ...

## Executive summary
...
## Cross-competitor trends
...

## [Competitor name]
### Latest product and business developments
| Development | Description | Date | Status | Source |
| --- | --- | --- | --- | --- |
### Latest official content
| Title | Author | Date | Channel | Summary | URL |
| --- | --- | --- | --- | --- | --- |
### Customer/user sentiment
**Assessment:** ...
**Evidence base and channels:** ...
**Positive themes:** ...
**Negative themes:** ...
**Emerging topics:** ...
### Apparent strategy
[150–250 words; separate observations and hypotheses]
### Strategic implications
...
### Gaps and confidence
...

[Repeat for every competitor]

## Sources and methodology
...
## Changes since previous update
...
```

## Quality requirements

- **Industry-agnostic:** no default competitors, technologies, markets, or sentiment platforms.
- **Evidence first:** link to direct sources; do not invent names, dates, authors, quotes, URLs, or sentiment.
- **Accurate recency:** distinguish released vs announced vs merely highlighted.
- **Meaningful comparisons:** tailor dimensions to industry and the user's decision.
- **Cautious inference:** label predictions as hypotheses and state confidence.
- **Transparent limitations:** sparse coverage is a finding, not permission to fill gaps.
