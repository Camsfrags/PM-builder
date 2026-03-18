# PM Roadmap Agent — Example Output

## Roadmap Summary
- **Product stage:** Growth
- **Period:** Q2 2026 (April–June)
- **Primary OKR:** Become the go-to financial tool for Brazilian MEI freelancers
  - KR1: 30-day retention 23% -> 50%
  - KR2: Weekly active users 340 -> 800
  - KR3: DAS-related support tickets reduced by 60%
- **Prioritization lens:** For a growth-stage product with retention as the primary KR, we weight validated opportunities (existing evidence) over assumed ones, and retention impact over acquisition impact. Job importance x satisfaction gap breaks ties.

---

## Prioritization Scoring

| Opportunity | OKR Impact | Job Importance | Satisfaction Gap | Confidence | Effort | Priority |
|-------------|-----------|----------------|-----------------|------------|--------|----------|
| Day 1 onboarding confusion | High | High | High | High (68% Day 1 drop) | Medium | NOW |
| DAS transparency gap | High | High | High | High (34% tickets) | Medium | NOW |
| Project-based income mismatch | High | High | High | High (3 interviews) | High | NOW |
| MEI revenue ceiling alert | Medium | Medium | High | Medium (Sebrae data) | Low | NEXT |
| Freelancer pricing calculator | Low (acquisition) | High | High | Medium (search data) | Medium | LATER |

---

## Roadmap Now/Next/Later

### NOW — Q2 2026 (April–June)

**1. MEI-First Onboarding Wizard**
- **Connected OKR:** KR1 (retention 23%->50%) + KR2 (WAU 340->800)
- **Connected Job (JTBD):** "When I first open the app, I want to understand what to do immediately, so I don't waste time figuring it out."
- **Connected OST Opportunity:** Day 1 onboarding confusion (68% Day 1 drop-off — highest confidence signal in the dataset)
- **Why NOW:** 68% of users drop on Day 1 — this is the single largest retention leak. Cannot improve retention without fixing the entry point. Medium effort, highest expected impact on KR1.
- **Success metric:** Day 1 completion rate from 32% to 60%; 30-day retention improvement of at least 8 percentage points within 6 weeks of launch

**2. DAS Plain-Language Breakdown Screen**
- **Connected OKR:** KR3 (DAS tickets -60%) + KR1 (retention — trust is a retention driver)
- **Connected Job (JTBD):** "When the 20th arrives, I want to know exactly what I owe, so I can pay without hiring an accountant."
- **Connected OST Opportunity:** DAS transparency gap (34% support tickets + 340-upvote Reddit thread + 8 NPS verbatims)
- **Why NOW:** Directly addresses KR3 (60% ticket reduction). DAS confusion is the #1 stated reason for low trust. If users don't trust the core feature, no other improvement matters. Low-medium effort with direct, measurable KR impact.
- **Success metric:** DAS-related support tickets reduced by 60% within 4 weeks of launch; manual gov.br verification clicks reduced by 40%

**3. Project-Based Income Model**
- **Connected OKR:** KR1 (retention 23%->50%) — confirmed as primary abandonment trigger in 3 qualitative interviews
- **Connected Job (JTBD):** "When a client pays in installments, I want my cash flow to update automatically, so I can plan without doing math."
- **Connected OST Opportunity:** Project-based income model mismatch (3 churned interviews + 23 support tickets)
- **Why NOW:** Highest qualitative confidence — 3 churned users named this as the reason they left. High effort but cannot be pushed to NEXT because it is actively causing churn today.
- **Success metric:** Partial payment support tickets drop to zero; 30-day retention for users who record a project-based payment reaches 55%+

---

### NEXT — Q3 2026 (July–September)

**4. MEI Revenue Ceiling Alert**
- **Connected OKR:** Supports next-quarter OKR on financial confidence and compliance
- **Connected Job (JTBD):** "When I approach my annual revenue limit, I want to be warned in plain language, so I can make decisions before it's too late."
- **Why NEXT and not NOW:** High importance but low urgency for users currently below 50% of the ceiling. Sebrae data is compelling but needs primary validation — we don't yet know if users are unaware vs. ignoring the limit. Q2 capacity is already full with 3 high-confidence items.
- **What needs to be true to promote to NOW:** NPS survey result shows >40% of users don't know the R$81k limit exists -> promotes to NOW immediately

**5. Freelancer Pricing Calculator (MVP)**
- **Connected OKR:** Potential acquisition hook for Q3 OKR — outside Q2 retention scope
- **Connected Job (JTBD):** "When a client asks my price, I want to calculate my real cost including taxes, so I can quote confidently."
- **Why NEXT and not NOW:** This is primarily an acquisition feature (22k monthly searches), not a retention feature. Q2 is retention-focused. Fake door test in Q2 will validate demand before we commit to building.
- **What needs to be true to promote to NOW:** Fake door landing page test achieves >8% CTR -> validates acquisition potential -> promote to Q3 NOW

---

### LATER — Q4 2026+

**6. NFS-e Municipality Integration**
- **Signal that put it here:** Conta Azul MEI's biggest weakness (works in ~30% of cities); consistent top complaint in App Store reviews across all competitors
- **Why not sooner:** Requires city-by-city API integration across 5,570 municipalities — massive engineering effort with unclear ROI per city. Needs market sizing analysis per city before prioritizing.
- **What needs to happen to promote to NEXT:** Map top 20 cities by freelancer density + confirm API availability. If 80% of users are covered by top 20 cities, promotes to NEXT with scoped effort.

---

## Dropped Items

**Social/Community Features ("see what other freelancers earn")**
- **Reason dropped:** No connection to any Q2 OKR or validated user job. Zero signal in discovery data. Suggested by one stakeholder — not by user research.
- **What would bring it back:** Discovery evidence showing social comparison as a top-5 user need

**AI-Powered Expense Categorization**
- **Reason dropped:** High effort, medium impact on Q2 KRs. The root cause of abandonment has been validated as income model mismatch — not categorization confusion. Solving the wrong problem at high cost.
- **What would bring it back:** Post-Q2 data showing categorization (not income model) as the primary abandonment driver

---

## Stakeholder Narrative

"This quarter we are laser-focused on retention because we have strong signal that 68% of users
never get past Day 1, and those who do churn primarily because the app doesn't understand how
freelancers actually get paid — in projects and installments, not monthly salaries.

We are solving three problems in Q2: rebuilding the first-time experience so new users immediately
understand what to do; making DAS calculation transparent so users stop manually verifying on
gov.br and start trusting us; and building project-based income tracking so the app finally
matches how freelancers work.

We are NOT working on the pricing calculator or NFS-e integration this quarter — not because
they aren't valuable, but because fixing retention comes first. A leaky bucket with a beautiful
new feature is still a leaky bucket.

If we execute on these three items, we expect 30-day retention to move from 23% to at least
40% by end of June, with DAS support tickets dropping by 60%. In Q3, we shift to acquisition
with the pricing calculator — but only after the retention foundation is solid."

---

## Risks & Dependencies

- **Risk 1: Project-based income model requires backend data model change** -> Mitigation: Engineering spike in Week 1 of April to confirm scope. If effort exceeds 6 weeks, split into "milestone payments" (NOW) and "retainer tracking" (NEXT).
- **Risk 2: Onboarding wizard depends on knowing user's income type at signup** -> Mitigation: Add single-question income type survey at registration (1-day effort) before wizard build starts. This data feeds both onboarding and the income model feature.
- **Risk 3: DAS breakdown requires Receita Federal data reliability** -> Mitigation: Build with manual calculation display first (static, no API). Receita Federal API integration added as v2 only after static version is validated with users.
