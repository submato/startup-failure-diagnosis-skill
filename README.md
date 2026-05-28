# Startup Failure Diagnosis Skill

Diagnose startup ideas with failed-startup antipatterns inspired by Loot Drop's public failure research.

This is a Cursor/agent skill for founders, indie hackers, product builders, and investors who want a sharper answer than "validate the market." It turns a startup idea into a failure-chain diagnosis, risk scorecard, validation plan, and kill criteria.

## What It Does

- Maps a startup idea to likely failure antipatterns.
- Scores risk across demand, product, competition, distribution, unit economics, runway, operations, regulation, and team.
- Produces red flags and counter-evidence questions.
- Designs 7-14 day validation experiments.
- Sets explicit stop-or-pivot criteria.
- Suggests a safer rebuild angle when demand is recoverable.

## Why This Exists

Most startup advice is too generic. Loot Drop's public pages summarize 1,600+ failed startups and highlight recurring failure modes such as no market need, running out of cash, competition, product/tech failure, legal/regulatory issues, team conflict, and unit economics.

This skill distills those patterns into a practical diagnostic workflow. It does not treat any individual failure case as verified ground truth. Use it as a risk lens, then validate with current customer evidence, pricing tests, usage data, and unit economics.

Sources:

- [Loot Drop FAQ](https://www.loot-drop.io/faq)
- [Loot Drop Learning Framework](https://www.loot-drop.io/why-they-fail)
- [Loot Drop Insights](https://www.loot-drop.io/insights)
- [Loot Drop AI Deep Dive](https://www.loot-drop.io/deep-dive/ai)

## Install

Copy the skill folder into your project:

```bash
.agents/skills/startup-failure-diagnosis/
```

Or install it as a personal skill:

```bash
~/.cursor/skills/startup-failure-diagnosis/
```

The required file is:

```text
startup-failure-diagnosis/SKILL.md
```

The supporting files are:

```text
startup-failure-diagnosis/antipatterns.md
startup-failure-diagnosis/examples.md
```

## Quick Prompt

```text
Use the startup-failure-diagnosis skill to evaluate this idea:

[Describe the startup idea]

Return:
1. One-line verdict
2. Most likely failure chain
3. Risk scorecard from 0-5
4. Red flags
5. Counter-evidence needed
6. 7-14 day validation plan
7. Kill criteria
8. Rebuild angle
```

## Example

Input:

```text
Open-source this skill and build a paid online version.
First run is free, then users pay per diagnosis.
```

Expected style of output:

```text
One-line verdict:
High risk unless the open-source skill is treated as distribution and the paid product sells a decision-ready diagnosis report.

Most likely failure chain:
No Market Need -> Distribution Vacuum -> Competition / Commodity Trap -> Unit Economics

Core red flag:
If users can copy the open-source skill and run it locally, the paid online version needs a stronger value boundary than "call the AI once."
```

See the full demo in [demos/conversation-5a314bdf.md](demos/conversation-5a314bdf.md).

## Output Format

The skill returns:

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

## Counter-Evidence Needed
- [Evidence that would reduce risk]

## 7-14 Day Validation Plan
1. [Experiment]

## Kill Criteria
- Stop or pivot if [metric threshold] by [date/sample size].

## Rebuild Angle
[How to narrow, reposition, change channel, reduce cost, or create defensibility.]
```

## License

Apache-2.0.

## Disclaimer

This skill provides business analysis, not financial, legal, or investment advice. Validate assumptions with real customers, current market data, legal counsel where needed, and your own judgment.
