---
type: document
id: launch-planning-playbook
title: Launch Planning Playbook
description: "Step-by-step guide to planning and executing a product launch marketing campaign"
tags: [Production, Tested]
connections:
  - target: product-launch-framework
    type: references
metadata:
  document_type: "playbook"
  audience: "marketing-teams"
---

## Launch Planning Playbook

This playbook provides a practical, step-by-step guide for planning and executing a product launch. It covers the full lifecycle from initial strategy through post-launch optimisation, with checklists and decision points at each stage.

### Before You Start: The Three Questions

Before investing any time in launch planning, answer these honestly:

1. **Is the product ready?** A premature launch damages credibility more than a delayed launch. If the product is not ready, push back on the date rather than launching something half-baked.

2. **Is there a real audience?** Who specifically will care about this launch? If you cannot name 5 real people who would benefit, the audience definition needs more work.

3. **What is the right launch tier?** Not everything deserves a Tier 1 launch. Overlaunching a minor feature trains your audience to ignore announcements. Underlaunching a major product wastes its market entry moment.

### Step 1: Assemble the Launch Team (L-8 weeks)

**Core team members:**
- **Launch lead (marketing):** Owns the plan, timeline, and coordination
- **Product liaison:** Provides product details, demos, and technical accuracy
- **Content creator:** Writes launch copy, blog posts, and campaign assets
- **Design:** Creates visual assets, landing pages, and email templates
- **Growth/paid:** Manages paid advertising and performance marketing

**Extended team (briefed, not daily involved):**
- Sales team (needs enablement materials)
- Customer success (needs training and documentation)
- Executive sponsor (approves positioning and major spend)
- Legal/compliance (reviews claims and messaging)

Establish a communication cadence: weekly standups for the core team, fortnightly updates for the extended team.

### Step 2: Define Positioning (L-7 to L-6 weeks)

This is the most important step. Everything else flows from positioning.

**Process:**
1. Gather inputs: product brief, customer research, competitive analysis, market context
2. Run the positioning-statement-writer prompt to generate variants
3. Test positioning with 3-5 people from the target audience (even informal conversations count)
4. Select and refine the winning positioning
5. Get executive approval

**Output:** Approved positioning statement, messaging pillars, and messaging hierarchy

**Common mistake:** Rushing through positioning to start creating assets. Assets built on weak positioning are polished but ineffective.

### Step 3: Build the Launch Plan (L-6 to L-5 weeks)

**Process:**
1. Determine launch tier based on the product-launch-framework criteria
2. Run the channel-strategy skill to evaluate and prioritise channels
3. Run the launch-plan-generator prompt to produce the comprehensive plan
4. Review plan with the launch team and extended stakeholders
5. Finalise budget allocation and get spending approval
6. Set up tracking infrastructure (UTM parameters, landing pages, event tracking)

**Output:** Approved launch plan with timeline, budget, and RACI

### Step 4: Create Campaign Assets (L-5 to L-2 weeks)

**Asset priority order:**
1. **Landing page** — The central destination for all launch traffic. Build first, test early.
2. **Email sequence** — Run the launch-email-sequence-builder prompt. Review, refine, load into the email platform.
3. **Press release** — Run the press-release-writer prompt. Get legal and executive approval.
4. **Sales enablement** — Battle cards, FAQ document, demo script, pricing guide.
5. **Social media content** — Platform-specific posts for pre-launch, launch day, and post-launch.
6. **Blog post** — Detailed announcement post for the company blog.
7. **Paid advertising creative** — Ad copy and visual assets for each paid channel.
8. **Support documentation** — Help articles, known issues, and customer communication templates.

**Quality checkpoint (L-2 weeks):** All assets complete and approved. If assets are not ready, consider delaying the launch rather than shipping unfinished materials.

### Step 5: Execute Pre-Launch (L-2 to L-1 weeks)

**Activities:**
- Send internal announcement (all-hands, Slack, email)
- Brief the sales team with enablement materials
- Brief customer success with training and documentation
- Send pre-launch teaser email (Email 1)
- Begin social media teaser content
- Conduct media briefings under embargo (Tier 1 only)
- Send countdown email (Email 2)
- Test all tracking links, landing pages, and conversion paths
- Verify email platform is configured and tested

**Pre-launch checklist:**
- [ ] Landing page live and tested on mobile
- [ ] All UTM parameters working and tracking in analytics
- [ ] Email sequence loaded, tested, and approved
- [ ] Press release approved by legal and executive team
- [ ] Sales team briefed and equipped
- [ ] Social posts scheduled
- [ ] Paid ads created and in review
- [ ] Support documentation published
- [ ] Monitoring dashboard configured

### Step 6: Launch Day Execution

**Hour-by-hour guide:**
- **08:00:** Team check-in. Confirm all systems ready.
- **09:00:** Publish blog post and update website.
- **09:30:** Send launch email (Email 3).
- **10:00:** Distribute press release. Post on social media.
- **10:30:** Activate paid advertising.
- **11:00:** Monitor first metrics. Check for issues.
- **12:00:** Team sync. Review initial reception. Address any problems.
- **14:00:** Second social media push.
- **16:00:** End-of-day metrics check. Adjust paid ads if needed.
- **17:00:** Team debrief. Plan for Day 2.

**What to monitor:**
- Website traffic (real-time)
- Email open rate and click rate
- Social media engagement
- Sign-up or conversion rate
- Error logs and support tickets
- Media coverage and mentions

### Step 7: Post-Launch Momentum (L+1 to L+4 weeks)

The biggest mistake teams make is treating launch day as the finish line. Launch day is the starting gun.

**Week 1:** Feature deep-dive email (Email 4), continued social posting, paid ad optimisation, media follow-up
**Week 2:** Social proof email (Email 5), customer story development, retargeting campaigns
**Week 3:** Last chance email (Email 6), content marketing (guides, tutorials, use cases)
**Week 4:** Performance review, strategy adjustment, transition to ongoing marketing

### Step 8: Post-Launch Analysis (L+4 weeks)

Run the post-launch-analysis-prompt with complete performance data. Produce a retrospective that covers:
- Goal performance scorecard
- Channel effectiveness analysis
- Messaging effectiveness analysis
- Lessons learnt
- Recommendations for ongoing marketing and future launches

Share the retrospective with the full launch team and extended stakeholders. The learnings are as valuable as the launch itself.

### Launch Planning Mistakes to Avoid

1. **Skipping positioning work** — Assets without strategy look pretty but underperform.
2. **Planning in isolation** — Marketing launches fail when sales, product, and support are surprised.
3. **Launching without tracking** — If you cannot measure it, you cannot learn from it.
4. **One-day mindset** — A launch is a 6-8 week campaign, not a single announcement.
5. **Copying the competition** — Your launch should reflect your positioning, not mimic a competitor's playbook.
6. **Ignoring qualitative signals** — Customer feedback and sales conversations reveal insights that dashboards miss.
