---
name: customer-pain-point-analyzer
description: Analyze customer interview transcripts to identify and rank up to five evidence-backed customer pain points, distinguish underlying needs from feature requests, and draft outcome-focused user stories. Optionally deduplicate and update tickets when authorized.
---

# Customer Pain Point Analyzer

## Objective
Analyze a customer call transcript (Markdown or plain text) and identify **up to five validated customer pain points**. Focus on underlying operational needs, not requested solutions.

## Inputs
- Required: customer call transcript.
- Optional: customer name, interviewer names, customer speaker names, technical stack, ticketing destination, and existing ticket list.
- If speaker roles are unclear, ask for clarification or mark attribution as uncertain. **Do not treat every unidentified speaker as a customer.**

## Speaker attribution
Extract pain points only from statements attributable to customers. Interviewer questions, interpretations, and proposed solutions are not customer evidence unless explicitly confirmed by the customer. Do not infer customer roles from names alone.

## Customer context
Identify the customer's role/persona and technical environment **only when supported by the transcript**. Otherwise state `Not established in transcript`.

## Validation criteria
A valid pain point reflects a concrete operational difficulty, such as:
- Frustration, inefficiency, or repetitive manual work
- Delays, risk, poor visibility, or reliability problems
- Scaling constraints or observability gaps

Statements such as “we have to,” “we end up manually,” “we don't have visibility,” or “it takes too long” can be useful signals, but **phrasing alone is not validation**. Requests such as “I want” or “it would be great if” require evidence of an underlying problem.

Exclude unsupported feature requests, solution-only statements, and generic opinions. Do not invent details.

## Analysis process
1. Identify customer speakers and distinguish them from interviewers.
2. Extract evidence of current behavior, workarounds, consequences, and desired outcomes.
3. Cluster related statements into distinct underlying problems; avoid duplicate pain points.
4. Rank validated pain points by **frequency, intensity, and business impact**. Do not equate repeated interviewer prompts with customer frequency.
5. Return **at most five**. If fewer are validated, return fewer. If none are validated, state: `Pain point not clearly validated in this call.`
6. For each, write an outcome-focused user story: `As a [type of user], when [context], I need [capability], so I can [business outcome].`
7. Include a short verbatim customer evidence quote or precise transcript reference where available. Do not fabricate quotations.
8. Distinguish confirmed business impact from plausible but unconfirmed implications.

Avoid solution bias. Do not prescribe UI elements or technical implementations unless they are explicitly stated as constraints and relevant to the problem.

## Ticket workflow (optional)
**Default: analysis only. Do not create or modify tickets unless explicitly requested and authorized.**

If ticket access and a destination are available:
1. Retrieve existing tickets in the target group or board.
2. Compare the underlying problem, not just the title, against existing tickets.
3. If substantially similar, propose appending the new user story with `Additional validation from [Customer Name]` (when known).
4. Otherwise propose a new short, problem-oriented, outcome-focused title.
5. Present the proposed actions for confirmation before any writes, unless the user has explicitly approved automatic ticket creation/updates.
6. After execution, report actual ticket links and outcomes. Never claim an action succeeded without tool confirmation.

If the ticket system is not connected, show `Proposed: Create new ticket`, `Proposed: Append to existing ticket`, or `Deduplication not checked` as appropriate; never imply a ticket was created.

## Required output
Repeat this structure for each validated pain point:

### Pain Point N – [Short problem-oriented title]
**Customer Call Source:** [Customer name or unknown]
**Customer technical stack and persona:** [Supported context or not established]

**User Story:**
As a [type of user], when [context], I need [capability], so I can [business outcome].

**Current Behavior:** [Evidence-based description]

**Desired Behavior:** [Desired outcome, not a presumed feature]

**Root Problem:** [Core unmet need]

**Business Impact:** [Confirmed impact; label any inference]

**Customer Evidence:** [Short quote or transcript reference]

**Ticket Action:** [Proposed action, verified completed action, or `Deduplication not checked`]

## Quality checks
- No interviewer-only claims treated as customer validation.
- No more than five pain points; fewer when evidence is weak.
- No fabricated persona, stack, impact, quote, or ticket status.
- Pain point titles describe problems, not features.
- Ticket writes require authorization and real tool access.
