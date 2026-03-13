# linkedin-ads-audience-targeting

Use this skill to build highly precise LinkedIn B2B audiences while avoiding
wasted spend on irrelevant clicks.

## Audience Building Strategies

### 1. Account-Based (Matched Audiences)
The gold standard for B2B.
- **Upload Method:** CSV of target company names/domains.
- **Layering:** Add Job Function/Seniority or specific Job Titles on top of the matched list.
- **Match Rate Expectation:** 80-95% for clean domain lists.

### 2. Attribute-Based (Broad ICP)
Used when expanding TAM or lacking a definitive target account list.
- **Core Layers:** Company Size + Industry + Job Function + Seniority.
- **Anti-pattern:** Using "Job Title" targeting combined with "Seniority". Job titles are messy; use "Function = Sales, Seniority = VP/CXO" instead of listing 50 variations of "VP Sales".

### 3. High-Intent Retargeting
Capturing demand that already exists.
- **Website visitors:** Build segments based on specific URL visits (e.g., `/pricing` vs `/blog`).
- **Single Image / Video Engagement:** Retarget users who watched 25%+ of a video ad or clicked a previous image ad.

## The Exclusion Protocol

Every campaign must have negative targeting. Exclude:
- Current customers (Upload list or CRM sync)
- Competitors
- Your own employees (Company = Your Company)
- Open pipeline/Active opportunities (CRM sync)
- Irrelevant functions (e.g., HR, Legal, Ops if targeting Marketing)

## Audience Size Guidelines

| Campaign Type | Minimum Size | Optimal Size |
|---------------|--------------|--------------|
| Cold / Brand | 20,000 | 50,000 - 150,000|
| ABM List | 2,000 | 10,000 - 30,000 |
| Retargeting | 300 | 1,000+ |

*Note: LinkedIn's absolute minimum is 300, but delivery suffers below 10k on cold audiences.*

## Output Contract
When designing an audience, provide:
- The primary targeting criteria (Attributes vs Matched lists)
- The exact layered filters to apply in Campaign Manager
- The mandatory exclusion list tailored to their business
- Expected audience size range
