# Startup Failure Antipattern Library

Use this file as the diagnostic library behind `startup-failure-diagnosis`.

## 1. No Market Need

**Pattern**: Users understand the idea but do not feel enough pain to pay, switch, or change behavior.

**Signals**
- Praise without payment.
- Many free users, weak conversion.
- Problem is real but low priority.
- Buyer and user are different, and the buyer has no budget urgency.

**Diagnostic questions**
- What painful event makes the user search for this now?
- What are users already paying in money, time, headcount, or risk?
- What existing workflow must be displaced?
- Would users prepay, sign an LOI, or commit usage before the product exists?

**Validation**
- Pre-sell to 10-20 target customers.
- Run concierge delivery before building software.
- Test switching behavior, not stated interest.

## 2. Ran Out of Cash

**Pattern**: The company needs more time, talent, R&D, inventory, compliance, or sales cycles than its runway allows.

**Signals**
- Long build before first revenue.
- Enterprise sales cycle exceeds runway.
- Hardware, AI, biotech, autonomy, or regulated markets with high burn.
- Hiring plan assumes the next round will arrive.

**Diagnostic questions**
- How many months until real revenue, not demos?
- What must be true before the next fundraising window?
- Which costs scale before revenue scales?
- What can be cut without killing learning velocity?

**Validation**
- Build a cash milestone map.
- Model best/base/worst runway.
- Define a trigger for cutting scope early.

## 3. Team or Founder Conflict

**Pattern**: The team lacks the needed mix of technical, sales, domain, finance, or operating ability, or founders disagree on risk, pace, equity, or direction.

**Signals**
- Technical founder has no buyer access.
- Business founder cannot sell before product is ready.
- No one owns finance, compliance, or operations.
- Strategic disagreements appear before customer evidence exists.

**Diagnostic questions**
- Who can sell this to the first 10 customers?
- Who owns the riskiest function?
- What decision rights exist when metrics are weak?
- What founder skill gap must be filled before scale?

**Validation**
- Assign one owner per critical risk.
- Run a pre-mortem on founder conflict.
- Define pivot and shutdown decision rules.

## 4. Competition

**Pattern**: Incumbents, platforms, or better-funded competitors can copy, bundle, subsidize, or distribute the product faster than the startup can defend.

**Signals**
- Core advantage is a feature, not a workflow or network.
- Competing with a tech giant's roadmap.
- Customer can get "good enough" inside an existing tool.
- No proprietary data, distribution, compliance depth, or switching cost.

**Diagnostic questions**
- Why will customers choose this over the default incumbent?
- What can the startup know, access, or distribute that others cannot?
- Could a platform bundle the same feature for free?
- Is the wedge narrow enough to beat broad incumbents?

**Validation**
- Interview customers who recently bought a competitor.
- Test a differentiated wedge with a niche segment.
- Identify non-copyable assets before scaling.

## 5. Product or Tech Failure

**Pattern**: The product cannot meet the minimum quality, reliability, UX, safety, or integration standard required for the market.

**Signals**
- Demo works, production reliability does not.
- Workflow integration is harder than model or feature development.
- Users abandon after novelty.
- Edge cases destroy trust.

**Diagnostic questions**
- What failure rate can customers tolerate?
- Which edge cases create legal, safety, trust, or revenue risk?
- What integrations are required before value is realized?
- Does the product reduce work or create review burden?

**Validation**
- Run pilots in real workflows, not sandbox demos.
- Track time saved, error rate, abandonment, and support load.
- Test the worst 20% of cases, not the easiest 80%.

## 6. Legal or Regulatory Issues

**Pattern**: Compliance, licensing, privacy, data rights, safety, labor rules, financial rules, or healthcare rules block deployment or make the product too expensive to operate.

**Signals**
- "We will handle compliance later."
- Product uses sensitive data without clear consent or retention policy.
- Market requires licenses, audits, liability coverage, or procurement review.
- The MVP touches safety-critical decisions.

**Diagnostic questions**
- What law, platform policy, or certification can stop deployment?
- Who bears liability when the product is wrong?
- What data can be used, stored, transferred, or automated?
- Does the first version need enterprise-grade compliance?

**Validation**
- Run a compliance pre-check before building.
- Talk to buyers' legal/procurement teams.
- Design the MVP to avoid regulated actions where possible.

## 7. Unit Economics

**Pattern**: The product can attract users but cannot serve them profitably. Growth makes losses larger.

**Signals**
- CAC payback is unknown or longer than runway.
- Gross margin drops as usage increases.
- AI inference, human labor, logistics, returns, support, or onboarding costs are hidden.
- Pricing is based on competitors, not cost-to-serve and willingness to pay.

**Diagnostic questions**
- What is fully loaded gross margin after delivery, support, compute, and payment fees?
- What is LTV, CAC, and payback period by channel?
- Which cost grows with each customer or transaction?
- What price would make the business healthy, and will customers pay it?

**Validation**
- Calculate unit economics per customer or transaction.
- Charge early instead of using free pilots as false demand.
- Track margin at small scale before increasing acquisition.

## 8. Focus Drift and Pivot Fog

**Pattern**: The startup chases too many segments, features, or pivots before proving one narrow wedge.

**Signals**
- Roadmap has multiple ICPs.
- Pivot decisions are driven by fear or investor pressure, not evidence.
- Every sales objection becomes a feature.
- The product message changes weekly.

**Diagnostic questions**
- What is the single segment where pain, budget, and access overlap?
- Which feature is required for the first paid outcome?
- What evidence justifies the current pivot?
- What will the team explicitly not build?

**Validation**
- Write a one-segment wedge statement.
- Kill features that do not serve the first paid workflow.
- Use a decision log for pivots.

## 9. Distribution Vacuum

**Pattern**: The product is built before a repeatable go-to-market path exists.

**Signals**
- "If we build it, users will come."
- Growth depends on viral loops that have not been proven.
- Paid ads are the only channel and CAC is unknown.
- Founders cannot reach buyers directly.

**Diagnostic questions**
- Where do target buyers already gather?
- What channel can produce 10, 100, and 1,000 customers?
- What is the cost and conversion rate by channel?
- What proof makes distribution easier over time?

**Validation**
- Run channel tests before product completion.
- Sell manually to the first 10 customers.
- Measure conversion from problem awareness to paid usage.

## 10. Operational Scalability Trap

**Pattern**: The business looks like software but actually scales with people, inventory, logistics, support, curation, or local execution.

**Signals**
- Human curation or support is required for quality.
- Marketplace liquidity requires manual intervention.
- Returns, fraud, inventory, or fulfillment eat margin.
- Each new market requires a local operating team.

**Diagnostic questions**
- Which parts require humans per transaction?
- Does service quality fall when volume doubles?
- Can automation replace operations without harming trust?
- What breaks first at 10x usage?

**Validation**
- Map every manual step and its cost.
- Run a high-volume simulation.
- Automate only after identifying the true bottleneck.

## 11. Timing Mismatch

**Pattern**: The problem is real, but infrastructure, regulation, buyer behavior, compute cost, or market education is not ready.

**Signals**
- Customers agree with the vision but defer purchase.
- Adoption depends on ecosystem changes outside the startup's control.
- Sales cycles are education-heavy.
- The product gets revived successfully years later by others.

**Diagnostic questions**
- What external change makes now different?
- What must happen before customers can adopt?
- Is there a smaller wedge that works today?
- Are costs, regulations, or user habits moving in the right direction?

**Validation**
- Identify a now-specific trigger.
- Sell to early adopters with urgent current pain.
- Avoid broad market education as the main strategy.

## 12. AI-Specific Commodity Trap

**Pattern**: The startup wraps AI capabilities that are quickly commoditized by foundation models, cloud platforms, or incumbents.

**Signals**
- Defensibility is "our model is better."
- No proprietary data or workflow lock-in.
- Inference costs rise with usage.
- Enterprise users like the demo but avoid deployment.

**Diagnostic questions**
- What remains valuable if GPT, Claude, Gemini, or a cloud provider improves next month?
- Does the product own data, workflow, compliance, or distribution?
- Are inference costs below 30% of revenue at realistic usage?
- Does the product fit existing workflows without change management pain?

**Validation**
- Model gross margin after inference.
- Test retention after novelty fades.
- Build around a vertical workflow, not general AI capability.
