# Competitive Intelligence Analyzer

An Agent Skill for monitoring **Bigeye, Monte Carlo, Acceldata, and Anomalo** and maintaining an evidence-based data observability competitive intelligence report.

## What it does

- Tracks up to **10 recent product releases or highlighted features** per competitor, with dates and direct source links.
- Summarizes the **5 latest official blog or LinkedIn posts** per competitor.
- Analyzes **Reddit sentiment**, recurring praise and complaints, and emerging discussions, while flagging thin evidence.
- Synthesizes each competitor's **product, content, and positioning strategy**.
- Converts research into **actionable product management implications** and updates `competitors-status.md`.

## Competitors and starting sources

| Competitor | Source |
| --- | --- |
| Bigeye | [Blog](https://www.bigeye.com/blog) |
| Monte Carlo | [Changelog](https://docs.getmontecarlo.com/changelog) |
| Acceldata | [Documentation](https://docs.acceldata.io/) |
| Anomalo | [Website](https://www.anomalo.com/) |

## Example prompt

> Use the competitive-intelligence-analyzer skill to research Bigeye, Monte Carlo, Acceldata, and Anomalo. Update competitors-status.md with recent releases, blog posts, Reddit sentiment, and actionable competitive insights. Cite every source and flag missing evidence.

## Files

- [SKILL.md](SKILL.md) — full instructions and research quality requirements
- [competitors-status.md](competitors-status.md) — report starter template; **not a completed research report**

## Notes

The skill requires access to current public sources. It does not treat an undated product highlight as a new release or infer Reddit sentiment when there is too little discussion.
