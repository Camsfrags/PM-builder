# PM Discovery Agent — Example Output

## Desired Outcome (Teresa Torres Framework)
**Business outcome:** Increase 30-day retention from 23% to 50% — measured by users who log at least 3 financial events in their first 30 days.

**User outcome:** "I want to feel in control of my MEI finances without needing an accountant or spending more than 10 minutes per week on it."

**The "AND" statement (Torres):** When users consistently log their finances without friction (user outcome), they stay active in the app long enough to see its value (business outcome). Both outcomes are served by reducing the cognitive load of first-time use — not by adding more features.

---

## Opportunity Solution Tree (OST)

**Outcome:** Increase 30-day retention from 23% to 50%

  └── **Opportunity 1:** Freelancers feel lost on Day 1 — they don't know what to do first and the app doesn't map to how they think about their finances
        └── Potential Solutions: MEI-specific onboarding wizard ("How do you receive payments? Per project / monthly retainer / mix"); "Your first action" prompt; Progressive disclosure hiding advanced features until week 2
        └── Riskiest Assumption: Users are leaving due to confusion, not because the core value proposition doesn't resonate with them

  └── **Opportunity 2:** Users don't trust the app's DAS calculation — they verify it manually on gov.br anyway, which defeats the purpose
        └── Potential Solutions: Plain-language "Your DAS this month is R$X because..." breakdown screen; Side-by-side gov.br comparison tool; One-tap DAS verification via Receita Federal API
        └── Riskiest Assumption: Users would stop manually verifying if the app showed its calculation reasoning transparently

  └── **Opportunity 3:** The app forces a monthly salary income model on freelancers who get paid per project, milestone, or retainer — creating constant friction
        └── Potential Solutions: "Project" as a first-class object (not just a transaction tag); Milestone payment tracker with expected vs. received toggle; Retainer vs. one-time income type at transaction creation
        └── Riskiest Assumption: The data model mismatch (salary logic vs. project logic) is the root cause of abandonment — not just a UX/labeling issue

  └── **Opportunity 4:** Freelancers don't know they're approaching the MEI annual revenue ceiling (R$81k) until it's too late — exposing them to financial and legal risk
        └── Potential Solutions: Live revenue ceiling progress bar on dashboard; Monthly alert: "You're at 73% of your MEI annual limit — here's what that means"; "What happens if I exceed R$81k" plain-language explainer
        └── Riskiest Assumption: Users are genuinely unaware of the ceiling risk — not aware but choosing to ignore it

  └── **Opportunity 5:** Freelancers cannot confidently price their services because no tool helps them calculate their real cost (taxes + non-billable hours + desired take-home)
        └── Potential Solutions: MEI Pricing Calculator wizard; "What should I charge for a 40h project?" step-by-step tool; Benchmark pricing by freelancer category (designer, dev, consultant)
        └── Riskiest Assumption: Pricing uncertainty is a felt pain strong enough to motivate downloading an app — making it an acquisition hook, not just a retention feature

---

## User Jobs (JTBD)

**Job 1: "When the 20th of the month arrives, I want to know exactly how much DAS I owe and confirm I have enough, so I can pay on time without hiring an accountant."**
- Type: Functional + Emotional (anxiety reduction)
- Current solution: Manually checking MEI Portal (gov.br) and cross-referencing with their own spreadsheet
- Satisfaction level: Low
- Evidence: 34% of beta support tickets reference DAS confusion; Reddit r/MEI thread (340 upvotes): "Nunca sei se o valor está certo mesmo usando app"

**Job 2: "When I finish a project, I want to generate a professional invoice quickly, so I can get paid without looking disorganized to my client."**
- Type: Functional + Social
- Current solution: Word/PDF manual templates or generic invoice generators not adapted to Brazilian NFS-e requirements
- Satisfaction level: Low
- Evidence: Conta Azul MEI invoice feature rated 2.8 stars on App Store; top complaint in 1-star reviews: "doesn't work in my city" (NFS-e municipality fragmentation issue)

**Job 3: "When a client pays late or in installments, I want my cash flow to update automatically, so I can decide whether to take new projects without doing math."**
- Type: Functional
- Current solution: Manual spreadsheet update after every payment change — described as "I gave up because I had to redo everything each time something changed" (churned user interview #2)
- Satisfaction level: Very Low
- Evidence: 23 of 47 support tickets cite confusion with partial or late payments; 3 churned user interviews confirm this as the primary abandonment trigger

**Job 4: "When January arrives and I need to file my DASN-SIMEI annual declaration, I want all my revenue already categorized, so I can file in under 30 minutes."**
- Type: Functional + Emotional
- Current solution: Retroactive manual categorization of 12 months of bank transactions — called "the worst week of the year" by 2 churned users
- Satisfaction level: Very Low
- Evidence: NPS verbatim (score: 28): "I downloaded 3 apps this year and none of them saved me time in January"; Sebrae 2023 report confirms DASN-SIMEI stress as top MEI pain point

**Job 5: "When a potential client asks for my price, I want to calculate my real hourly cost including taxes and unpaid hours, so I can quote confidently without underselling myself."**
- Type: Functional + Social
- Current solution: None — freelancers either guess or use generic calculators not adapted to MEI tax structure
- Satisfaction level: Not addressed by any competitor
- Evidence: "como precificar freelancer" — 22k monthly searches (SEMrush estimate); zero direct competitors solve this job in the Brazilian MEI context

---

## Pain Points

- **Pain:** App is built around fixed monthly income logic — doesn't handle project-based, irregular, or milestone-based payments natively.
  **Evidence:** 23/47 support tickets on partial payment confusion; 3 churned interviews: "the app doesn't understand how I get paid."
  **Frequency:** High | **Intensity:** High
  **Related OST opportunity:** Opportunity 3

- **Pain:** NFS-e (electronic invoice) systems vary per Brazilian municipality — no tool integrates with all 5,570 cities, leaving most users unable to generate compliant invoices in-app.
  **Evidence:** Conta Azul MEI App Store top 1-star complaint: "doesn't work in my city"; affects approximately 70% of municipalities with their own local NFS-e system.
  **Frequency:** High | **Intensity:** High
  **Related OST opportunity:** Opportunity 1 + Opportunity 2

- **Pain:** DAS calculation is opaque — users don't trust the app's number and check gov.br manually anyway, making the app redundant for its core promise.
  **Evidence:** Reddit thread (340 upvotes); 8 NPS verbatims; 34% of support tickets.
  **Frequency:** High | **Intensity:** Medium
  **Related OST opportunity:** Opportunity 2

- **Pain:** Accounting terminology (Pró-labore, Receita Bruta, Simples Nacional, Anexo III) is inaccessible to freelancers without accounting training.
  **Evidence:** 18 support tickets with "what category should I use?" questions; 2 churned interviews: "I didn't understand what to put where so I just stopped."
  **Frequency:** Medium | **Intensity:** High
  **Related OST opportunity:** Opportunity 1

- **Pain:** No tool warns users when approaching the MEI annual revenue ceiling (R$81k) — exposing them to automatic category change (Simples Nacional) with significant tax implications.
  **Evidence:** Sebrae 2023 MEI report: 28% of MEIs unknowingly exceed the annual limit; zero competitors show a live revenue ceiling warning.
  **Frequency:** Medium | **Intensity:** Very High (financial and legal risk)
  **Related OST opportunity:** Opportunity 4

---

## Market Gaps

- **Gap:** No tool provides plain-language DAS reconciliation that a person with zero accounting background can verify in under 2 minutes.
  **Affected job:** Job 1 (DAS payment confidence)
  **Market signal:** 340-upvote Reddit thread + 8 NPS verbatims + 34% of support tickets
  **OST opportunity:** Opportunity 2
  **Opportunity size:** Large

- **Gap:** No tool handles project-based income natively — all competitors assume a fixed monthly salary model.
  **Affected job:** Job 3 (cash flow with irregular income)
  **Market signal:** 23 support tickets + 3 churned interviews + App Store review pattern across 3 competitors
  **OST opportunity:** Opportunity 3
  **Opportunity size:** Large

- **Gap:** No tool proactively warns MEI users approaching R$81k with a clear "what happens next" explanation in plain language.
  **Affected job:** Job 4 (tax compliance without accountant)
  **Market signal:** Sebrae 2023 — 28% exceed limit unknowingly; zero competitors address this
  **OST opportunity:** Opportunity 4
  **Opportunity size:** Large

- **Gap:** No MEI-specific pricing calculator exists that factors in taxes, non-billable hours, and desired take-home pay.
  **Affected job:** Job 5 (confident pricing)
  **Market signal:** 22k/month searches for "como precificar freelancer"; zero direct solutions in the Brazilian MEI context
  **OST opportunity:** Opportunity 5
  **Opportunity size:** Medium-Large

---

## Competitive Landscape

- **Conta Azul MEI**
  Jobs addressed: Invoice generation (partial), DAS tracking
  Critical weakness: NFS-e works in approximately 30% of municipalities; UX rated "complex for non-accountants" in 67% of 1-star reviews on App Store
  OST implication: Opportunity 1 (Day 1 confusion) and Opportunity 2 (DAS trust gap) are wide open

- **Mobills / Organizze**
  Jobs addressed: Personal expense tracking, monthly budget categories
  Critical weakness: Built entirely for salaried employees — no MEI features, no DAS, no NFS-e, no project income model
  OST implication: Opportunity 3 (project-based income) is completely unaddressed by both

- **Granatum / Nibo**
  Jobs addressed: Full accounting for SMBs (invoicing, payroll, tax)
  Critical weakness: Priced for companies (R$99-299/month), requires accountant knowledge to operate, onboarding takes days
  OST implication: All 5 opportunities are open — these tools don't serve MEI self-service needs at any level

- **Spreadsheets (Excel / Google Sheets)**
  Jobs addressed: Everything — but entirely manually, with no MEI-specific logic
  Critical weakness: Breaks under irregular income; zero automation; no alerts; requires user to know accounting categories
  OST implication: The real competitor to beat — the spreadsheet habit is the default for 60%+ of MEI freelancers and represents the baseline all opportunities must outperform

---

## Assumption Mapping (Teresa Torres)

1. **Assumption:** Users abandon in the first 30 days because of confusion and UX friction — not because the core value proposition (financial control without an accountant) doesn't resonate.
   **Risk level:** High — if wrong, onboarding and UX fixes will not improve retention at all
   **Test method:** Exit survey triggered at Day 3 inactivity: "What stopped you from continuing?" with 4 options + open field
   **Timeline:** 1 week to instrument, 2 weeks to collect signal

2. **Assumption:** Users would trust the app's DAS number and stop checking gov.br manually if the app showed its calculation reasoning step by step.
   **Risk level:** High — if wrong, the trust gap is about accuracy (a data problem), not transparency (a UX problem)
   **Test method:** Paper prototype of "DAS breakdown screen" — show to 5 users and ask: "Would you still check gov.br after seeing this?" Measure yes/no ratio.
   **Timeline:** 1 week

3. **Assumption:** The mismatch between the app's salary-based income model and freelancers' project-based reality is causing active abandonment — not just mild annoyance.
   **Risk level:** High — if wrong, the fix is a glossary or tooltip, not a data model rebuild
   **Test method:** Interview 5 churned users with: "Walk me through the last time you tried to record a payment that felt wrong or confusing in the app."
   **Timeline:** 2 weeks

4. **Assumption:** Freelancers are genuinely unaware of the R$81k MEI revenue ceiling and its consequences — not aware but choosing to deal with it later.
   **Risk level:** Medium — affects whether this is an education feature or a risk-alert feature
   **Test method:** Add one question to next NPS survey: "Do you know the annual MEI revenue limit and what happens if you exceed it? Yes / No / I know it exists but not the details."
   **Timeline:** 3 days

5. **Assumption:** The pricing calculator (Job 5) is a strong enough pain point to drive app downloads — making it an acquisition hook, not just a retention feature.
   **Risk level:** Medium — affects where in the product funnel to build it (landing page vs. post-onboarding)
   **Test method:** Fake door — add "MEI Pricing Calculator" as a CTA on the landing page and measure click-through rate vs. other CTAs over 1 week
   **Timeline:** 1 week

---

## Recommended Discovery Cadence (Teresa Torres)

**Week 1 — Focus: Day 1 abandonment (Opportunity 1)**
- Interview 2 users who signed up but never returned (churned within first 7 days)
- Assumption to test: Confusion vs. lack of perceived value
- Deliverable: Updated OST branch for Opportunity 1 — promote or deprioritize based on evidence

**Week 2 — Focus: DAS trust gap (Opportunity 2)**
- Interview 2 active users while showing them the paper prototype of the "DAS breakdown screen"
- Assumption to test: Would showing calculation reasoning eliminate manual gov.br verification?
- Deliverable: Go/no-go decision on investing in DAS transparency feature

**Week 3 — Focus: Project-based income mismatch (Opportunity 3)**
- Interview 2 churned users using the "walk me through recording a payment" prompt
- Assumption to test: Is the pain a UX/labeling issue or a fundamental data model mismatch?
- Deliverable: Decision on scope — tooltip fix vs. data model rebuild for Opportunity 3

**Week 4 — Synthesis + OST update**
- Synthesize all 6 interviews + assumption test results from Weeks 1-3
- Update OST: promote top 2 opportunities, deprioritize or discard weakest ones
- Deliverable: Prioritized OST ready to inform next sprint planning

**Interview Starter Questions (MEI Freelancer Discovery — Teresa Torres continuous interviewing style):**
1. "Think about the last time you had to deal with your MEI finances — not in general, but the specific last time. What triggered it and what did you actually do, step by step?"
2. "Tell me about the last time you weren't sure if you were handling your MEI taxes correctly. What did you do to figure it out — and how did that go?"
3. "Walk me through what happens when a client pays you late or in installments. What do you do right after you receive that payment?"
4. "Have you ever downloaded a financial app and stopped using it? Tell me exactly what happened the last time that occurred."
5. "When you think about your MEI finances, what's the one thing that makes you most anxious — and what do you currently do about it?"
