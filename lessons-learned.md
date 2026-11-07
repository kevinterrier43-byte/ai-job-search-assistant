# Lessons Learned

Things I changed after using the workflow on my own job search.

## What worked

- **Asking for 3 roles, not 30.** Making the agent defend one pick per company, with gaps named, gave me better applications and less wasted time than a long list of matches.
- **Source checks.** Making the agent report which resume version and timestamp it used caught stale-source mistakes immediately.
- **Staging instead of sending.** Leaving drafts open in browser tabs let me make quick edits in context, then approve.
- **Writing samples.** Giving the agent real examples of how I write worked better than describing my "tone."

## What didn't work at first

- **One big prompt.** Discovery, screening, and outreach in one set of instructions was hard to debug. Splitting them into separate skills with clear inputs and outputs fixed that.
- **Trusting memory.** Early runs pulled details from older resume versions or past conversations. "Read fresh every run" is now rule #1.
- **Treating employer history as role eligibility.** A company having supported a requirement in the past doesn't mean a specific posting will. I added explicit labels (Confirmed / Likely / Unknown / Incompatible).
- **Ranking people by connection data.** The tool can't tell how well my friend actually knows someone. Now it ranks companies and roles, and my friend chooses who to ask.
- **Overstating skills.** Without a rule, drafts sometimes rounded "familiar with" up to "experienced in." The accuracy rules and master resume as the single source of truth fixed that.

## Revising instructions

I keep a running disagreement log: when I reject or rewrite an output, I note what was wrong and why. Every so often I turn those notes into instruction changes, then run the revised instructions through cross-model review (originally ChatGPT and Claude by hand, now Perplexity Model Council) until no model proposes further changes. Then I decide what to keep.

## What I haven't measured yet

I don't have rigorous numbers for time saved or response rates. The ~500 → 3 postings example is one company audit, not an average. Adding lightweight tracking is the next improvement.
