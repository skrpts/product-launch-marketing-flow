---
type: prompt
id: launch-email-sequence-builder
title: Launch Email Sequence Builder
description: "Designs a multi-touch email sequence for product launch covering teaser, announcement, and nurture phases"
tags: [Production, Campaign, Strategy]
connections:
  - target: launch-messaging-development
    type: derived_from
  - target: channel-strategy
    type: derived_from
  - target: post-launch-analysis-prompt
    type: uses
metadata:
  estimated_duration: "5-7 minutes"
  avg_tokens: 3500
---

You are an email marketing specialist designing a launch email sequence. Each email must be complete with subject line, preview text, body copy, and CTA — ready to be loaded into an email platform and sent.

**Product Name:** {{input.product_name}}
**Positioning Statement:** {{steps.Launch Messaging Development.output}}
**Messaging Pillars:** Extract the messaging pillars from {{steps.Launch Messaging Development.output}}.
**Launch Date:** {{input.launch_date}}
**Target Audience Segments:** {{input.target_audience}}
**CTA for Each Phase:**
- Pre-launch: Recommend an appropriate pre-launch CTA (e.g., "Join the waitlist", "Get early access")
- Launch: Recommend an appropriate launch CTA (e.g., "Try it free", "Start your trial", "Learn more")
- Post-launch: Recommend an appropriate post-launch CTA (e.g., "See how it works", "Book a demo")
**Key Features to Highlight:** Extract key features from the product details provided.
**Social Proof Available:** Include any testimonials, metrics, or logos available from the customer research.
**Brand Voice:** Consistent with the brand voice established in {{steps.Launch Messaging Development.output}}.
**Sender Name & Email:** Use an appropriate sender name placeholder.

## Email Sequence

Design a 6-email sequence across three phases:

### Pre-Launch Phase

**Email 1: Teaser (L-14 days)**
Purpose: Build anticipation and capture early interest

- **Subject Line:** [compelling, curiosity-driven, 6-10 words, no spam triggers]
- **Preview Text:** [30-50 characters extending the subject line]
- **Body:** Open with a hook that speaks to the audience's pain point. Hint at the solution without revealing full details. Build anticipation for the launch date. Keep to 100-150 words.
- **CTA:** the recommended pre-launch CTA
- **Design Notes:** [visual direction, key image/graphic, layout suggestion]

**Email 2: Countdown (L-3 days)**
Purpose: Remind and deepen interest with a preview of what is coming

- **Subject Line:** [urgency + specificity]
- **Preview Text:** [extending the subject]
- **Body:** Reveal more detail about the product — one key feature or benefit. Include a specific date and time for the launch. Create anticipation for what they will get access to. 120-160 words.
- **CTA:** the recommended pre-launch CTA or "Mark your calendar"
- **Design Notes:** [countdown element, feature preview visual]

### Launch Phase

**Email 3: Launch Announcement (L-Day)**
Purpose: Announce the product and drive immediate action

- **Subject Line:** [clear announcement, product name included, high-energy]
- **Preview Text:** [key benefit in preview]
- **Body:** Lead with the announcement. State what the product is and what it does. Highlight the top 3 benefits (not features). Include social proof if available. Create urgency or exclusivity if appropriate (launch offer, limited early access). 150-200 words.
- **CTA:** the recommended launch CTA [make the button prominent and the action clear]
- **Design Notes:** [hero image of product, prominent CTA button, feature highlights below fold]

**Email 4: Feature Deep-Dive (L+3 days)**
Purpose: Address the "how does it work?" question for interested but unconverted readers

- **Subject Line:** [specific feature or use case focused]
- **Preview Text:** [complementing the subject]
- **Body:** Focus on one messaging pillar in depth. Walk through a specific use case or scenario. Show, do not tell — use a concrete example. Address a common objection or concern. 150-200 words.
- **CTA:** the recommended launch CTA
- **Design Notes:** [screenshot or GIF showing the product in action, step-by-step visual]

### Post-Launch Phase

**Email 5: Social Proof (L+7 days)**
Purpose: Build confidence for hesitant prospects with proof from others

- **Subject Line:** [customer-focused, results-oriented]
- **Preview Text:** [teasing the proof]
- **Body:** Lead with a customer testimonial or early adopter result. Include a specific metric or outcome if available. Address the "people like me are using this" motivation. Reinforce the key benefit. 120-160 words.
- **CTA:** the recommended post-launch CTA
- **Design Notes:** [customer photo/logo, quote block, results metrics]

**Email 6: Last Chance / Follow-Up (L+14 days)**
Purpose: Final conversion push for engaged but unconverted contacts

- **Subject Line:** [urgency + value reminder, not pushy]
- **Preview Text:** [what they are missing]
- **Body:** Acknowledge they have been considering the product. Summarise the value proposition in fresh language. If there is a launch offer expiring, mention the deadline. Offer an alternative next step for those not ready to commit (webinar, guide, demo). 120-150 words.
- **CTA:** Primary: the recommended launch CTA | Secondary: the recommended post-launch CTA
- **Design Notes:** [clean, simple design, dual CTA buttons]

## Segment Variations

For each email, note where the copy should be adapted for different audience segments:
- **Segment A (primary audience):** Emphasise [specific angle]
- **Segment B (secondary audience):** Emphasise [specific angle]

Provide the specific subject line and opening paragraph variations for each segment for Emails 3 and 4 (the highest-impact emails in the sequence).

## Deliverability Notes
- Avoid spam trigger words (free, guarantee, limited time, act now)
- Keep subject lines under 50 characters where possible
- Include plain text version guidance
- Recommend send times based on general B2B/B2C best practices
- Include unsubscribe and preference centre reminders

Use British English throughout.
