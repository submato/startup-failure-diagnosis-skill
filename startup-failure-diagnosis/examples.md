# Startup Failure Diagnosis Examples

## Example 1: AI Content Tool

**Input**

```text
I want to build an AI tool that helps short-form content creators generate post drafts, titles, and cover ideas. It will be subscription-based.
```

**Output pattern**

```markdown
## One-Line Verdict
Medium-high risk. The idea has visible demand, but the main danger is becoming a commodity AI wrapper with weak retention and platform dependency.

## Most Likely Failure Chain
AI-Specific Commodity Trap -> Distribution Vacuum -> Unit Economics -> Ran Out of Cash

## Risk Scorecard
- Demand: 3 - Creators want content help, but willingness to pay depends on whether output improves traffic or revenue.
- Product/Tech: 3 - Generation quality is easy to demo but hard to make consistently publishable.
- Competition: 5 - Many AI writing tools and platform-native features can copy this.
- Distribution: 4 - Creator acquisition may be noisy and paid channels can be expensive.
- Unit Economics: 3 - Subscription can work, but model cost and churn must be controlled.
- Cash/Runway: 2 - MVP can be lean if built on existing models.
- Operations/Regulation/Team: 3 - Platform rules and content compliance matter.

## Red Flags
- Users only use it once for inspiration, then churn.
- Differentiation is prompt quality rather than workflow, data, or distribution.
- The product depends on an external platform algorithm it cannot control.

## Counter-Evidence Needed
- 20 creators pay before launch or commit to a paid pilot.
- Users publish AI-assisted content 3+ times in 14 days.
- Generated content improves measurable saves, comments, leads, or sales.

## 7-14 Day Validation Plan
1. Manually deliver 30 posts for 10 creators and charge a small fee.
2. Track whether creators publish, edit heavily, and return for more.
3. Test one narrow segment, such as local service businesses or solo e-commerce sellers.

## Kill Criteria
- Stop or pivot if fewer than 3 of 20 target users agree to pay.
- Stop or pivot if fewer than 30% publish a generated post within 7 days.

## Rebuild Angle
Avoid generic content generation. Build a vertical workflow: competitor monitoring, brand-safe drafts, image/script templates, posting calendar, and ROI tracking for one monetizing creator segment.
```

## Example 2: Marketplace for Local Services

**Input**

```text
We want to build a marketplace connecting homeowners with vetted local repair workers.
```

**Output pattern**

```markdown
## One-Line Verdict
High operational risk. This can work only if trust, supply quality, and repeatable local acquisition are solved one city at a time.

## Most Likely Failure Chain
Operational Scalability Trap -> Distribution Vacuum -> Unit Economics -> Ran Out of Cash

## Red Flags
- Every new city requires manual worker vetting and support.
- Quality failures create trust and refund costs.
- Paid acquisition may be needed on both sides of the marketplace.

## Counter-Evidence Needed
- One neighborhood reaches repeat transactions without heavy subsidies.
- Contribution margin stays positive after refunds, support, and acquisition.
- Supply quality can be maintained without founder-led manual work.

## 7-14 Day Validation Plan
1. Run a concierge version in one neighborhood with 20 jobs.
2. Track time spent per job, refund rate, repeat rate, and acquisition source.
3. Test whether homeowners will pay a service fee for reliability.

## Kill Criteria
- Stop or narrow if manual ops exceed 30 minutes per transaction after 20 jobs.
- Stop or pivot if repeat purchase or referral is below 20%.

## Rebuild Angle
Start as managed software for a niche contractor category before becoming a broad marketplace.
```
