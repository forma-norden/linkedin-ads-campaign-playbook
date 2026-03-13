# linkedin-ads-measurement-attribution

Use this skill to correctly track conversions, measure ROI, and set up
attribution models for LinkedIn campaigns.

## Tracking Infrastructure

### 1. The Insight Tag
The foundational pixel. Must be installed across all website pages.
**Function:** Enables retargeting, website demographics reporting, and browser-based conversion tracking.
**Setup:** Add to Google Tag Manager (GTM) or directly in `<head>`. Validate via the LinkedIn Campaign Manager interface.

### 2. Conversions API (CAPI)
Server-side tracking. Critical as browser tracking degrades.
**Function:** Sends conversion data directly from your server (or CRM) to LinkedIn, bypassing ad blockers and cookie restrictions.
**Setup:** Requires developer support or a middleware tool like Zapier/n8n/Ruler Analytics to pipe CRM stage changes back to LinkedIn.

## Defining Conversion Events

Do not rely solely on "Lead" forms. Define micro-conversions to train the algorithm faster:
- **Top of Funnel:** "Key Page View" (Visited pricing or product page)
- **Mid Funnel:** "Content Download" (Submitted form for asset)
- **Bottom Funnel:** "Demo Request" (Submitted high-intent form)
- **Pipeline:** "MQL/SQL Created" (Via CAPI when CRM status updates)

## Attribution Models in LinkedIn

LinkedIn offers different ways to credit an ad for a conversion:
- **Last Touch (Default):** The last ad they clicked or viewed gets 100% of the credit.
- **Even Credit:** All ads they interacted with split the credit equally.

### Click vs. View Attribution
By default, LinkedIn attributes a conversion if someone clicked an ad within 30 days, or viewed an ad within 7 days.
- **B2B Recommendation:** Shorten View attribution to 1 day if you have a high volume of traffic. Keep Click attribution at 30 days due to long B2B sales cycles.

## KPIs by Funnel Stage

| Stage | Primary Metric | Target Benchmark |
|-------|----------------|------------------|
| Cold / Awareness | Cost per Click (CPC), CTR | CTR > 0.4%, CPC < $8 |
| Warm / Consideration | Cost per Lead (CPL) | CPL $50 - $150 (depends on asset) |
| Hot / Capture | Cost per Pipeline Generated | Varies heavily by ACV. Target 3-5x Pipeline ROI. |

## Setting up Lead Gen Forms vs. Landing Pages

### Lead Gen Forms (Native)
- **Pros:** 2-3x higher conversion rate, auto-filled fields, lower CPL.
- **Cons:** Lower intent, requires Zapier/n8n to sync to CRM.

### Landing Pages
- **Pros:** Higher intent leads, forces them to consume your website copy.
- **Cons:** Higher barrier to entry, requires optimized mobile experience, higher CPL.

**Rule of Thumb:** Use Lead Gen Forms for Top/Mid-funnel content distribution. Use Landing Pages for Bottom-funnel Demo requests where you need them to understand the product before the call.
