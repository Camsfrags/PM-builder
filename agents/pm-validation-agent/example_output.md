# PM Validation Agent — Example Output

## Hypothesis Analysis
**Restated:** We believe that Brazilian freelancers (MEI/ME, 30k-100k BRL/year) will pay for an expense tracking app because manual categorization in spreadsheets consumes 15+ min/week and generates anxiety during tax season.

**Riskiest Assumption:** That the time spent on categorization is a *felt pain* significant enough to motivate payment — not just a mild inconvenience they've accepted.

**Why it's the riskiest:** Users may acknowledge the time cost but have adapted to it. Without confirming emotional intensity (stress, anxiety, tax season panic), there's no proof of willingness-to-pay.

---

## Test Design
**Recommended Methodology:** Problem Interviews (qualitative) + 1 Fake Door test (quantitative signal)

**Justification:** With R$300, 2 weeks, and no paid acquisition, you cannot run a statistically significant survey or A/B test. Problem interviews with 8 users from your existing Slack community will confirm whether the pain is real and intense. A fake door (a simple landing page with a "Join Waitlist" CTA) run in parallel gives a quantitative signal of intent.

**Execution Plan:**
1. Draft 7-question interview script focused on current behavior, not the solution
2. Recruit 8 freelancers from Slack community (send DM with 2-sentence pitch)
3. Run 30-min interviews over Days 3–8 (record with permission)
4. Simultaneously: designer builds a 1-page landing page describing the value prop
5. Share landing page link in 3 freelancer communities on Days 5–10
6. Synthesize interview findings using affinity mapping on Days 9–11
7. Compile results + go/no-go recommendation by Day 14

---

## Sample Size
**Recommended:** 8 problem interviews + 150 landing page unique visitors

**Minimum viable:** 6 interviews (below this, patterns are unreliable for qualitative research)

**Sampling Strategy:** Directly message members of the Slack community who match the ICP. For landing page traffic, post in 3 freelancer communities (Comunidade MEI Brasil, Freelas.io Discord, Designer Freelancer BR).

---

## Success Criteria
**Primary metric (Interviews):** >= 6 of 8 interviewees spontaneously describe tax season or categorization as a source of stress without prompting.

**Primary metric (Fake Door):** >= 8% waitlist conversion rate from landing page visitors (12+ signups from 150 visitors).

**Secondary metrics:**
- Average self-reported time on financial admin per week >= 20 minutes
- >= 4 interviewees mention having tried and abandoned an existing tool

**PASS:** Both primary metrics are met -> proceed to solution interviews + pricing test.
**FAIL:** Either metric is missed -> reframe hypothesis or pivot target audience.

---

## Timeline
**Week 1 (Days 1–7):**
- Day 1: Finalize interview script + recruit 8 participants via Slack DM
- Day 2: Designer builds landing page (1-pager, Carrd.co — free plan)
- Days 3–7: Run 5 interviews (30 min each) + publish landing page to 2 communities

**Week 2 (Days 8–14):**
- Days 8–10: Run remaining 3 interviews + post landing page to 3rd community
- Days 11–12: Affinity mapping of interview insights
- Day 13: Analyze landing page conversion data
- Day 14: Write synthesis doc + go/no-go recommendation

---

## Resources Needed
**People:**
- PM: ~12 hours total (recruiting, interviewing, synthesis, report)
- Designer: 5 hours (landing page design and copy)

**Tools (all free):**
- Carrd.co — landing page (free tier)
- Tally.so — waitlist form (free tier)
- Notion or Miro — affinity mapping (free tier)
- Loom or Google Meet — interview recording

**Budget Breakdown:**
- R$ 0 — all tools on free tiers
- R$ 300 — held in reserve for potential incentive if recruitment stalls (offer R$30 gift card to 10 participants)

---

## Risk Assessment
- **Risk 1: Low interview recruitment response** -> Mitigation: Send personalized DMs referencing a specific pain point; offer a 5-min async option via Loom if 30 min is too long
- **Risk 2: Landing page traffic too low for signal** -> Mitigation: Post in 5 communities instead of 3; ask 2 community admins to pin the post
- **Risk 3: Survivorship bias in Slack community** -> Mitigation: Explicitly recruit users who say they DON'T use any financial tool, not just those already interested in the topic

---

## Next Steps
**If PASS:** Run 5 solution interviews showing 3 different pricing models (R$19/mo, R$39/mo, R$9/mo). Goal: identify willingness-to-pay threshold.

**If FAIL:** Run 5 follow-up interviews with the question: "What would have to be true for you to pay for this?" Use answers to reframe the value prop or pivot to a different ICP (e.g., freelancers earning 100k-300k BRL/year with more complex tax situations).
