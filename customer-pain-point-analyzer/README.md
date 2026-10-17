# Customer Pain Point Analyzer

An Agent Skill for turning customer interview transcripts into **up to five validated customer pain points** and outcome-focused user stories, without confusing feature requests for underlying needs.

## What it does
- Separates customer evidence from interviewer prompts.
- Identifies customer persona and technical stack when supported.
- Groups related problems and ranks them by frequency, intensity, and business impact.
- Documents current behavior, desired outcomes, root problems, business impact, and evidence.
- Optionally proposes ticket creation or deduplication; writes require authorization and connected tools.

## Installation
Copy the `customer-pain-point-analyzer` folder, including `SKILL.md`, into the skills directory supported by your AI agent. Consult your agent's documentation for its specific installation path.

## Example prompt
> Analyze this customer interview transcript with the customer-pain-point-analyzer skill. Interviewers are Alice and Bob. Identify only validated customer pain points and draft user stories. Do not create tickets.

## Privacy
Review transcripts for personal data, customer-confidential information, and internal company details before sharing them with an AI tool or publishing outputs.

## Format
Uses the `SKILL.md` convention from [Agent Skills](https://agentskills.io/).
