---
type: workflow
id: product-launch-marketing-flow
title: Product Launch Marketing Flow
description: "Go-to-market marketing plans for product launches — messaging, channels, timeline, and measurement"
tags: [Production, Tested, Campaign, Strategy]
connections:
  - target: launch-messaging-development
    type: uses
  - target: channel-strategy
    type: uses
  - target: launch-measurement
    type: uses
  - target: llm-service
    type: runs_on
  - target: product-launch-framework
    type: references
  - target: launch-planning-playbook
    type: references
  - target: brand-voice-guide
    type: references
  - target: audience-segmentation
    type: uses
  - target: image-briefing
    type: uses
metadata:
  estimated_duration: "35-50 minutes"
  trigger: manual
output_step: "image-briefing"
composite_steps:
  - "launch-messaging-development"
  - "channel-strategy"
  - "launch-measurement"
  - "audience-segmentation"
  - "image-briefing"
execution:
  - skill: "launch-messaging-development"
    step_type: "generation"
  - skill: "channel-strategy"
    step_type: "synthesis"
  - skill: "launch-measurement"
    step_type: "synthesis"
  - skill: "audience-segmentation"
    step_type: "synthesis"
  - skill: "image-briefing"
    step_type: "generation"
    context:
      brand_guidelines: ""
---

## Overview

This workflow produces a complete marketing plan for a product launch, from initial positioning and messaging through channel strategy, campaign execution assets, and post-launch performance analysis. It is designed to run in phases that mirror the actual launch timeline: pre-launch preparation, launch execution, and post-launch optimisation.

## Pipeline Stages

### Phase 1: Positioning & Messaging (4-6 weeks before launch)

#### Stage 1.1: Positioning Development

**Input:** Product details (features, benefits, target audience), competitive landscape, customer research, market context

Invoke the **launch-messaging-development** skill to establish the strategic messaging foundation. Then run the **positioning-statement-writer** prompt to produce a formal positioning statement and messaging hierarchy.

**Output:** Positioning statement, messaging pillars, key claims with proof points, audience-specific value propositions.

**Gate:** Positioning must be reviewed and approved by product and executive stakeholders before proceeding. Messaging built on weak positioning wastes effort downstream.

#### Stage 1.2: Launch Plan Generation

**Input:** Positioning outputs from Stage 1.1, budget, team resources, launch date, launch tier (major/minor/incremental)

Invoke the **channel-strategy** skill to evaluate and recommend channel allocation. Then run the **launch-plan-generator** prompt to produce a detailed launch marketing plan with timeline, channel strategy, and resource allocation.

**Output:** Complete launch plan using the **launch-plan-template** format, with timeline documented in the **launch-timeline-template**.

### Phase 2: Campaign Asset Development (2-4 weeks before launch)

#### Stage 2.1: Press Release

**Input:** Positioning statement, product details, company boilerplate, key quotes, availability information

Invoke the **press-release-writer** prompt to produce a launch press release suitable for distribution to media and publication on the company newsroom.

**Output:** Publication-ready press release with headline, subheadline, body, quotes, boilerplate, and media contact information.

#### Stage 2.2: Email Sequence

**Input:** Positioning statement, audience segments, product details, launch timeline, CTAs for each launch phase

Invoke the **launch-email-sequence-builder** prompt to design a multi-touch email sequence covering pre-launch teaser, launch announcement, feature deep-dives, and follow-up nurture.

**Output:** Complete email sequence with subject lines, preview text, body copy, and CTAs for each email.

**Note:** Stages 2.1 and 2.2 can run in parallel.

### Phase 3: Post-Launch Analysis (1-4 weeks after launch)

#### Stage 3.1: Performance Analysis

**Input:** Launch metrics (traffic, sign-ups, downloads, revenue, media coverage, social engagement), goals from the launch plan, channel-specific performance data

Invoke the **launch-measurement** skill to evaluate launch performance against goals. Then run the **post-launch-analysis-prompt** to produce a thorough launch retrospective with recommendations.

**Output:** Launch performance report with metric analysis, channel effectiveness assessment, and recommendations for future launches.

## Error Handling

- If positioning research reveals the product does not have a clear differentiator, escalate to product leadership before investing in launch marketing. Marketing cannot fix a weak product.
- If the launch date moves, regenerate the timeline and adjust email sequences. All dates in the plan should reference relative milestones ("L-14 days") rather than fixed dates where possible.
- If budget is cut mid-planning, rerun the channel-strategy skill with updated constraints to reprioritise channels rather than uniformly reducing all channels.
- If post-launch metrics significantly underperform goals, investigate whether the issue is messaging, channel, audience targeting, or product-market fit before adjusting tactics.
- If a competitive launch occurs close to yours, run the threat-assessment to evaluate impact and consider timing or messaging adjustments.

## Launch Tier Guidelines

| Tier | Description | Pipeline Scope | Typical Duration |
|------|-------------|----------------|-----------------|
| **Tier 1 — Major** | New product, new market entry, rebrand | Full pipeline, all stages | 6-8 weeks |
| **Tier 2 — Significant** | Major feature, new pricing, partnership | Full pipeline, abbreviated Phase 2 | 4-6 weeks |
| **Tier 3 — Incremental** | Feature update, minor enhancement | Stages 1.1, 2.2, and 3.1 only | 2-3 weeks |

## Inputs

| Name | Required | Description | Example |
|------|----------|-------------|---------|
| `{{input.product_name}}` | Yes | Product name | `Acme Analytics Pro` |
| `{{input.product_details}}` | Yes | Product details (features, benefits, description) | `Paste the relevant brief, notes, source material, or dataset here.` |
| `{{input.target_audience}}` | Yes | Target audience segments | `Marketing managers at mid-size B2B SaaS companies` |
| `{{input.competitive_landscape}}` | Yes | Competitive landscape | `Paste the relevant brief, notes, source material, or dataset here.` |
| `{{input.customer_research}}` | Yes | Customer research | `Paste the relevant brief, notes, source material, or dataset here.` |
| `{{input.launch_date}}` | Yes | Launch date | `15 April 2026` |
| `{{input.market_context}}` | No | Market context | `Paste a short brief describing the goal, audience, and constraints.` |

## Outputs

| Name | Description |
|------|-------------|
| Positioning statement, messaging pillars, key claims | Positioning statement, messaging pillars, key claims with proof points, audience-specific value propositions |
| Complete launch plan using the launch-plan-template format, | Complete launch plan using the launch-plan-template format, with timeline documented in the launch-timeline-template |
| Publication-ready press release | Publication-ready press release with headline, subheadline, body, quotes, boilerplate, and media contact information |
| Complete email sequence | Complete email sequence with subject lines, preview text, body copy, and CTAs for each email |
| Launch performance report | Launch performance report with metric analysis, channel effectiveness assessment, and recommendations for future launches |

## Setup

Before running this workflow:

1. No external services required — paste your content directly and provide any supporting context as inputs or source nodes.
2. Review the included documents, assets, or source nodes and customise them to match your team, brand, or domain conventions where needed.
3. No specific AI provider or API key is required beyond your configured skrptiq LLM provider.

## Provider Notes

- Most stages work with any capable model; stronger models usually improve synthesis, judgement, and writing quality.
- Extraction, classification, and formatting steps generally run well on smaller or faster models.
- Because there are no vendor-specific integrations here, provider choice is mostly a trade-off between speed, quality, and cost.

## Example Input

To test this workflow immediately after import:

```
Product Name: "Acme Analytics Pro"
Product Details: "Paste the relevant brief, notes, source material, or dataset here."
Target Audience: "Marketing managers at mid-size B2B SaaS companies"
Competitive Landscape: "Paste the relevant brief, notes, source material, or dataset here."
Customer Research: "Paste the relevant brief, notes, source material, or dataset here."
Launch Date: "15 April 2026"
Market Context: "Paste a short brief describing the goal, audience, and constraints."
```

