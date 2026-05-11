# Research Notes: Where Vibe Coding Breaks Down

**Article ID:** `vibe-coding-manufacturing-governance`
**Research Date:** 2026-05-10
**Status:** complete

---

## Research Summary

Citizen development and vibe coding are colliding with manufacturing at exactly the wrong moment. Adoption of low-code/no-code tools is accelerating (70-75% of new enterprise apps by 2025-26), but governance hasn't kept pace — 73% of low-code planners have no defined governance rules. In manufacturing specifically, this creates two distinct failure modes: shadow IT that fragments data and bypasses safety signals at the operational layer, and over-controlled IT backlogs that force operators into Excel workarounds at the productivity layer. The ISA-95 hierarchy maps cleanly to a governance framework: the answer to "should this be democratized?" is almost entirely determined by which level of the stack the software touches.

---

## Key Findings

### Finding 1: 73% of low-code adopters have no governance rules
**Source:** KPMG survey of 715 EMA companies, via txminds.com/blog/low-code-governance-citizen-development  
**Relevance:** Establishes the governance gap as a quantified, systemic problem — not an edge case.  
> "73% of low-code planners (and 65% of users) have not yet defined governance rules, which risks uncontrolled citizen development and the proliferation of shadow IT."

### Finding 2: 45% of AI-generated code contains security flaws
**Source:** Veracode 2025 GenAI Code Security Report, via baytechconsulting.com  
**Relevance:** Vibe-coded apps aren't just operationally risky — they're structurally insecure at a high base rate.  
> "Nearly 45% of AI-generated code contains security flaws. When LLMs are given a choice between a secure and insecure method, they choose the insecure path nearly half the time."

### Finding 3: Organizations without governance experience 3-4x more sprawl and violations
**Source:** Microsoft Power Platform Center of Excellence data, via valoremreply.com  
**Relevance:** Quantifies the cost of absent governance — not just risk, but measurable operational degradation.  
> "Organizations without formal Power Platform governance experience application sprawl, security violations, and compliance breaches at rates 3-4x higher than organizations with established Centers of Excellence."

### Finding 4: The ISA-95 / Purdue Model defines 5 levels of manufacturing software
**Source:** ISA.org, Siemens, itotinsider.com  
**Relevance:** This is the architectural foundation for the governance framework. Each level has fundamentally different risk profiles for citizen development.  
- **L0**: Physical processes (conveyors, motors, physical assets)
- **L1**: Intelligent devices — sensors, actuators, PLCs
- **L2**: Control systems — SCADA, HMI, DCS
- **L3**: Manufacturing operations — MES, quality management, maintenance systems
- **L4**: Enterprise — ERP, scheduling, financial planning

### Finding 5: Shadow IT accounts for 42% of average company's apps; slow IT response drives 38% of employees to it
**Source:** Productiv via G2, JumpCloud  
**Relevance:** Shadow IT in manufacturing isn't aberrant behavior — it's a rational response to IT backlogs. Over-centralization causes the problem it tries to prevent.  
> "42% of the average company's applications are the result of shadow IT. Slow IT response times drive 38% of employees towards shadow IT."

### Finding 6: The "hidden factory" — 20-40% of capacity consumed by unrecorded workarounds
**Source:** Armand Feigenbaum / Hakunamatatatech hidden factory analysis  
**Relevance:** Manufacturing has always had a shadow operation — Excel spreadsheets, paper logs, whiteboard schedules. Vibe coding is just the latest and most powerful form of this. The hidden factory concept gives the article historical grounding.  
> "The hidden factory refers to unrecorded and unmeasured activities — rework, scrap, manual workarounds — that can account for 20% to 40% of a factory's total capacity."

### Finding 7: OT/IT convergence has expanded the attack surface; ransomware against industrial operators up 46% in a single quarter (2025)
**Source:** Protiviti blog, IoT Security Institute, iot-analytics.com  
**Relevance:** The security stakes of unauthorized software in manufacturing are rising, not falling. A vibe-coded app that connects to OT networks is not a productivity tool — it's an attack vector.  
> "Ransomware attempts against industrial operators increased 46% in a single quarter [2025]. Attackers view manufacturing organizations as a path of least resistance."

### Finding 8: Tulip's governance model — role-based access, approval workflows, citizen developer framework with guardrails
**Source:** tulip.co, Gartner Peer Insights, AWS Partner blog  
**Relevance:** Tulip is the clearest existing example of the "paved road" governance model — operator-buildable within centrally governed guardrails.  
> "The platform empowers engineers with powerful no-code and low-code capabilities while providing the necessary guardrails through version control and edit access. Testing and approval workflows [enable] fast and safe publishing of applications."

### Finding 9: EU Cyber Resilience Act requires secure-by-design for software products — affects vibe-coded manufacturing apps
**Source:** ai-laws.org, Lawfare Media  
**Relevance:** Regulatory pressure is coming. Manufacturers deploying AI-generated or citizen-developed software face compliance exposure under CRA and potentially ISO/IEC 62443 for OT security.  
> "The EU Cyber Resilience Act requires manufacturers of software-based products to implement comprehensive cybersecurity requirements including developing products according to secure-by-design principles and conducting mandatory risk assessments."

### Finding 10: Mendix (Siemens-backed) and Power Platform have meaningful governance tooling; Appian provides audit trails for regulated industries
**Source:** Gartner Peer Insights, Mendix documentation, Microsoft Learn 2025 wave  
**Relevance:** Major platforms have governance infrastructure — but it requires deliberate configuration. The tools exist; the governance frameworks to apply them in manufacturing do not.

---

## Data Points & Statistics

| Stat | Value | Source | Year |
|------|-------|--------|------|
| Enterprise apps built with low-code/no-code | 70-75% of new apps | Gartner | 2025 |
| Low-code adopters with no governance rules | 73% | KPMG (715 companies) | 2024-25 |
| AI-generated code with security flaws | 45% | Veracode GenAI Report | 2025 |
| Shadow IT as share of company apps | 42% | Productiv | 2024 |
| Employees driven to shadow IT by slow IT response | 38% | Various | 2024 |
| Hidden factory capacity consumption | 20-40% | Feigenbaum / industry | Ongoing |
| Ransomware increase vs. industrial operators | +46% in one quarter | Protiviti | 2025 |
| Governance gap penalty (sprawl/violations) | 3-4x higher rate | Microsoft CoE data | 2024-25 |

---

## Key Players / Companies

| Company | Role | Relevant Details |
|---------|------|-----------------|
| Tulip | Operator-first low-code for manufacturing | Best example of paved-road governance; role-based access, approval workflows |
| Mendix (Siemens) | Enterprise low-code, manufacturing-focused | Strong governance; Siemens ownership gives OT/IT credibility |
| Microsoft Power Platform | Broad enterprise low-code | Center of Excellence toolkit; 3-4x governance penalty data |
| Rockwell Automation / FactoryTalk | Industrial automation, L1-L3 | Strong controls at lower ISA-95 levels; expanding to higher layers |
| Siemens Industrial Edge | IIoT and edge computing | Controlled app deployment at OT/IT boundary |
| Appian | Process automation | Audit trails; relevant for regulated manufacturing (pharma, food) |

---

## Expert Perspectives

**Jonas Berge (LinkedIn, ISA-95/Purdue architecture expert):**
> The key benefit of the Purdue model is that regardless of technology and vendor, people understand what a level 2 system means and where it fits in the overall architecture. Systems belonging to different levels are not mixed, which increases stability and security.

**Armand Feigenbaum (quality pioneer, "hidden factory" concept):**
> What is officially measured on the production floor often ignores a "shadow" operation — rework, workarounds, manual patches — that can account for 20% to 40% of total factory capacity.

---

## Counterarguments / Nuance

1. **"Governance stifles innovation"** — The real cost of over-governance is quantifiable (38% shadow IT rate driven by slow IT response). The article must acknowledge this is a real failure mode, not just a concern.
2. **"ISA-95 is outdated"** — True that cloud, IoT, and modern architectures are blurring ISA-95 level boundaries. The framework should acknowledge this and argue that the *governance principle* (lower = more controlled) survives even if the exact boundaries shift.
3. **"Operators are more capable than IT gives them credit for"** — Also true. The governance framework shouldn't be used to justify IT control-hoarding. The paved road model must genuinely enable democratization at the appropriate layers.

---

## Gaps / Open Questions

- **Specific manufacturing incident data**: No public data on safety near-misses or incidents directly caused by citizen-developed apps. This is anecdotal in practitioner discussions. The article should acknowledge this gap.
- **Adoption rates by ISA-95 level**: No data specifically on where citizen development is currently happening by layer. The article's framework is prescriptive; actual current-state mapping would strengthen it.
- **ROI of paved-road governance**: Limited quantitative data on outcomes when manufacturers implement structured (vs. either extreme) governance. Tulip case studies are the best available source.

---

## Source Library

| # | Title | URL | Type | Date |
|---|-------|-----|------|------|
| 1 | Low-Code Governance: A Framework for Citizen Development | txminds.com/blog/low-code-governance-citizen-development | Industry blog (KPMG data) | 2025 |
| 2 | Veracode 2025 GenAI Code Security Report | baytechconsulting.com/blog/ai-vibe-coding-security-risk-2025 | Security research | 2025 |
| 3 | Power Platform at Scale: Governance & CoE | valoremreply.com/resources/insights/blog/power-platform-at-scale | Microsoft partner analysis | 2025 |
| 4 | ISA-95 Standard Documentation | isa.org/standards-and-publications/isa-standards/isa-95-standard | Standards body | Ongoing |
| 5 | ISA-95 and the Purdue Model Explained | itotinsider.substack.com/p/isa-95-and-the-purdue-model-explained | Technical explainer | 2024 |
| 6 | Shadow IT Statistics | track.g2.com/resources/shadow-it-statistics | Market research | 2024 |
| 7 | Manufacturing OT Security Challenges | blog.protiviti.com/2026/01/16/manufacturings-ot-security-challenges | Consulting research | 2026 |
| 8 | Tulip Platform — Build, Govern, Scale | tulip.co/blog/build-govern-scale-key-takeaways-from-the-virtual-event | Vendor (primary source) | 2024-25 |
| 9 | EU Cyber Resilience Act and vibe coding | blog.ai-laws.org/bad-vibes-for-vipe-coding | Legal/regulatory analysis | 2025 |
| 10 | Hidden Factory concept | hakunamatatatech.com/our-resources/blog/hidden-factory | Manufacturing analysis | 2024 |
| 11 | OT/IT Convergence Security — Protiviti | blog.protiviti.com | Consulting research | 2026 |
| 12 | Microsoft Power Platform Governance 2025 Wave 1 | learn.microsoft.com/en-us/power-platform/release-plan/2025wave1 | Official documentation | 2025 |
