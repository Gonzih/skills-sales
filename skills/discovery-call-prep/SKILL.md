---
name: discovery-call-prep
description: Prepare for a discovery call with research questions, pain hypothesis, competitor differentiators, and a talk track outline.
triggers: ["prep discovery call", "discovery call prep", "prepare for discovery", "discovery prep", "call prep"]
---

# Discovery Call Prep

## What this skill does
Given a prospect name, company, and deal context, this skill generates a comprehensive discovery call preparation kit. It produces targeted research questions, a pain hypothesis based on industry and role signals, competitor differentiators, and a structured talk track outline to guide the conversation.

## How to invoke
/discovery-call-prep [prospect name] at [company] — [role/context]

## Workflow steps

### Step 1 — Prospect & Company Research Summary
Summarize what is known or inferable about the prospect's company: industry, size, likely tech stack, recent news signals (funding, hiring, product launches), and business priorities. Identify the prospect's role and typical pain points for that persona.

### Step 2 — Pain Hypothesis
Formulate 3–5 pain hypotheses ranked by likelihood. Each hypothesis should follow the format: "We believe [company] is experiencing [pain] because [signal], which is causing [business impact]." These guide the questions you'll ask to confirm or disconfirm.

### Step 3 — Discovery Questions
Generate 10–15 open-ended discovery questions organized by category:
- **Situation** — understand current state and context
- **Problem** — surface pain and urgency
- **Implication** — expand impact of the problem
- **Need-payoff** — connect solution value to their goals

### Step 4 — Competitor Differentiators
List the top 2–3 likely competitors the prospect may be evaluating or currently using. For each, provide 2–3 crisp differentiators that favor your solution, framed as discovery questions or statements you can weave naturally into conversation.

### Step 5 — Talk Track Outline
Produce a time-boxed talk track for a 45-minute discovery call:
- **0–5 min** — Rapport, agenda setting, confirm time
- **5–15 min** — Situation questions, company/role context
- **15–30 min** — Problem and implication questions, pain confirmation
- **30–40 min** — Solution positioning, differentiator moments
- **40–45 min** — Next steps, mutual action plan

## Live Data Sources

- **Crunchbase API** — funding rounds, headcount, investor signals, and company stage. Use `GET /entities/organizations/{permalink}` to pull funding history and employee count for the prospect's company before the call.
- **NewsAPI** (`newsapi.org`) — recent press coverage and company news. Query `GET /v2/everything?q={company}&sortBy=publishedAt` to surface recent announcements, leadership changes, or product launches that can be woven into rapport-building and pain hypotheses.
- **LinkedIn company page patterns** — headcount growth by department (available on the "People" tab without authentication), recent hires in leadership roles, and open job postings as hiring-signal proxies for strategic priorities.
- **BuiltWith technology detection** — tech stack fingerprint for the prospect's domain. Use `GET https://api.builtwith.com/v21/api.json?KEY={key}&LOOKUP={domain}` to identify current tooling, detect gaps your solution fills, and surface integration talking points.

## Example outputs
A structured markdown document with five labeled sections: company summary, ranked pain hypotheses, categorized discovery questions, competitor comparison table, and a time-boxed talk track. Ready to paste into a call notes doc or CRM.
