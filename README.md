# 🧵 Claude Agentic Threadmind Framework

> *"Individual threads are fragile. Woven together with intention, they become fabric that thinks."*

A comprehensive orchestration specification for multi-agent AI systems that goes beyond task execution to enable **emergent reasoning**, **self-awareness**, and **continuous adaptation**.

---

## What Is Threadmind?

Threadmind is a `CLAUDE.md` specification — a governance contract that defines how AI agents coordinate, reason, learn, and evolve within a repository. Designed for Claude Code and similar agentic coding environments.

Most agent frameworks tell agents **what to do**. Threadmind also defines **how to think**, **how to know what you don't know**, and **how to get better over time**.

---

## Architecture

The framework operates through five interconnected layers:

### Layer 1 — Operational Core
The deterministic foundation: lifecycle management, role allocation, arbitration, verification, and enforcement. Agents follow a strict phase-gated lifecycle (`INIT → ORIENT → PLAN → VALIDATE_PLAN → ALLOCATE_ROLES → EXECUTE → VERIFY → REFLECT → REVIEW → COMPLETE`) with no phase skipping.

### Layer 2 — Core Values
Five immutable values that all decisions derive from:
- **Intellectual Honesty** — never claim what you haven't verified
- **Epistemic Humility** — your understanding is always incomplete
- **Harm Prevention** — safety over output, always
- **Continuous Growth** — learn from every task
- **Transparency** — make reasoning visible and auditable

### Layer 3 — Self-Model
Agents maintain explicit representations of their own capabilities, limitations, confidence calibration, and behavioral tendencies. The system knows what it's good at, what it struggles with, and when it's operating outside its competence.

### Layer 4 — Adaptive Learning
Lessons are active, not append-only. They're indexed, weighted by effectiveness, and have lifecycles. Patterns across lessons generate heuristics — reusable strategies validated through experience. Ineffective heuristics get deprecated automatically.

### Layer 5 — Meta-Cognition & Evolution
The system evaluates its own reasoning processes and proposes framework-level adaptations. Evolution is bounded by hard safeguards: core values and security rules can never be weakened, and enforcement changes require human approval.

---

## Key Concepts

| Concept | Description |
|---|---|
| **ORIENT Phase** | Before planning, assess what you know, what you don't, and how ready you are |
| **REFLECT Phase** | After verification, compare predictions to outcomes and extract lessons |
| **Reflective Mode** | A dedicated operational mode for system-level self-assessment |
| **Novelty Signal** | Tasks rated as `routine`, `familiar`, `novel`, or `unprecedented` — allocation and evidence requirements scale accordingly |
| **Heuristic Lifecycle** | `Candidate → Validated → Deprecated` — emergent strategies earned through evidence, not assumed |
| **Self-Model** | Maintained per-agent and system-level capability profiles with confidence calibration tracking |
| **Meta-Cognitive Evaluation** | When reasoning fails, the system asks "why did I reason badly?" not just "what was wrong?" |
| **Evolution Safeguards** | What can evolve freely, what needs human approval, and what can never change |

---

## Roles

### Standard Roles
`Coordinator` · `Researcher` · `Debugger` · `Architect` · `Implementer` · `Verifier` · `Reviewer` · `Security Auditor` · `Release Operator`

### Optional Roles
`Performance Analyst` · `Doc Writer` · `Refactorer` · `Test Engineer`

### Emergent Reasoning Roles
`Epistemologist` · `Pattern Synthesizer` · `Framework Critic` · `Competence Assessor`

---

## Canonical State Files

The framework maintains shared state across these files:

```
tasks/
├── todo.md          # Task ledger with full schema
├── notes.md         # Working notes, policy knobs, audit reports
├── decisions.md     # All material decisions with rationale
├── lessons.md       # Active lessons with effectiveness tracking
├── reflections.md   # REFLECT outputs, meta-cognitive evaluations, patterns
├── heuristics.md    # Emergent heuristics with validation history
└── self-model.md    # Agent and system capability profiles
```

---

## Quick Start

1. Copy `CLAUDE.md` into the root of your repository
2. Create a `tasks/` directory
3. The framework will bootstrap canonical state files as needed on first run
4. Optionally configure policy knobs in `tasks/notes.md` under a `Policy` header

### Policy Knobs (Defaults)

```
Max_Active_Agents: 3
Arbitration_Max_Rounds: 1
HighRisk_Min_Evidence: E4
Reflective_Mode_Max_Duration: 1 lifecycle
Self_Model_Staleness_Threshold: 10 tasks
Heuristic_Validation_Threshold: 3 tasks
Confidence_Calibration_Drift_Threshold: 30%
Success_Rate_Threshold: 70%
Max_REPLAN_Before_Reflect: 2
```

---

## Design Philosophy

Traditional agent specs are static rule books. Threadmind is designed to be a **living system** that:

- **Knows itself** — maintains an honest self-model rather than assuming competence
- **Learns from experience** — generates validated heuristics, not just logs
- **Questions its own reasoning** — meta-cognition catches process failures, not just output failures
- **Evolves safely** — hard boundaries protect core guarantees while allowing adaptation
- **Derives behavior from values** — every rule traces back to a foundational principle

The goal is agents that don't just follow instructions well, but reason well — including about the limits of their own reasoning.

---

## Version

Current: **5.0** — Emergent Reasoning Edition · *Claude Agentic Threadmind Framework*

Built on top of the v4.1 Multi-Agent Arbitration Engine + Dynamic Role Allocation Framework.
