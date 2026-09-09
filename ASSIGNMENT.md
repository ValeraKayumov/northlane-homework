# Senior AI Analyst - Take-home assignment

Improvado, Transformation Team. Deadline: 5 calendar days from receiving this kit. Deliverables in English.

## The situation

You are the analyst on a new client account. **Northlane Digital** is a marketing agency running paid media for three brands:

- **AUR** - Aurelia Skincare (US + EU markets)
- **PKF** - Peak Fuel Nutrition (US + CA)
- **NMB** - Nimbus Travel Gear (US)

You received raw exports covering **2026-05-01 to 2026-07-31**:

| File | What it claims to be |
|---|---|
| `campaigns_dim.csv` | Campaign dimension across platforms |
| `facebook_ads_daily.csv` | Meta daily performance |
| `google_ads_daily.csv` | Google Ads daily performance |
| `tiktok_ads_daily.csv` | TikTok daily performance |
| `ga4_sessions.csv` | GA4 daily sessions by source/medium/campaign |
| `crm_leads.csv` | CRM leads with UTM attribution, status, and deal amounts |

The client's CMO asks:

> "Which channel actually drives qualified pipeline for each brand, and where would you shift $20k of monthly budget? Also - why do the numbers in your reports never match what I see in Ads Manager?"

Like any real client data, these exports contain issues. Finding, quantifying, and correctly handling them **is** the assignment - nobody will tell you how many there are or where.

## Deliverables

**A. Transformation repo.** A dbt project (preferred) or structured SQL (DuckDB/Postgres/BigQuery - your pick) that builds, from the raw files: (1) a staging layer, (2) a unified daily cross-channel performance mart, (3) a channel -> lead -> SQL/won funnel mart joined to CRM. Include tests where they earn their place. It must run from a clean clone via README instructions.

**B. `DATA_QUALITY.md`.** A findings register: every data issue you found - the evidence (query + numbers), the business impact, and what you decided to do about it and why. A documented decision NOT to fix something is a valid entry.

**C. Client-facing one-pager (English).** Answer the CMO's question directly: channel/brand recommendation with numbers, the $20k reallocation, and a plain-language explanation of why dashboard totals differ from Ads Manager. Written for a CMO, not for an analyst.

**D. AI workflow appendix.** Two parts:
1. *How you actually worked:* which AI tools, for what, and at least one concrete case where the AI's output was wrong or misleading and how you caught it.
2. *Automation design:* a 1-2 page spec for an AI agent that would run data-quality checks on this pipeline automatically on every refresh. What is automated vs human-approved, how you would measure the agent's accuracy, and how you would build trust in it before letting it write anywhere.

## Rules

- **AI tools are allowed and expected.** We use Claude Code daily; pretending otherwise would be silly. What we grade is your judgment: what you asked, what you verified, and what you shipped.
- Any stack is fine as long as it runs locally from your README.
- If something is ambiguous, make an assumption, write it down, and move on - that mirrors the job.
- How much time each part deserves is your call. An honest "here is what I would do next with more time" section beats a gold-plated half-answer.

## What happens next

A 30-minute review call: a short walkthrough of your solution, a few questions about your code and decisions, and one small live exercise on the same dataset. Part of the call will be in English.
