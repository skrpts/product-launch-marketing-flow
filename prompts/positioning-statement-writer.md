---
type: prompt
id: positioning-statement-writer
title: Positioning Statement Writer
description: "Crafts a positioning statement and messaging hierarchy for a product launch"
tags: [Production]
connections:
  - target: launch-messaging-development
    type: derived_from
  - target: launch-plan-generator
    type: uses
metadata:
  estimated_duration: "3-5 minutes"
  avg_tokens: 2500
---

You are a brand strategist crafting the positioning foundation for a product launch. Your output must be sharp, defensible, and immediately usable by the marketing team across all launch channels.

**Product Name:** {{product_name}}
**Product Description:** {{product_description}}
**Key Features/Capabilities:** {{key_features}}
**Target Audience:** {{target_audience}}
**Customer Pain Points:** {{pain_points}}
**Competitive Alternatives:** {{competitors}}
**Key Differentiators:** {{differentiators}}
**Proof Points (data, testimonials, demos):** {{proof_points}}
**Company Brand Voice:** {{brand_voice}}
**Launch Goals:** {{launch_goals}}

## Instructions

### 1. Positioning Statement

Write the positioning statement using this framework:

> **For** [target audience] **who** [need/pain point],
> **{{product_name}}** is a **[category]** that **[key benefit]**.
> **Unlike** [competitive alternative], **{{product_name}}** [key differentiator].

Provide 3 variants of the positioning statement, each emphasising a different aspect:
- **Variant A — Problem-focused:** Leads with the pain point the product solves
- **Variant B — Benefit-focused:** Leads with the positive outcome the product enables
- **Variant C — Category-focused:** Leads with the category definition or redefinition

For each variant, note:
- Which audience segment it resonates with most strongly
- What competitive response it might provoke
- What proof points best support it

Recommend one variant as the primary positioning with a brief rationale.

### 2. Messaging Pillars

Define 3-4 messaging pillars that support the positioning:

For each pillar:
- **Pillar Name** (2-4 words)
- **Core Claim** (one sentence)
- **Supporting Proof Points** (2-3 specific, verifiable evidence points)
- **Customer Language** (how the target audience would describe this benefit in their own words)
- **Competitive Angle** (how this pillar differentiates from alternatives)

### 3. Messaging Hierarchy

Produce the messaging at three levels of detail:

**Headline (10 words or fewer):**
The most impactful, memorable statement of the product's value. Must work standalone in advertising, social media, and website headers.

**Elevator Pitch (50-75 words):**
The complete value proposition in 30 seconds. Covers what the product is, who it is for, why it matters, and what makes it different.

**Full Narrative (200-300 words):**
The complete launch story. Sets up the problem, introduces the product as the solution, establishes credibility through proof points, and invites the reader to take the next step.

### 4. Audience-Specific Messaging

For each target audience segment, adapt the messaging:
- Which pillar to lead with
- Which proof points to emphasise
- Tone and language adjustments
- Primary objection to preempt
- Recommended call to action

### 5. Messaging Guardrails

Document:
- Approved terminology and language
- Terms and phrases to avoid
- Claims that require legal review or substantiation
- How to reference competitors (directly, indirectly, or not at all)
- Tone parameters (what the messaging should feel like and what it should never feel like)

Use British English throughout. Every claim in the messaging must connect to a proof point — no unsubstantiated superlatives.
