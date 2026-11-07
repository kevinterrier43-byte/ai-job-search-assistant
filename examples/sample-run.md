# Sample Run (fictional)

An end-to-end example of the **company-job-hunt-outreach** skill. The company, people, and postings are made up. The structure matches a real run.

## Request

> Acme Analytics

## Source check

Resume: "Resume - Master" (last modified 2026-11-06 1:43 PM) · Preferences: "Job Preferences" (last modified 2026-11-01 9:12 AM)

## Step 1–2: Role screening

The agent found **47** open postings at Acme Analytics. **6** were plausible on title, and after screening:

| Role | Required quals met | Location | Pay | Eligibility | Result |
|---|---|---|---|---|---|
| Senior Data Analyst, Product (REQ-0001) | 6 of 6 | Chicago, hybrid | $120–140K | Likely (employer history only) | **Selected** |
| Analytics Engineer (REQ-0007) | 4 of 6 (gaps: Airflow, 3+ yrs Snowflake) | Remote | $130–150K | Likely | Runner-up |
| Data Scientist, Pricing (REQ-0012) | 3 of 6 (needs production ML) | NYC | $150–170K | Unknown | Skipped: stretch on core requirement |
| BI Developer (REQ-0019) | 5 of 6 | Onsite, Austin | $95–105K | Likely | Skipped: below pay floor |
| Data Analyst Intern (REQ-0023) | n/a | Chicago | n/a | n/a | Skipped: seniority (hard filter) |
| Data Engineer (REQ-0031) | n/a | n/a | n/a | Incompatible | Skipped: posting excludes requirement |

**Why REQ-0001:** asks for SQL, Tableau, A/B testing, and stakeholder-facing KPI work, all backed by resume bullets. Hybrid in Chicago matches the top location preference.

**Gaps to address:** posting prefers Looker; resume has Tableau (transferable, don't claim Looker).

## Step 3: Contacts

The agent then goes to the company's LinkedIn profile and parses through people at the company to identify relevant targets for outreach using a criteria I established myself.

| Contact | Title | Why them | Connection |
|---|---|---|---|
| Jordan Example | Analytics Manager, Product | Likely hiring manager (**inferred** from team and title) | 2nd degree, shared school |
| Sam Placeholder | Technical Recruiter | Recruits for data roles per their profile | Not connected |
| Riley Sample | Senior Data Analyst | Same team, could refer | 1st degree |

Checked: no prior messages or pending invites with any of the three.

## Step 4: Drafts

**Connection note → Jordan Example** (271 / 300 characters)

> Hi Jordan, I saw Acme is hiring a Senior Data Analyst on the product team. I've spent 5 years building product analytics and KPI dashboards in SQL and Tableau, and we both went to [school]. I'd love to connect and learn more about the team.

**Message → Riley Sample** (connected, resume attached)

> Hi Riley, I hope you're doing well. I'm interested in the Senior Data Analyst, Product role (REQ-0001): [link]. My background lines up closely: I owned 60+ dashboards and data models used across 6 teams and designed A/B tests on a personalization product. Would you be open to referring me? I've included a short blurb below you can paste into the referral form, and my resume is attached. Thank you!
>
> **Referral blurb:** Kevin is a product and data analyst with 5+ years of SQL, Tableau, and dbt experience who has owned analytics products end to end, from requirements to governance. He has designed A/B tests and KPI dashboards that guided product prioritization, which maps directly to this role's focus on product analytics.

## Step 5–6: Staged for review

| Contact | Draft | Chars | Resume | Status |
|---|---|---|---|---|
| Jordan Example | Connection note | 271 | N | Staged in tab, not sent |
| Sam Placeholder | Connection note | 254 | N | Staged in tab, not sent |
| Riley Sample | Message | n/a | Y (upload confirmed) | Staged in tab, not sent |

**Nothing has been sent.**

## Step 7: After approval

> **Me:** Send Riley and Jordan; hold Sam.
>
> **Agent:** Are you sure? This will send: (1) the message to Riley Sample with resume PDF attached, (2) the connection note to Jordan Example. Sam Placeholder stays unsent.
>
> **Me:** Yes.
>
> **Agent:** Sent: Riley (message delivered), Jordan (invitation pending). Held: Sam.
