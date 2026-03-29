---
type: skill
id: channel-strategy
title: Channel Strategy
description: "Evaluates and recommends marketing channel allocation for a product launch based on audience, budget, and goals"
tags: [Production, Tested, design:product, design:launch]
connections:
  - target: llm-service
    type: runs_on
  - target: product-launch-framework
    type: references
metadata:
  estimated_duration: "4-6 minutes"
  avg_tokens: 2500
---

## Capability

Evaluates available marketing channels against launch goals, target audience behaviour, budget constraints, and team capabilities to produce a prioritised channel strategy. Ensures launch resources are allocated to the channels most likely to deliver results rather than spread thinly across every available option.

## When to Use

- Planning channel allocation for an upcoming product launch
- Reassessing channel strategy when budget changes mid-launch
- Evaluating whether to add a new channel to the launch mix
- Post-launch, determining which channels delivered the best ROI for future planning
- Comparing channel effectiveness across different audience segments

## Process

1. **Audience-Channel Mapping** — For each target audience segment, identify:
   - Where they consume information (social platforms, publications, communities, events)
   - How they discover new products (search, word of mouth, advertising, analyst reports, peer recommendations)
   - What content formats they prefer in each channel
   - At what stage of the buyer journey each channel is most influential

2. **Channel Evaluation** — Assess each potential channel against:
   - **Reach:** How many target audience members can this channel reach?
   - **Relevance:** Is this channel contextually appropriate for the product and message?
   - **Cost:** What is the cost per impression, engagement, and conversion?
   - **Control:** How much control do you have over timing, messaging, and targeting?
   - **Speed:** How quickly can this channel generate results?
   - **Capability:** Does the team have the skills and resources to execute well on this channel?

3. **Channel Tiering** — Categorise channels into:
   - **Primary channels (60-70% of budget/effort):** Highest confidence channels that directly reach the target audience. These carry the core launch message.
   - **Supporting channels (20-30% of budget/effort):** Channels that amplify the primary message, provide social proof, or reach secondary audiences.
   - **Experimental channels (5-10% of budget/effort):** New or unproven channels worth testing during the launch to gather data for future launches.

4. **Channel Sequencing** — Map channels to the launch timeline:
   - **Pre-launch (L-4 to L-1 weeks):** Teaser and anticipation-building channels (email, social, community)
   - **Launch day/week:** Maximum impact channels (PR, paid ads, email blast, social, influencer)
   - **Post-launch (L+1 to L+4 weeks):** Sustained awareness and nurture channels (content marketing, retargeting, email sequences, SEO)

5. **Budget Allocation** — Distribute budget across channels with specific spend recommendations:
   - Fixed costs (PR agency, event production, design assets)
   - Variable costs (paid advertising, sponsored content, influencer fees)
   - Contingency reserve (10% of total budget for opportunistic or reactive spending)

6. **Success Metrics by Channel** — Define what success looks like for each channel:
   - Primary KPI (awareness metric, engagement metric, or conversion metric)
   - Target numbers for the launch period
   - Tracking mechanism (UTM parameters, dedicated landing pages, promo codes)

## Inputs

- Target audience segments with channel preferences
- Launch budget (total and any channel-specific constraints)
- Team capabilities and resource availability
- Launch timeline and key dates
- Launch tier (major, significant, incremental)
- Historical channel performance data from previous launches (optional)

## Outputs

- Prioritised channel list with tier assignments
- Budget allocation by channel with rationale
- Channel sequencing timeline
- Success metrics and targets by channel
- Risk assessment (channels with highest uncertainty)
- Channel brief for each primary channel (what, when, how much)

## Constraints

- Never recommend channels the team cannot execute well — a poorly executed channel is worse than an absent one
- Budget allocation must total 100% including contingency — no open-ended recommendations
- Every recommended channel must have a measurable KPI — if you cannot measure it, do not recommend it
- Consider channel fatigue — the same audience receiving the message across 8 channels simultaneously is annoying, not effective
