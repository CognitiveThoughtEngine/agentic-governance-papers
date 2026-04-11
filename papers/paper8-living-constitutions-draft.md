# Paper 8 — Living Constitutions for AI (Draft)

**Title:** Living Constitutions for AI: Amendment-Driven Governance for Autonomous Systems

**Author:** Michael K. Saleme, Cognitive Thought Engine LLC

**Status:** In draft (Draft v1.0, April 10, 2026)

**Expected Publication:** Q2/Q3 2026 (Zenodo preprint)

---

## Abstract

Autonomous AI systems operating over extended time horizons face a governance problem that static rulebooks cannot solve: the rules themselves must evolve as the system encounters novel failure modes, regulatory changes, and operational realities that policy authors did not anticipate at deployment time. We argue that *living constitutions* — governance documents that incorporate formal amendment processes, ratification gates, citation mandates, and continuous enforcement verification — provide the missing primitive for governing AI systems that must adapt without losing accountability continuity.

We present the HRAO-E Constitutional Governance Architecture, a production system that has processed 64 constitutional amendments across 97 days of autonomous operation, governing 54 agents executing approximately 153 decisions per day. The architecture's Constitutional Governance Gate (CGG) enforces governance health as a pre-execution constraint: if the constitutional learning system is not functioning — if lessons are not being drawn from incidents, amendments are not being ratified, or documentation is stale — agent execution is throttled until governance health is restored.

Code-level enforcement — the Section 0.5 citation mandate requiring every gate decision to cite its constitutional section number, enforced by pre-commit hooks and achieving a 96/100 audit score with zero critical violations — closes the gap between written governance and running software. The 64-amendment record constitutes an auditable governance history that maps directly to EU AI Act Article 27 Fundamental Rights Impact Assessment (FRIA) requirements, providing the kind of traceable, versioned governance evidence that static documentation frameworks cannot produce by design.

We situate this work against constitutional theory (Hart, Fuller, Dworkin), related AI governance frameworks, and the EU AI Act compliance landscape approaching its August 2026 implementation deadline. We conclude that living constitutions are the missing governance primitive for autonomous AI systems — not because static rules are wrong, but because they cannot learn.

---

## Key Themes

- **The static ruleset problem:** Every production autonomous system operating over months will encounter failure modes that policy authors did not anticipate. Governance frameworks with no amendment mechanism are guaranteed to drift from operational reality — and the drift accelerates as autonomy increases.
- **Hart's secondary rules applied to AI:** The living constitution architecture introduces secondary rules explicitly — rules about how rules are created, modified, and enforced — which Hart identified as necessary for any effective legal system. Static AI governance frameworks are almost entirely primary-rule systems.
- **EU AI Act FRIA alignment:** The 64-amendment record, with ratification dates and incident triggers, produces the traceable governance evidence required by Article 27 Fundamental Rights Impact Assessment that static documentation cannot produce by design.

---

## Constitutional Theory Grounding

The paper draws on three constitutional theorists:

- **H.L.A. Hart** — Primary vs. secondary rules. Without secondary rules (rules about rules), governance cannot adapt or resolve conflicts. Static AI governance frameworks lack secondary rules entirely.
- **Lon Fuller** — Inner morality of law: non-retroactivity, stability, consistency. The 24-hour ratification cooling period implements Fuller's stability criterion.
- **Ronald Dworkin** — Law as integrity. Section 0.6 (Agent Character) provides the principled basis for agent behavior in novel situations not covered by any specific rule.

---

## Implementation

The CGG gate and amendment tracking infrastructure is implemented in:

- **constitutional-agent (PyPI):** https://pypi.org/project/constitutional-agent/
- **GitHub:** https://github.com/CognitiveThoughtEngine/constitutional-agent

---

## Related Papers

- [Paper 2 — Constitutional Self-Governance](paper2-csg.md): The constitutional document this paper's amendments evolve
- [Paper 4 — Harness Design](paper4-harness.md): Infrastructure that enforces constitutional citations
- [Paper 6 — Six-Gate Architecture](paper6-six-gate-draft.md): CGG gate in the full six-gate system
