# Design Decisions

Short notes on why the workflow is built the way it is.

## 1. A configured agent instead of a custom app

I tested several AI job-search tools first. Most were built for mass applying, and none handled my specific filters or the referral-first approach. Perplexity Computer let me write my own instructions and reusable skills, connect my Google Drive and Gmail, and use Comet to act in a browser where I'm already logged into LinkedIn. That let me get a working system running without building and maintaining my own app.

**Tradeoff:** the logic lives in natural-language instructions, so it's less testable than code. The guardrails and the disagreement log are how I make up for that.

## 2. Quality over volume

The goal is the best 1 role per company, not every role that matches a keyword. Each run compares all plausible openings at a company against required vs. preferred qualifications, location, pay, seniority, and eligibility before recommending one. If nothing passes, the answer is "no good fit," and that's a valid output.

## 3. Read sources fresh every run

Resumes and preferences change often. I maintain a comprehensive master resume and several role-specific versions. Early on, the agent sometimes relied on an older copy it remembered. Now every run starts by reading the current documents from Drive and reporting the document name and last-modified time, so I can catch a stale source immediately.

## 4. Separate instructions, reference data, and operational data

- **Instructions** change rarely and only after I review them.
- **Reference data** (resume, preferences, writing samples) changes when my background or goals change.
- **Operational data** (target companies, people, roles) changes every session.

Keeping them apart means I can swap the target company list without touching the rules, and update the resume without rewriting prompts.

## 5. Split the work into focused skills

One giant prompt was hard to debug. I split the workflow by inputs and outputs:

| Skill | Trigger | Output |
|---|---|---|
| Company job hunt & outreach | I list company names | One best role + 3–5 contacts + staged drafts per company |
| Friend intro finder | I paste a friend's LinkedIn profile | Top roles reachable through that friend + an intro-request message |
| Networking follow-up check | Scheduled on weekdays | Triage of replies and referral links + drafted responses |

Each skill can be improved or tested on its own.

## 6. Human approval is a hard boundary

The agent drafts, stages, and pre-fills, but it never sends or submits. Messages are typed into the LinkedIn composer and left unsent, and application forms stop on the final review page. Sending needs my explicit approval of the specific item, then a final confirmation.

**Why:** a wrong message to a hiring manager can't be taken back. The time saved by automating the last click isn't worth that risk.

## 7. Cross-model review, with me as the tiebreaker

Different models catch different problems. I started by copying drafts between ChatGPT and Claude and asking each to critique the other until neither proposed changes. I now use Perplexity Model Council for this. Two models agreeing doesn't make an answer correct, so the final decision stays with me.

## 8. Match how I actually write

The agent reads a folder of real messages and emails I've written, so outreach sounds like me: direct, specific, and without corporate filler. A few of my writing preferences are encoded as hard rules (for example, "Thank you" instead of "Thanks").

## 9. Friends choose who to introduce me to

The friend intro finder originally ranked specific people to ask about. Connection data can't tell how well two people actually know each other, so I changed it to rank companies and roles and let my friend decide who to approach.
