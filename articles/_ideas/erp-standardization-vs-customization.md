# Article Idea: You're Customizing the Wrong Things: ERP, Process Standardization, and What AI Changes

**Slug:** `erp-standardization-vs-customization`
**Created:** 2026-04-12
**Priority:** 3
**Tags:** ERP, standardization, customization, process design, AI, manufacturing, SAP, implementation

---

## The Hook

> The orthodox advice on ERP implementation is: change your processes to fit the software, not the other way around. Most manufacturers ignore this and spend millions customizing. But the orthodoxy has a second half that nobody talks about: some processes are genuinely worth defending. The hard problem — and the one AI is about to make much harder — is knowing which is which.

## Core Argument / Thesis

Most manufacturers fail ERP implementations in a specific, predictable way: they customize extensively, justify it as protecting competitive advantage, and end up with an unmaintainable system that costs more to upgrade than to replace. The orthodox advice — standardize your processes to fit the software — is correct far more often than practitioners admit. But it's not universally correct, and the failure to distinguish "legacy habit dressed as operational identity" from "genuine process differentiation" is the root cause of most ERP disasters. AI is changing this calculus in two ways: it makes standard processes smarter (reducing the advantage of bespoke ones), and it makes customized systems increasingly incompatible with AI tooling trained on standard data models. The framework for when to standardize and when to customize has never been more important — or more urgently needed.

## Key Questions to Answer

1. Why do manufacturers consistently over-customize ERP, even when they know the orthodox advice? (Political incentives, power dynamics between IT and operations, fear of process change, vendor sales tactics)
2. What is the actual cost of customization — not just implementation cost but the ongoing tax on upgrades, talent, and AI compatibility?
3. How do you distinguish a process that is genuinely differentiating from one that is legacy habit? What questions surface the difference?
4. How does AI change the standardization calculus? (AI models are trained on standard data models; customized schemas degrade AI performance; standard processes generate comparable benchmarks that enable AI learning)
5. What does the right customization decision framework look like — and at what level of the stack should it be applied? (Data models vs. workflows vs. UI vs. reporting)
6. What do the best ERP implementations do differently — how do they handle the standardize/customize decision in practice?

## Why Now

SAP S/4HANA migration is forcing thousands of manufacturers to make implementation decisions right now — and the AI compatibility question is brand new. SAP, Oracle, and Microsoft are all building AI features on top of standard data models; customers with heavily customized instances are finding those features don't work for them. The cost of past customization is becoming visible in a new way. At the same time, a new generation of vertical SaaS ERP vendors (purpose-built for specific manufacturing verticals) argues that their standard processes are better fit than generic ERP — reducing the need to customize. The question of when to standardize and when to customize is being re-litigated in real time.

## Target Reader

A CFO, VP of IT, or VP of Operations at a mid-to-large manufacturer who is either in the middle of an ERP implementation, evaluating an upgrade to S/4HANA, or questioning why their existing ERP costs so much to maintain. Also: ERP implementation consultants who need a clearer framework for advising clients on scope.

## Potential Data / Analysis Angles

- **The customization cost model**: Total cost of ERP customization over a 10-year lifecycle — implementation, maintenance, upgrade friction, talent premium for custom-code expertise. Build a model with realistic inputs.
- **The AI compatibility gap**: Which SAP/Oracle/Microsoft AI features are unavailable or degraded for customers with custom data models? Map this with specifics.
- **Failure mode analysis**: Root cause analysis of ERP implementation overruns — what percentage trace to scope creep driven by customization?
- **The differentiation test**: A decision framework (quiz-style or matrix) for whether a process deserves customization. Test it against common examples (demand forecasting, production scheduling, quality holds, pricing).
- **Vertical SaaS as the standardization bet**: How purpose-built ERP vendors (Katana for discrete SMB, Rootstock for Salesforce-native manufacturers, Cetec for job shops) are winning by offering better standard processes, not more customization.

## Preliminary Sources / Leads

- SAP S/4HANA migration guides and upgrade complexity documentation
- Panorama Consulting ERP implementation failure reports (annual)
- Gartner "ERP Customization Best Practices" research
- McKinsey / Deloitte ERP implementation post-mortems
- SAP, Oracle, Microsoft documentation on AI features and data model requirements
- Interviews with ERP implementation consultants (SIs like Accenture, Deloitte, smaller boutiques)
- Case studies: manufacturers that standardized aggressively and won; manufacturers that customized and paid for it
- Literature on "business process reengineering" (Hammer & Champy) — the intellectual foundation of the standardize-to-fit-software orthodoxy

## Central Framework (to develop in outline)

**The Customization Decision Filter** — four questions applied to any process before deciding to customize:

1. **Is this process genuinely differentiating?** Would a competitor copying this process gain measurable advantage? If no → standardize.
2. **Is the standard process actually inferior — or just unfamiliar?** Have you modeled the outcomes of the standard process, or are you assuming it won't work? If just unfamiliar → standardize.
3. **What is the 10-year cost of defending this customization?** Including upgrade friction, talent, and AI feature incompatibility. If the cost exceeds the value → standardize.
4. **Can the differentiation be achieved above the data model layer?** Via workflow configuration, reporting, or UI rather than schema changes? If yes → standardize the data model, customize the layer above it.

The article's thesis is that manufacturers who apply this filter honestly find that fewer than 20% of their planned customizations survive it.
