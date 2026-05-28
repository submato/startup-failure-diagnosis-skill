---
name: startup-failure-diagnosis
description: Diagnoses startup ideas, MVPs, pitch decks, rebuild plans, and business models using antipatterns distilled from 1100+ failed startup case studies and public startup post-mortem research. Use when evaluating startup ideas, PMF risk, startup failure risk, CAC/LTV, unit economics, platform dependency, competition, regulatory risk, 创业想法验证, or 创业失败诊断.
version: "0.1.0"
license: Apache-2.0
allowed-tools: WebFetch, WebSearch
when_to_use: "Use when the user asks whether a startup idea is viable, why startups fail, how to avoid startup failure, how to rebuild a failed startup idea, or how to diagnose business model risk."
argument-hint: "<startup idea, landing page, pitch deck, business plan, product brief, or failed startup case>"
metadata:
  tags:
    - startup
    - failure-analysis
    - business-model
    - pmf
    - unit-economics
    - startup-diagnosis
    - startup-failure
    - startup-autopsy
    - startup-idea-validation
    - 创业失败诊断
    - 创业想法验证
    - 商业模式诊断
    - PMF风险
---

# Startup Failure Diagnosis

This skill turns patterns distilled from 1100+ failed startup case studies into a practical diagnostic workflow. It is inspired by public startup post-mortem research, but it does not treat any single case as absolute truth. Use the patterns as risk lenses, then demand current evidence from customers, pricing tests, usage data, and unit economics.

## What This Skill Does

1. Maps a startup idea or plan to likely failure antipatterns.
2. Scores risk across demand, product, competition, go-to-market, unit economics, cash, team, operations, timing, and regulation.
3. Produces red flags, counter-evidence questions, validation experiments, and kill criteria.
4. Suggests a safer rebuild angle when the original idea has recoverable demand.

## Source Model

The skill uses 7 core failure antipatterns commonly found in startup post-mortems:

- No Market Need
- Ran Out of Cash
- Team/Founder Conflict
- Competition
- Product/Tech Failure
- Legal/Regulatory Issues
- Unit Economics

Startup failures rarely come from one reason. Product problems, competition, pricing/unit economics, focus drift, marketing/distribution, cash management, operational scalability, regulation, PMF, and team conflict compound into a failure chain.

For the detailed diagnostic library, read [antipatterns.md](antipatterns.md). For examples, read [examples.md](examples.md).

## Quick Start

Use this skill for prompts like:

```text
Analyze this startup idea for failure risks: [idea]
Review this pitch deck like a failed-startup autopsy.
Will this product die from CAC/LTV, retention, or platform dependency?
Use failed startup patterns to rebuild this idea: [failed startup or concept]
请使用 startup-failure-diagnosis skill 分析这个创业想法：[idea]
这个项目最可能怎么失败？请给出失败链条、风险评分、验证实验和 kill criteria。
```

## Required Inputs

If the user gives only a vague idea, ask for the missing pieces most likely to change the diagnosis:

- Target customer and urgent use case
- Current alternative or competitor
- Pricing and expected willingness to pay
- Acquisition channel
- Retention or repeat-use mechanism
- Delivery cost, gross margin, or inference/operations cost
- Regulatory or platform dependency

Do not block on perfect information. If data is missing, mark assumptions and diagnose what could be inferred.

## Diagnosis Workflow

1. **Restate the business clearly**: customer, problem, product, channel, revenue model, and market context.
2. **Identify the failure chain**: choose the 2-4 antipatterns most likely to trigger each other. Example: weak PMF leads to paid acquisition dependence, which breaks CAC/LTV, which drains cash.
3. **Score risk**: assign 0-5 for each dimension below. 0 means low known risk, 5 means severe unresolved risk.
4. **Ask for counter-evidence**: name the evidence that would disprove the risk judgment.
5. **Design fast validation**: prefer 7-14 day experiments that test payment, retention, distribution, or cost.
6. **Set kill criteria**: define measurable stop/pivot thresholds before more building.
7. **Propose rebuild angle**: if the market gap is real, narrow the segment, change distribution, improve economics, or reduce dependency.

## Risk Dimensions

Score these dimensions from 0 to 5:

- Demand risk: users acknowledge the problem but may not pay or switch.
- Product risk: quality, UX, technical feasibility, or reliability may not clear the bar.
- Competition risk: incumbents, platforms, or fast followers can bundle or copy.
- Distribution risk: there is no repeatable, affordable acquisition channel.
- Unit economics risk: LTV, margin, payback, or cost-to-serve does not work.
- Cash/runway risk: the project needs too much time, CAPEX, or R&D before revenue.
- Focus risk: the plan depends on too many segments, features, or pivots.
- Operations risk: fulfillment, support, marketplace liquidity, or human labor will not scale.
- Regulatory risk: compliance, data rights, safety, or licensing can block deployment.
- Team risk: missing founder skills, incentive conflict, or execution mismatch.

## Output Format

Respond in this structure unless the user asks for a different format:

```markdown
## One-Line Verdict
[Plain-language judgment with confidence level.]

## Most Likely Failure Chain
[Antipattern A] -> [Antipattern B] -> [Antipattern C]

## Risk Scorecard
- Demand: [0-5] - [reason]
- Product/Tech: [0-5] - [reason]
- Competition: [0-5] - [reason]
- Distribution: [0-5] - [reason]
- Unit Economics: [0-5] - [reason]
- Cash/Runway: [0-5] - [reason]
- Operations/Regulation/Team: [0-5] - [reason]

## Red Flags
- [Specific red flag]
- [Specific red flag]
- [Specific red flag]

## Counter-Evidence Needed
- [Evidence that would reduce risk]
- [Evidence that would reduce risk]

## 7-14 Day Validation Plan
1. [Experiment]
2. [Experiment]
3. [Experiment]

## Kill Criteria
- Stop or pivot if [metric threshold] by [date/sample size].
- Stop or pivot if [metric threshold] by [date/sample size].

## Rebuild Angle
[How to narrow, reposition, change channel, reduce cost, or create defensibility.]
```

## Scoring Rules

- High confidence requires direct evidence: paid pilots, retention cohorts, gross margin math, sales-cycle data, signed LOIs, or real usage logs.
- Interviews alone reduce uncertainty but do not prove demand. Prefer proof of payment, switching, or repeated use.
- If a startup relies on AI, score unit economics and competition harshly unless model cost, workflow integration, proprietary data, and distribution are clear.
- If a startup is in health, finance, education, transportation, labor, housing, or child-related markets, always check regulatory and trust requirements.
- If the plan depends on marketplaces, logistics, support, curation, or local operations, check whether human labor scales linearly with revenue.

## Rebuild Logic

When turning a failed idea into a new opportunity, do not simply "do it with AI." Require one of these structural changes:

- Cost curve changed: serverless, foundation models, automation, or open-source tooling makes the old unit economics viable.
- Distribution changed: a new channel, community, platform, or workflow creates cheaper acquisition.
- Buyer changed: a narrower segment now has budget, urgency, or regulatory pressure.
- Scope changed: a smaller wedge avoids the original operational or technical trap.
- Defensibility changed: proprietary data, workflow lock-in, compliance depth, or trusted distribution creates a moat.

## Quality Bar

- Be concrete, skeptical, and useful.
- Name the riskiest assumption, not just a list of generic startup advice.
- Separate "market wants this problem solved" from "this company can solve it profitably."
- Use confidence labels: High, Medium, Low.
- Never present public post-mortem summaries as verified ground truth. Treat them as pattern evidence and ask for current validation.
