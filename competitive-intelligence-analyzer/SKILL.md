---
name: competitive-intelligence-analyzer
description: Research data observability competitors' latest product releases, official content, and Reddit sentiment; maintain a sourced competitors-status.md intelligence report.
---

# Competitive Intelligence Analyzer

## Goal

Perform comprehensive, current competitive intelligence for the following data observability vendors and update `competitors-status.md` with actionable findings for product management.

| Competitor | Starting source |
| --- | --- |
| Bigeye | https://www.bigeye.com/blog |
| Monte Carlo | https://docs.getmontecarlo.com/changelog |
| Acceldata | https://docs.acceldata.io/ |
| Anomalo | https://www.anomalo.com/ |

Treat these URLs as starting points, not the only permitted sources. Locate each vendor's official release notes, product updates, blog, newsroom, and LinkedIn posts as appropriate. Search Reddit separately for each company and product, including alternative spellings (e.g., "Monte Carlo" + "data observability", "Acceldata", "Bigeye data", "Anomalo"). Exclude unrelated uses of ambiguous terms.

## Research requirements

### 1. Ten latest released or highlighted features per competitor

Find the **10 most recent verifiable** product releases or prominently highlighted features, prioritizing release notes and dated announcements over undated marketing pages. For each record include:

- **Feature name**
- **Description:** what it does and who benefits
- **Release/announcement date:** ISO date if available; otherwise `Not disclosed`
- **Source URL:** direct feature announcement, documentation, or release note
- **Evidence type:** Released / Announced / Highlighted (not necessarily new)

Sort by confirmed date descending, with undated highlights last. Do not describe an undated highlighted capability as a new release. If fewer than 10 verifiable items exist, list only those found and explicitly state the gap. Do not invent feature names, dates, or URLs.

### 2. Five latest official posts per competitor

Find the **5 most recent** posts on the official blog, or official LinkedIn page when blog coverage is absent or stale. Include:

- **Title**
- **Author:** if named, else `Not listed`
- **Publication date:** ISO date if available, else `Not disclosed`
- **Summary:** 2–3 sentences on the message and takeaways
- **URL:** direct link to the post
- **Channel:** Blog / LinkedIn

Sort by verified publication date descending. Distinguish marketing announcements from substantive product updates. If fewer than five are accessible, say so.

### 3. Reddit sentiment

Search Reddit for each competitor and relevant product names; use multiple searches and inspect original threads and comments. Capture the search terms, search date, timeframe, relevant subreddit(s), and approximate number of **relevant** independent discussions reviewed. Filter out unrelated brand mentions, spam, self-promotion, and duplicates.

Report:

- **Sentiment category:** Predominantly positive / Mixed / Predominantly negative / Insufficient evidence
- **Positive themes:** recurring themes with direct Reddit thread links
- **Negative themes:** recurring themes with direct Reddit thread links
- **Emerging topics:** new or growing discussion topics, with links and dates

Do not manufacture a numeric sentiment score. If data is sparse, say `Insufficient evidence` and avoid claiming community consensus. Separate first-hand customer accounts from hearsay and vendor marketing. Reddit is directional qualitative evidence, not a representative sample.

### 4. Overall strategy (150–250 words per competitor)

Synthesize observed product focus, AI/integration investment, target customers, blog/content positioning, and strengths or weaknesses in public discourse. Explicitly distinguish **confirmed observations** from **inferences** about future direction. Cite the underlying releases, posts, and Reddit discussions. Do not infer a roadmap from marketing language alone.

### 5. Actionable product management implications

For each competitor add:
- **Competitive moves to watch** (up to three)
- **Opportunities / differentiation hypotheses** (up to three), with evidence and confidence
- **Questions for customer discovery** (up to three)
- **Change since prior report** when an earlier report exists; preserve prior observations instead of silently replacing history

## Execution workflow

1. Open the existing `competitors-status.md` if present; preserve useful history, previous update date, and established structure. If absent, create it using the template below.
2. Record the current **research date** and a consistent **lookback window** (default 90 days for releases/posts, extend backward only to fill requested counts). Never imply completeness beyond what was actually reviewed.
3. Visit official sources first; use search to locate relevant updates. Verify each item against its direct source and capture publication dates.
4. Search Reddit by vendor and product. Cite original Reddit discussions; avoid counting the same cross-post or thread multiple times.
5. Cross-check recency and duplicates. Prefer explicit dates; never assign today's date to undated content.
6. Write the report for all four vendors, with consistent sections and source URLs for every factual entry.
7. Summarize **cross-competitor patterns** and a concise **executive takeaway** with implications for data observability product strategy.
8. Update `competitors-status.md` in the user's current workspace/repository if write access is available. If not, return the complete Markdown for manual saving; do not claim a file was updated.
9. Note source-access limitations, insufficient Reddit evidence, and any gaps in the requested counts.

## Output file: competitors-status.md

Use this structure:

```markdown
# Data Observability Competitive Intelligence
**Last researched:** YYYY-MM-DD
**Coverage window:** ...
**Competitors:** Bigeye, Monte Carlo, Acceldata, Anomalo

## Executive summary
...
## Cross-competitor trends
...

## Bigeye
### Latest 10 product features
| Feature | Description | Date | Evidence type | Source |
| --- | --- | --- | --- | --- |
### Latest 5 official posts
| Title | Author | Date | Channel | Summary | URL |
| --- | --- | --- | --- | --- | --- |
### Reddit sentiment
**Assessment:** ...
**Evidence base:** ...
**Positive themes:** ...
**Negative themes:** ...
**Emerging topics:** ...
### Apparent strategy (150–250 words)
...
### Product management implications
...
### Gaps and confidence
...

## Monte Carlo
[Repeat same sections]

## Acceldata
[Repeat same sections]

## Anomalo
[Repeat same sections]

## Sources and methodology
...
## Changes since previous update
...
```

## Quality bar

- **No fabricated dates, features, authors, sentiment, or URLs.**
- Each feature/post has a direct source; each Reddit theme links to supporting threads.
- Clearly label release vs announcement vs evergreen feature highlight.
- Do not confuse content recency with product-release recency.
- No unsupported strategic certainty: mark projections as hypotheses.
- Be concise but comprehensive; focus on decisions, not promotional copy.
