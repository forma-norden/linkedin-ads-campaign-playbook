# linkedin-ads-outbound-sync

Use this skill to bridge the gap between LinkedIn Ads (Marketing) and
Cold Outbound (Sales). Ads should provide air cover for SDRs.

## Structural Alignment Protocols

### 1. The ABM Synchronization Play
Sales and Marketing attack the exact same target account list simultaneously.
- **Marketing:** Uploads the Target Account List (TAL) to LinkedIn as a Matched Audience. Runs Awareness and Case Study ads.
- **Sales:** Runs targeted cold email and LinkedIn DM outreach to the buying committee at those exact same accounts.
- **The Angle:** "I saw [Company] was engaging with our content regarding [Pain Point]..."

### 2. The Intent-Triggered Outbound Play
Marketing passes high-intent engagement data to Sales for immediate action.
- **The Signal:** A target account registers for a webinar or downloads a playbook via a LinkedIn Lead Gen Form.
- **The Routing:** n8n/Zapier pipes the lead into a specific SDR sequence in Outreach/Apollo.
- **The SLA:** Sales must reach out within 15 minutes of the form fill while the topic is top of mind.

### 3. The Retargeting Audience Builder
Sales provides data to fuel Marketing's retargeting efforts.
- **The Process:** Every time an SDR identifies a strong champion or has a positive "Not right now, maybe in 6 months" conversation, they tag the contact in the CRM.
- **The Sync:** A dynamic CRM audience syncs to LinkedIn Campaign Manager.
- **The Campaign:** Marketing runs "Nurture" campaigns specifically to this "Closed Lost / Timing" audience until they are ready to buy.

## Setting Up Intent Alerts for SDRs

Instead of expecting SDRs to check LinkedIn Campaign Manager, push the data to where they work.

1. Use **LinkedIn Website Demographics** to see which companies are visiting the site after seeing ads.
2. If a target account shows a surge in visits, trigger a Slack alert to the assigned SDR.
3. The SDR initiates a "Soft Touch" play—connecting on LinkedIn, commenting on posts, or sending a highly personalized, non-salesy email.

## Anti-Patterns in Sales/Marketing Sync

- Marketing launching ads to an audience Sales has never heard of.
- Sales doing cold outbound to accounts that Marketing has marked as "low priority."
- Sending a generic, automated "Thank you for downloading our eBook, want a demo?" email 24 hours later (too late, too generic).

## Output Contract
When advising on sync strategies, provide:
- The specific play (ABM Sync, Intent Trigger, or Nurture).
- The technical routing required between LinkedIn and the CRM/Outbound tool.
- A sample script/angle the SDR should use when following up on the ad engagement.
