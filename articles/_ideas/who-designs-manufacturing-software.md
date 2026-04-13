# Article Idea: Nobody Knows How to Design Manufacturing Software (And It Shows)

**Slug:** `who-designs-manufacturing-software`
**Created:** 2026-04-12
**Priority:** 4
**Tags:** UX, product design, manufacturing software, operator experience, industrial software, product management

---

## The Hook

> The average MES interface looks like it was designed by someone who had heard of a factory but never visited one. The average consumer app looks like it was designed by someone who had never met an enterprise customer. Manufacturing software manages to be both.

## Core Argument / Thesis

Manufacturing software has a design problem rooted in a people problem: nobody with the right combination of skills is making the design decisions. Industrial engineers know the process but not software. Enterprise software PMs know software but not manufacturing. UX designers know design but not the domain. Operators know exactly what they need but lack the language to specify it — and are rarely asked. The result is software that operators route around, creating the shadow IT, paper-based workarounds, and Excel sprawl that every digital transformation project inherits. The vendors who crack this — and a small number are — share a specific organizational pattern: they've found a way to put operators at the center of the design process, not as a research input but as a design authority.

## Key Questions to Answer

1. Who is currently making design decisions in industrial software companies — and what is their background? (Engineering-led vs. PM-led vs. domain-expert-led)
2. What are the specific UX failure modes that result from each background mismatch? (Engineer-designed: feature-complete, workflow-hostile. PM-designed: well-structured, process-ignorant. UX-designed: beautiful, contextually wrong.)
3. What does the operator experience problem actually cost? (Workaround time, training cost, error rates, adoption failure, failed implementations)
4. Who are the vendors getting this right — and what organizational pattern explains it? (Tulip's operator-first model, Parsec's shop-floor-up design philosophy, others)
5. What does a manufacturing software design process that actually works look like? Who is in the room, what artifacts are produced, how are operators involved?
6. How is AI changing this — and in which direction? (AI could enable better operator interfaces; it could also enable vendors to skip the hard design work by making operators talk to a chatbot instead)

## Why Now

Two things are happening simultaneously. First, the "consumerization of enterprise software" trend has raised operator expectations — people who use beautiful consumer apps all day have less patience for terrible industrial software. Second, AI is creating a design fork: some vendors are using AI to build genuinely more adaptive, operator-friendly interfaces; others are using "just ask the AI" as an excuse to avoid designing good software at all. The question of who should design manufacturing software is also the question of which of these paths the industry takes.

## Target Reader

Two audiences: (1) Industrial software founders and product leaders trying to understand why their adoption numbers are disappointing and their customers keep building workarounds. (2) Digital transformation leaders at manufacturers who are evaluating software and want to know what good design actually looks like — so they can recognize it in vendor demos.

## Potential Data / Analysis Angles

- **The workaround cost**: What percentage of manufacturing operations rely on Excel, paper, or informal tools to supplement official systems? What does this cost in time, errors, and missed insights? (LNS Research, Gartner, IDC data available)
- **Background mapping of industrial software design teams**: Survey or LinkedIn analysis of job titles/backgrounds at 20 industrial software companies — who holds the design authority?
- **Adoption rate correlation**: Is there a correlation between operator involvement in software design and adoption rates / implementation success? Look for data in implementation case studies.
- **The Tulip model**: A detailed case study of Tulip's operator-first design approach — what they do differently, what outcomes it produces.
- **AI interface comparison**: Side-by-side evaluation of AI-enhanced manufacturing interfaces — which ones reduce operator cognitive load vs. which ones just add a chat window to a bad interface.

## Preliminary Sources / Leads

- Tulip's product philosophy and blog — they've written explicitly about operator-first design
- Parsec Automation (TrakSYS) design philosophy
- LNS Research: "The Operator Experience Gap" or similar
- Jakob Nielsen's work on industrial UX (older but foundational)
- "Design for the Factory Floor" — search for academic and practitioner literature
- Interviews with operators, production supervisors, quality engineers about software they actually use vs. officially use
- MESA International and its operator experience working groups
- Consumer-to-industrial UX crossover: designers who moved from consumer to industrial software (what surprised them)

## Central Framework (to develop in outline)

**The Four Designer Archetypes and Their Failure Modes:**

| Background | Strength | Characteristic failure |
|------------|----------|------------------------|
| Industrial engineer | Deep process knowledge | Designs for the process, not the person doing it. Feature-complete, workflow-hostile. |
| Enterprise software PM | Structured, scalable | Designs for the buyer (IT, procurement), not the user (operator). Passes demos, fails daily use. |
| Consumer UX designer | Operator empathy, clean interfaces | Contextually wrong. Beautiful interactions that don't map to shift work, gloved hands, loud environments, interrupted workflows. |
| The operator themselves | Knows exactly what's needed | Can't translate need into software specification. Produces shadow IT rather than requirements. |

**What good looks like:** A design authority that combines process knowledge (industrial engineer or experienced operator) with software fluency (PM or designer) — and a process that puts operators in design reviews, not just usability tests. The vendors winning on UX have found this combination. Most haven't.
