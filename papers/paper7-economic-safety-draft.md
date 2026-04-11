# Paper 7 — AI Economic Safety Gates (Draft)

**Title:** AI Economic Safety Gates: Formalizing Economic Harm Prevention in Autonomous Agent Systems

**Author:** Michael K. Saleme, Cognitive Thought Engine LLC

**Status:** Pre-submission review (Draft v1.0, April 9, 2026)

**Expected Publication:** Q2 2026 (Zenodo preprint)

---

## Abstract

AI safety research has largely converged on three harm categories: deception, alignment failure, and uncontrolled capability escalation. Economic harm — the capacity of autonomous agents to deplete financial runway, execute negative-margin operations, or make irrecoverable capital commitments — receives almost no formal treatment in the safety literature, despite being a concretely observable failure mode in production systems.

We present the Economic Profitability Gate (EPG), a production-deployed safety enforcement mechanism that evaluates every significant agent action against quantitative economic thresholds before permitting execution. The EPG is one of six gates in the HRAO-E constitutional governance architecture, operational for 96 days as of April 9, 2026, governing 38 autonomous agents executing approximately 153 decisions per day.

The EPG architecture includes two evaluation modes: a standard revenue-based mode (gross margin floors, burn coverage ratios, runway thresholds) and a stage-aware PRE_REVENUE mode (Amendment 59, ratified 2026-03-18) that substitutes value-creation metrics when MRR equals zero, resolving a circular dependency that would otherwise permanently freeze agent activity during legitimate early-stage operation. Two hard constraints — HC-3 (runway never below 3 months) and HC-4 (no gate FAIL ignored >24 hours) — enforce economic safety at the absolute level, above any gate-level adjustment.

We argue that economic harm should be recognized as a distinct AI safety dimension alongside deception and alignment, present the EPG architecture as a replicable template for economic safety enforcement, and situate this work against existing frameworks (NIST AI RMF, EU AI Act, OWASP LLM Top 10) that do not address economic harm as a safety category. Production evidence from 96 days of deployment, including gate state history, FREEZE and THROTTLE periods, and Amendment 59's resolution of the PRE_REVENUE circular dependency, is presented in full.

---

## Key Themes

- **Economic harm as a safety dimension:** Runway depletion, negative-margin operations, irreversible capital commitments, and burn rate acceleration are safety problems — not merely business problems — because they cause irreversible harm at speeds that outpace human correction.
- **PRE_REVENUE circular dependency:** Revenue-based economic gates permanently freeze zero-revenue systems, preventing the agent activity needed to generate revenue. Amendment 59's stage-aware evaluation resolves this without weakening economic safety.
- **Framework gap:** NIST AI RMF, EU AI Act, and OWASP LLM Top 10 do not address economic harm as a formal safety category. The EPG architecture fills this gap with a replicable, production-validated template.

---

## Implementation

The EPG gate is implemented in:

- **constitutional-agent (PyPI):** https://pypi.org/project/constitutional-agent/
- **GitHub:** https://github.com/CognitiveThoughtEngine/constitutional-agent

---

## Related Papers

- [Paper 2 — Constitutional Self-Governance](paper2-csg.md): HC-3 and HC-4 as hard constraint foundations
- [Paper 5 — Community Security](paper5-community-security.md): Economic harm as a community security vector
- [Paper 6 — Six-Gate Architecture](paper6-six-gate-draft.md): EPG in context of the full six-gate system
