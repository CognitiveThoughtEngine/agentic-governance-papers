# Paper 4 — Harness Design

**Title:** Harness Design for Constitutional AI Organizations

**Author:** Michael K. Saleme, Cognitive Thought Engine LLC

**Status:** Published

**DOI:** [10.5281/zenodo.19343034](https://doi.org/10.5281/zenodo.19343034)

**Zenodo Record:** https://zenodo.org/record/19343034

---

## Abstract

A constitutional governance document is necessary but not sufficient for governing autonomous AI systems. The harness — the infrastructure layer that translates written constitutional principles into executable agent constraints — determines whether constitutional governance is operationally real or merely aspirational. This paper presents a systematic approach to harness design for constitutional AI organizations, grounded in 90+ days of production operation of the HRAO-E system. Core harness components include: gate architecture (six pre-execution evaluation gates with formal state transitions), hard constraint enforcement (17 constraints implemented as typed code prohibitions with runtime verification), audit trail infrastructure (constitutional section citations required in every gate decision, enforced by pre-commit hooks), and the RALPH Loop fault-tolerance protocol (persistent failure markers, circuit breakers, external verification, dead letter queues). The paper argues that the gap between written governance and running software is the primary failure mode for AI governance frameworks — and that harness design is the discipline that closes it.

---

## Key Findings

- The gap between written governance and running software is not closed by policy documents or behavioral guardrails — it requires enforcement infrastructure at the code level: pre-commit hooks, typed constraints, and runtime citation requirements.
- Constitutional section citations embedded in every gate decision (enforced by pre-commit hooks achieving a 96/100 audit score) create an auditable governance trace that maps written principles to execution history.
- The RALPH Loop resilience protocol (persistent Signs, circuit breakers, external verification, dead letter queues) reduces silent agent failure from weeks-long undetected outages to sub-24-hour detection and recovery.

---

## BibTeX

```bibtex
@article{saleme2026harness,
  author      = {Saleme, Michael K.},
  title       = {Harness Design for Constitutional AI Organizations},
  year        = {2026},
  doi         = {10.5281/zenodo.19343034},
  url         = {https://doi.org/10.5281/zenodo.19343034},
  publisher   = {Zenodo},
  institution = {Cognitive Thought Engine LLC, Texas},
  keywords    = {AI governance, harness design, constitutional agents, gate architecture, enforcement infrastructure}
}
```

---

## Implementation

The harness design described in this paper is implemented in the `constitutional-agent` Python library:

- **GitHub:** https://github.com/CognitiveThoughtEngine/constitutional-agent
- **PyPI:** https://pypi.org/project/constitutional-agent/

---

## Related Papers

- [Paper 2 — Constitutional Self-Governance](paper2-csg.md): Principles the harness implements
- [Paper 6 — Six-Gate Architecture](paper6-six-gate-draft.md): Full formal treatment of the gate system
- [Paper 8 — Living Constitutions](paper8-living-constitutions-draft.md): Amendment-driven evolution requiring harness update protocols
