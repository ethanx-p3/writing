# Article Idea: Where Vibe Coding Breaks Down: A Governance Framework for Software in Manufacturing

**Slug:** `vibe-coding-manufacturing-governance`
**Created:** 2026-04-12
**Priority:** 1
**Tags:** software governance, vibe coding, manufacturing IT, safety, ISA-95, data models, citizen development, low-code, digital transformation

---

## The Hook

> Every knowledge worker can now vibe code a functional app in an afternoon. In most industries, that's a productivity unlock. In manufacturing, it could get someone killed — or corrupt the data models that every downstream system depends on. The question isn't whether to democratize software building on the factory floor. It's where to draw the fence.

## Core Argument / Thesis

Manufacturing is the clearest case study for why unconstrained software democratization fails — and for exactly where the boundaries should go. The ISA-95 hierarchy already encodes the answer: the lower you go toward physical processes, the more centralized control must be. The higher you go toward business logic and reporting, the more democratization is safe and valuable. A principled governance framework follows directly from this. Most manufacturers are getting it wrong in both directions: over-controlling productivity tooling that should be democratized, and under-controlling data models and workflows that must not be violated.

## Key Questions to Answer

1. What specific categories of manufacturing software are genuinely unsafe to democratize — and why? (Safety interlocks, PLCs, MES workflows, master data models, compliance reporting)
2. What categories are actively harmed by over-centralization — and what's the cost of not democratizing them? (Dashboards, work order UIs, shift handoff tools, operator-facing apps)
3. How does the ISA-95 / Purdue Model hierarchy map to a governance framework for software building rights?
4. What are the failure modes of unconstrained citizen development in manufacturing? (Shadow IT, data model fragmentation, safety signal bypass, compliance gaps)
5. What does a "paved road" governance model look like — where the safe path is also the easy path?
6. How are leading manufacturers and industrial software vendors actually solving this today? (Platforms like Tulip, Sight Machine, Plex, Rockwell's FactoryTalk — what controls do they bake in vs. expose?)

## Why Now

"Vibe coding" entered the mainstream vocabulary in 2025. AI coding assistants have made it genuinely easy for non-engineers to build functional software. Industrial low-code platforms (Tulip, Mendix, Appian) have been pushing citizen development in manufacturing for years. The two trends are now colliding: operators and engineers with no software background are building production-affecting applications. Most manufacturers have no governance framework to handle this. The failures are starting — shadow IT proliferation, inconsistent data, safety near-misses from well-intentioned but untested tooling.

## Target Reader

A VP of IT, Director of Digital Transformation, or VP of Operations at a mid-to-large manufacturer who is actively wrestling with the "how much should we let people build their own tools" question. Also: industrial software platform founders trying to understand where to draw the line in their permissioning models.

## Potential Data / Analysis Angles

- **The ISA-95 governance matrix**: A 2×2 or layered diagram mapping ISA-95 levels (0–4) to appropriate governance posture (fully locked → fully open). The central visual framework of the article.
- **Cost of over-centralization**: Data on IT backlog time, shadow IT prevalence, operator tool adoption rates when IT-built vs. operator-built
- **Failure mode taxonomy**: A structured table of citizen development failure modes in manufacturing (safety, data, compliance, integration) with real examples
- **Platform comparison**: How Tulip, Rockwell FactoryTalk, Siemens Industrial Edge, and others handle the governance question — what they lock vs. expose
- **The "paved road" model**: A framework diagram showing centralized guardrails (data models, APIs, safety interlocks) with a permissive build layer on top

## Preliminary Sources / Leads

- ISA-95 standard documentation and the Purdue Model
- Tulip's platform documentation — they've thought hard about this (operator-facing, low-code, manufacturing-specific)
- CISA / ICS-CERT guidance on OT/IT security (relevant to the safety argument)
- Gartner research on citizen development and low-code in industrial settings
- Rockwell Automation and Siemens product governance models
- Academic work on "sociotechnical systems" in manufacturing — the human-machine interface literature
- Manufacturing subreddit and LinkedIn practitioner discussions on shadow IT and citizen development
- Mendix, Appian, and Microsoft Power Platform case studies in manufacturing verticals

## Central Framework (to develop in outline)

**The Manufacturing Software Governance Stack** — four layers, each with a different governance posture:

| Layer | Examples | Governance posture |
|-------|----------|--------------------|
| **Physical control** (ISA-95 L0-L1) | PLCs, SCADA, safety interlocks | Fully locked. No citizen development. Period. |
| **Process execution** (ISA-95 L2-L3) | MES workflows, data models, quality holds | Centrally governed. Extensions allowed via approved APIs only. |
| **Operations visibility** (ISA-95 L3-L4) | Dashboards, OEE reporting, shift handoff | Paved road. Templates and guardrails provided; operators build on top. |
| **Business productivity** (ISA-95 L4+) | Scheduling tools, work order UIs, operator apps | Open. Democratize aggressively. |

The article's thesis is that most manufacturers are drawing the line in the wrong place — either too high (locking productivity tooling that should be open) or too low (letting citizen developers touch data models and workflows they shouldn't).

## Related Articles / Competitors

- Various "low-code in manufacturing" vendor content — all marketing, no governance framework
- "Citizen Development" Gartner reports — good data, too generic
- This article should be the first to map the governance question directly to the ISA-95 hierarchy with a prescriptive framework
