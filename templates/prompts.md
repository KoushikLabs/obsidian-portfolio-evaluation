---
type: template
title: "Reusable Claude Prompts for Portfolio Evaluation"
tags: [template, prompts, ai, ai-in-evaluation]
created: 2026-06-19
updated: 2026-06-19
---

# Reusable Claude Prompts for Portfolio Evaluation

Copy-and-adapt prompts for drafting portfolio evaluation plans, rubrics,
syntheses, and briefs for a *specific* funder or incubator. Replace every
`«placeholder»`.

**How to get the best results**
- Give Claude the context files: point it at this knowledge base (the
  [[methods/methods-index|methods]], the [[external-sources/norad-portfolio-mel-guide-summary|Norad summary]],
  the relevant [[templates/templates-index|template]]).
- Always ask for **contribution, not attribution** claims, and for **confidence
  levels**.
- Treat Claude's output as a **draft for an evaluator to judge** — keep evaluative
  judgement, contribution claims, and quality-of-evidence calls with the human
  (the lesson from the [[case-studies/A0248-A0249-ai-in-evaluation-masterclasses|AI-in-evaluation sessions]]).

---

## 1. Draft a portfolio evaluation framework for a specific funder

```
You are an evaluation adviser specialising in portfolio-level evaluation for
funders and incubators. Draft a portfolio evaluation framework for:

- Funder/incubator: «name + what they are»
- The portfolio: «number & type of grants/ventures, sectors, geographies, stage
  spread, total value, timeframe»
- Their strategic intent / what the portfolio is meant to achieve: «…»
- Decisions they need the evaluation to inform: «…»
- Budget & appetite: «one-off study / recurring / standing function; rough budget»

Follow the structure of the portfolio evaluation framework template (purpose →
portfolio theory of change → two-level evaluation questions → criteria & rubric →
synthesis method → data foundation → learning & use → workplan). 

Constraints:
- Keep project-level and portfolio-level questions clearly separate.
- Use contribution logic, not attribution. Flag where attribution is impossible.
- Recommend a fit-for-purpose "bricolage" of methods and JUSTIFY each choice.
- Explicitly decide whether to use OECD-DAC criteria and explain why/why not.
- Address how you'll handle heterogeneity (e.g. buckets of indicators + rubric).
Output as markdown. Mark anything you're inferring vs. what I told you.
```

## 2. Draft a portfolio-level theory of change

```
Help me articulate a PORTFOLIO-level theory of change (not project-level) for
«funder/portfolio». Here are the interventions and what each does: «list».
Here is the higher-level objective: «…».

Produce: (a) the high-level portfolio objective(s); (b) how the portfolio sits
within and contributes to the broader system; (c) 3–6 intervention clusters and
how they reinforce each other; (d) the funder's intended contribution and system
entry points; (e) the key portfolio-level assumptions and risks. Keep it
conceptual and strategic, NOT a detailed project logframe. Note where a nested
(country/cluster) ToC structure would help.
```

## 3. Generate portfolio-level evaluation questions

```
Given this portfolio theory of change: «paste ToC», generate portfolio-level
evaluation questions arranged in a matrix of Strategic vs Operational ×
Formative vs Summative (the Norad model). Then recommend the "vital few" (5–7)
to prioritise for an evaluation with «budget/scope», and explain the trade-off.
Keep them answerable; flag any that need data the funder probably doesn't have.
```

## 4. Build an evaluative rubric

```
Build an evaluative rubric for assessing «portfolio» against these criteria:
«list criteria, derived from the ToC». Use a 4-level scale
(Excellent/Good/Adequate/Poor). For EACH criterion × level, write a concrete,
observable word-picture so two assessors would rate the same case the same way.
Then list, per criterion, the evidence needed to justify a rating and a simple
quality-of-evidence test. Remember these are heterogeneous interventions — the
level descriptions must work across very different grants/ventures.
```

## 5. Design a cross-case analysis matrix

```
Design a cross-case analysis matrix to synthesise «N» «grants/ventures» into
portfolio-level patterns. Propose the columns (derived from this ToC and these
evaluation questions: «paste»), explain what each column captures, and explain
how to read the completed matrix for patterns (by cluster, by context, positive
deviance, gaps). Include a credibility checklist. Output as a markdown table I
can fill in.
```

## 6. Synthesise cross-case findings into portfolio-level lessons

```
Here is a completed cross-case matrix / set of case summaries: «paste». Acting as
a careful evaluator: (1) identify portfolio-level patterns (what works, for whom,
in which contexts); (2) surface common enablers and barriers; (3) flag positive
deviance and any negative/null results; (4) draft a portfolio-level CONTRIBUTION
story with explicit confidence levels and named rival explanations; (5) list the
evidence gaps. Be conservative: do not overclaim. Separate "well-evidenced" from
"plausible but thinly evidenced" findings.
```

## 7. Draft a one-page funder brief

```
Turn these portfolio evaluation findings: «paste» into a ONE-PAGE brief for a
non-evaluator audience («board / investment committee / incubator leadership»).
Follow the funder-brief template: bottom line (3 sentences) → what's working /
not / our contribution → the evidence behind it → a decisions table (scale / stop
/ strategy with recommendation, evidence, confidence) → evidence gaps. No
undefined jargon. Lead with the decision, not the method. Show confidence
honestly.
```

## 8. Build an Evidence Gap Map of the portfolio

```
Help me build an Evidence Gap Map of «funder»'s portfolio. Rows = intervention
types: «list». Columns = portfolio outcomes (from the ToC): «list». For each
grant/study I describe, place it in the right cell and code volume + quality of
evidence. Then read off: where evidence is concentrated, where it's thin, and
where we're making under-evidenced bets. Present as a markdown matrix plus a
short "what the gaps mean for strategy" note.
```

## 9. Stress-test a draft portfolio evaluation plan

```
Critique this draft portfolio evaluation plan: «paste». Play three roles in turn:
(1) a skeptical funder who asks "so what / will this change any decision?"; (2) a
methodologist who probes whether the synthesis method can actually bear the
weight of the heterogeneity; (3) a grantee worried about burden and fairness.
For each, give the toughest 3 questions and how I should strengthen the plan.
```

## 10. Adapt the Norad five-step model to an incubator cohort

```
Translate the Norad/Itad portfolio MEL five-step model (portfolio theory of
change → strategic & operational questions → monitoring → evaluations → learning
spaces) for an INCUBATOR/ACCELERATOR evaluating a cohort of «N» ventures over
«timeframe». Where the funder/grant language doesn't fit a cohort of ventures,
adapt it and say what you changed. Suggest cohort-appropriate progress markers
and success definitions (e.g. survival, follow-on funding, learning velocity).
```

---

## Guardrails (apply to every prompt)

- **Human owns the judgement.** Use Claude to draft, structure, synthesise, and
  pressure-test — not to make the final evaluative or contribution claim.
- **Contribution over attribution**, always, at portfolio scale.
- **Surface uncertainty.** Ask for confidence levels and rival explanations.
- **Don't invent evidence.** If Claude lacks data, it should say so, not fabricate
  cases or outcomes.
- **Privacy:** do not paste confidential grantee data or the private
  [[external-sources/external-sources-index|conference slides]] into any external tool
  without authorisation.

---

*Part of the [[index|Portfolio-Level Evaluation knowledge base]].*
