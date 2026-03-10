---
type: skill
id: launch-measurement
title: Launch Measurement
description: "Defines launch success metrics, tracking frameworks, and post-launch performance analysis methodology"
tags: [Production, Tested]
connections:
  - target: claude-service
    type: runs_on
  - target: product-launch-framework
    type: references
metadata:
  estimated_duration: "4-6 minutes"
  avg_tokens: 2500
---

## Capability

Establishes the measurement framework for a product launch — defining what success looks like, how to track it, and how to analyse results. Covers both the pre-launch setup of tracking infrastructure and the post-launch analysis of performance against goals.

## When to Use

- Setting up success metrics before a launch begins (measurement planning)
- Evaluating launch performance during the launch window (real-time monitoring)
- Conducting post-launch retrospectives (performance analysis)
- Comparing launch performance across multiple launches (benchmarking)
- Justifying launch investment to stakeholders (ROI reporting)

## Process

1. **Goal Definition** — Establish clear, measurable launch goals tied to business objectives:
   - **Awareness goals:** Media mentions, social reach, website traffic, search volume for brand/product terms
   - **Adoption goals:** Sign-ups, downloads, trial starts, demo requests, purchases
   - **Engagement goals:** Feature usage, activation rate, retention rate, NPS
   - **Revenue goals:** Revenue generated, pipeline influenced, deal acceleration

   Each goal must have a specific target number and timeframe (e.g., "500 trial sign-ups within 30 days of launch").

2. **Metric Framework Design** — Define the metrics hierarchy:
   - **North Star metric:** The single metric that best represents launch success
   - **Leading indicators:** Metrics that predict whether the North Star will be achieved (tracked daily during launch)
   - **Lagging indicators:** Metrics that confirm success after the launch window (tracked weekly/monthly)
   - **Diagnostic metrics:** Metrics that help explain why performance is above or below target (investigated when results are unexpected)

3. **Tracking Infrastructure** — Ensure all tracking is in place before launch:
   - UTM parameters for all marketing links (source, medium, campaign, content)
   - Dedicated landing pages with conversion tracking
   - Event tracking for key user actions (sign-up, activation, feature usage)
   - Attribution model selected and configured (first-touch, last-touch, multi-touch)
   - Dashboard built with real-time data for launch day monitoring

4. **Launch Day Monitoring Protocol** — Define what to monitor and how often during launch:
   - Real-time metrics: website traffic, sign-up rate, error rates
   - Hourly checks: social media engagement, email open rates, ad performance
   - Daily reviews: conversion rates, channel performance, media coverage
   - Escalation triggers: when to adjust tactics based on real-time data

5. **Post-Launch Analysis Framework** — Structure the retrospective:
   - Performance vs. goals (what hit target, what missed, by how much)
   - Channel effectiveness (cost per acquisition, ROI by channel)
   - Message effectiveness (which messaging resonated, which fell flat)
   - Audience analysis (which segments responded, which did not)
   - Timeline analysis (when did momentum peak and decline)
   - Competitive impact (any observable competitive response)

6. **Lessons and Recommendations** — Extract actionable insights:
   - What to repeat in future launches
   - What to change or eliminate
   - Budget reallocation recommendations based on channel ROI
   - Messaging refinements for ongoing marketing
   - Product feedback generated during launch

## Inputs

- Launch plan with goals and channel strategy
- Budget allocation by channel
- Current analytics infrastructure capabilities
- Historical launch data for benchmarking (optional)
- Launch metrics data (for post-launch analysis)

## Outputs

- Measurement framework with metric hierarchy
- Tracking setup checklist
- Launch monitoring dashboard specification
- Post-launch analysis report
- Lessons learnt document with recommendations
- Launch performance scorecard

## Constraints

- Goals must be specific and measurable — "increase awareness" is not a goal; "achieve 50,000 unique website visitors in launch week" is a goal
- Attribution is imperfect — acknowledge limitations honestly rather than presenting false precision
- Separate launch impact from baseline — compare against pre-launch baseline, not zero
- Do not optimise for vanity metrics — 10,000 page views with 0 sign-ups is a failure, not a success
- Include qualitative signals alongside quantitative data — customer feedback, sales team observations, and support ticket themes provide context that numbers alone cannot
