---
type: service
id: claude-service
title: Claude Service
description: "How this skrpt uses Anthropic Claude for launch messaging development, campaign planning, and performance analysis"
tags: [Production, Tested]
connections: []
metadata:
  provider: "anthropic"
  model: "claude-sonnet"
  estimated_duration: "N/A"
---

## Claude Service — Product Launch Marketing Flow

This skrpt uses Anthropic Claude as its primary AI service for all launch planning, messaging development, campaign asset creation, and post-launch analysis tasks.

### Usage Pattern

Claude is invoked across all three launch phases:

1. **Positioning & Messaging Development** — Claude develops positioning statements, messaging hierarchies, and audience-specific value propositions. This requires strategic thinking, understanding of competitive positioning frameworks, and the ability to craft compelling, differentiated messaging.

2. **Channel Strategy** — Claude evaluates marketing channels against audience behaviour, budget constraints, and launch goals to produce prioritised channel recommendations. This requires understanding of channel characteristics, audience behaviour patterns, and ROI-based reasoning.

3. **Launch Plan Generation** — Claude produces comprehensive launch plans with timelines, activities, budgets, and responsibility assignments. This requires structured planning, timeline management, and the ability to translate strategy into specific executable activities.

4. **Press Release Writing** — Claude drafts publication-ready press releases following standard PR format. This requires understanding of journalistic style, news value assessment, and the ability to write factually without marketing hyperbole.

5. **Email Sequence Design** — Claude designs multi-touch email sequences with complete copy for each email. This requires email marketing expertise, understanding of buyer psychology across the awareness-to-decision journey, and copywriting within email best practices.

6. **Post-Launch Analysis** — Claude analyses launch performance data against goals and produces retrospective reports with recommendations. This requires analytical reasoning, honest assessment, and the ability to translate data into strategic recommendations.

### Configuration

- **Temperature:** 0.4 for analytical tasks (channel strategy, launch measurement, post-launch analysis), 0.6 for creative tasks (messaging, press release, email copy)
- **Max tokens:** 3000 per invocation, 4000 for launch plans and email sequences
- **Context window:** Launch planning is highly contextual. Each stage builds on previous outputs. The positioning statement feeds into every subsequent stage.

### Data Handling

This skrpt processes product information, market data, and customer segment details. Claude:
- Uses product information solely for generating launch marketing materials
- Does not retain product details between sessions
- Treats competitive intelligence and pricing information as confidential
- Produces output suitable for internal review before external publication

### Requirements

- An active Anthropic API key or Claude CLI access
- Sufficient token quota for the full pipeline (approximately 20,000-25,000 tokens for a Tier 1 launch)
- All product details, competitive context, and performance data must be provided as input
