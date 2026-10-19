# Agent Skills

A growing collection of reusable AI agent skills for **product management, customer discovery, strategy, and competitive intelligence**.

Each skill provides a structured workflow designed to produce clear, actionable outputs. Skills can be used independently and adapted to different products, markets, and teams.

## Available skills

| Skill | What it does |
| --- | --- |
| [Customer Pain Point Analyzer](customer-pain-point-analyzer/README.md) | Extracts evidence-based customer pain points from interview transcripts, distinguishing underlying needs from feature requests. |
| [Strategic Document Builder](strategic-document-builder/README.md) | Builds structured, evidence-based product strategy documents connecting customer problems, business goals, strategic choices, and execution. |
| [Competitive Intelligence Analyzer](competitive-intelligence-analyzer/README.md) | Researches any competitors in any industry, tracking product developments, official content, customer sentiment, and strategic implications. |

## How to use

1. Open the skill you want to use.
2. Read its `README.md` for an overview and example prompt.
3. Follow its `SKILL.md` instructions, or install the skill in an AI agent that supports the [Agent Skills](https://agentskills.io/) convention.
4. Provide the relevant inputs (for example, interview transcripts, product research, or competitor names).

Each skill is self-contained. Check its instructions for any required research access, inputs, or output files.

## Repository structure

```text
agent-skills/
├── customer-pain-point-analyzer/
│   ├── SKILL.md
│   └── README.md
├── strategic-document-builder/
│   ├── SKILL.md
│   └── README.md
├── competitive-intelligence-analyzer/
│   ├── SKILL.md
│   ├── README.md
│   └── competitors-status.md
└── README.md
```

## Principles

- **Evidence over assumptions:** Separate verified findings from hypotheses.
- **Actionable outputs:** Focus on decisions and next steps, not just summaries.
- **Reusable workflows:** Adapt skills to different industries and contexts.
- **Transparent limitations:** Make missing information and uncertainty explicit.

## Privacy

Review inputs for confidential customer information, internal plans, and sensitive commercial data before sharing them with AI tools or publishing generated outputs.
