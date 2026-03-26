---
type: prompt
id: launch-plan-generator
title: Launch Plan Generator
description: "Generates a detailed launch marketing plan with phases, channels, timeline, and resource allocation"
tags: [Production]
connections:
  - target: channel-strategy
    type: derived_from
  - target: launch-messaging-development
    type: derived_from
  - target: press-release-writer
    type: uses
  - target: launch-plan-template
    type: references
  - target: launch-timeline-template
    type: references
metadata:
  estimated_duration: "5-8 minutes"
  avg_tokens: 3500
---

You are a marketing launch strategist creating a complete go-to-market plan. The plan must be specific enough that the marketing team can execute it without further strategic guidance — every activity, channel, and milestone should be clearly defined.

**Product:** {{input.product_name}}
**Positioning Statement:** {{steps.positioning-statement-writer.output}}
**Messaging Pillars:** Extract the messaging pillars from {{steps.positioning-statement-writer.output}}.
**Launch Date:** {{input.launch_date}}
**Launch Tier:** Determine the appropriate launch tier (Tier 1 Major / Tier 2 Significant / Tier 3 Incremental) based on the product details and market context.
**Target Audience Segments:** {{input.target_audience}}
**Total Marketing Budget:** Recommend an appropriate budget allocation based on the launch tier and market context.
**Team Resources:** Recommend team resource requirements based on the launch plan scope.
**Channel Strategy Recommendations:** {{steps.channel-strategy.output}}
**Key Constraints:** Identify any key constraints from the market context provided (e.g., regulatory approvals, partner dependencies, seasonal considerations).

## Instructions

Generate a launch plan following the launch-plan-template structure:

### 1. Launch Overview
- One-paragraph summary of the launch: what, why, who, when
- Success definition: the 3-5 metrics that define whether this launch succeeded
- Launch tier justification: why this tier, and what it means for scope

### 2. Pre-Launch Phase (L-6 to L-1 weeks)

**Internal Readiness (L-6 to L-4 weeks):**
- Sales enablement: battle cards, demo scripts, FAQ document, pricing guidance
- Customer success preparation: training materials, support documentation, known issues
- Internal communications: all-hands announcement, Slack channels, launch countdown
- Legal and compliance: messaging approval, claim substantiation, terms updates

**Teaser & Anticipation (L-3 to L-1 weeks):**
- Social media teaser campaign: [specific activities by platform and day]
- Email teaser to existing customers: [subject line, timing, CTA]
- Community and partner briefings: [who, when, what to share]
- Influencer/analyst pre-briefings: [targets, materials to share, embargo dates]
- Landing page: [pre-launch landing page with waitlist or notification sign-up]

### 3. Launch Week (L-Day to L+7 days)

**Launch Day:**
- Hour-by-hour schedule of activities
- Press release distribution: [channels, timing, target outlets]
- Email announcement: [segment-specific sends with timing]
- Social media: [platform-specific posts with timing]
- Website updates: [pages to update, new pages to publish]
- Paid advertising activation: [channels, budgets, targeting]
- Internal celebration: [how to energise the team]

**Launch Week:**
- Day-by-day activity calendar
- Content publishing schedule (blog posts, case studies, tutorials)
- Social media cadence and themes for each day
- Paid advertising monitoring and optimisation schedule
- Media follow-up and interview scheduling
- Community engagement activities

### 4. Post-Launch Phase (L+2 to L+8 weeks)

**Sustained Momentum (L+2 to L+4 weeks):**
- Content marketing: [blog posts, videos, webinars planned]
- Email nurture sequence: [for leads who did not convert at launch]
- Retargeting campaigns: [audiences, messaging, budget]
- Customer success stories: [early adopter case studies to develop]
- Social proof building: [review campaigns, testimonial collection]

**Optimisation (L+4 to L+8 weeks):**
- Performance review checkpoints: [when and what to assess]
- Message testing: [A/B tests to run based on initial data]
- Channel reallocation: [criteria for shifting budget between channels]
- Feedback integration: [how customer and market feedback loops back to marketing]

### 5. Budget Allocation

| Category | Budget | % of Total | Key Line Items |
|----------|--------|-----------|---------------|
| Paid advertising | [amount] | [%] | [channels] |
| Content production | [amount] | [%] | [assets] |
| PR and comms | [amount] | [%] | [activities] |
| Events/sponsorships | [amount] | [%] | [events] |
| Tools and platforms | [amount] | [%] | [tools] |
| Contingency | [amount] | 10% | Unplanned opportunities |
| **Total** | [amount] | 100% | |

### 6. Risk Register

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| [risk] | High/Med/Low | High/Med/Low | [mitigation plan] |

### 7. RACI Matrix

| Activity | Responsible | Accountable | Consulted | Informed |
|----------|------------|-------------|-----------|----------|
| [activity] | [role] | [role] | [roles] | [roles] |

Use British English throughout. Fill all fields with specific recommendations based on the inputs — no placeholder text or "TBD" entries.
