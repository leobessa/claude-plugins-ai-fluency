---
name: ai-collaboration-modes
description: "Select appropriate human-AI collaboration modes: Automation (AI acts independently), Augmentation (AI assists human work), or Agency (AI takes delegated responsibility)."
version: "1.0.0"
---

# Overview

**AI Collaboration Modes** defines three distinct patterns for human-AI work: Automation, Augmentation, and Agency. Each mode has different characteristics, appropriate uses, and governance requirements.

**Core Principle:** The mode of collaboration should match the task characteristics, not default to a single pattern.

---

## When to Use This Skill

- Designing AI-assisted workflows
- Choosing how to apply AI to a task
- Setting appropriate oversight levels
- Defining accountability structures
- Scaling AI across an organization

---

## The Three Modes

### Mode 1: Automation

**Definition:** AI performs tasks independently with minimal human involvement.

**Pattern:**
```
Input → [AI Process] → Output → [Use]
           ↓
    (Monitoring only)
```

**Characteristics:**
- High volume, low variance tasks
- Standardized inputs and outputs
- Clear success criteria
- Low cost of individual errors
- Aggregate quality matters more than individual quality

**Examples:**
- Email categorization
- Data format conversion
- Basic content tagging
- Routine document generation
- Simple customer query responses

**Appropriate when:**
- Task is repetitive and well-defined
- Output can be monitored at aggregate level
- Individual errors are recoverable
- Human review would be inefficient
- Quality requirements are well-specified

**Governance requirements:**
- Automated quality monitoring
- Exception handling for edge cases
- Regular sampling and audit
- Clear escalation criteria
- Performance dashboards

**Risk profile:**
- Low risk per task
- Aggregate risk if systematic errors
- Risk of drift without monitoring
- Complacency risk over time

---

### Mode 2: Augmentation

**Definition:** AI assists human work, with humans retaining control and decision-making.

**Pattern:**
```
Input → [AI Draft/Analysis] → [Human Review/Edit] → Output
                ↓                       ↓
         (Assists human)        (Human decides)
```

**Characteristics:**
- Human expertise is essential
- AI accelerates or enhances human work
- Judgment required for final output
- Quality depends on human oversight
- Human retains accountability

**Examples:**
- Document drafting with human editing
- Research synthesis for human analysis
- Code suggestions for human implementation
- Data analysis for human interpretation
- Decision support (not decision-making)

**Appropriate when:**
- Human judgment is needed
- Stakes are significant
- Context matters
- Output requires accountability
- Quality is critical

**Governance requirements:**
- Clear human review process
- Documented approval workflow
- Training on AI limitations
- Verification protocols
- Accountability assignment

**Risk profile:**
- Dependent on human oversight quality
- Risk of automation complacency
- Risk of output authority bias
- Mitigated by human in loop

---

### Mode 3: Agency

**Definition:** AI takes delegated responsibility for achieving objectives, with human oversight at strategic level.

**Pattern:**
```
Objective → [AI Planning] → [AI Execution] → [AI Evaluation] → Result
                ↓                                    ↓
        (Human approves plan)              (Human reviews result)
```

**Characteristics:**
- Multi-step, goal-oriented tasks
- AI determines approach within constraints
- Human provides objectives and boundaries
- Outcomes evaluated against goals
- Human oversight is strategic, not tactical

**Examples:**
- Research and analysis projects
- Complex document creation
- Multi-step workflow execution
- Investigation and synthesis
- Project-scoped tasks

**Appropriate when:**
- Task is goal-oriented, not script-defined
- Multiple approaches are valid
- Human time is the constraint
- Results can be verified
- Stakes warrant careful oversight

**Governance requirements:**
- Clear objective specification
- Defined boundaries and constraints
- Approval gates for significant actions
- Result verification process
- Clear accountability structure

**Risk profile:**
- Higher individual task risk
- Dependent on objective clarity
- Risk of scope creep
- Requires strong verification

---

## Mode Selection Framework

### Selection Criteria

| Factor | Automation | Augmentation | Agency |
|--------|------------|--------------|--------|
| **Task complexity** | Low | Medium | High |
| **Judgment required** | Minimal | Significant | At boundaries |
| **Human time available** | Low | Medium | Low |
| **Error cost** | Low | Medium | Variable |
| **Volume** | High | Medium | Low |
| **Standardization** | High | Medium | Low |

### Decision Tree

```markdown
START
  │
  ▼
Is the task repetitive with clear rules?
  │
  ├─ YES → Is individual error cost low?
  │         │
  │         ├─ YES → AUTOMATION
  │         │
  │         └─ NO → AUGMENTATION
  │
  └─ NO → Does task require human judgment?
           │
           ├─ YES → AUGMENTATION
           │
           └─ NO → Is task goal-oriented with clear success criteria?
                    │
                    ├─ YES → AGENCY
                    │
                    └─ NO → AUGMENTATION (default to human control)
```

### Mode Selection Template

```markdown
MODE SELECTION ANALYSIS

Task: [Description]

CHARACTERISTICS:
- Complexity: [Low/Medium/High]
- Volume: [Low/Medium/High]
- Judgment needed: [Minimal/Moderate/Significant]
- Error cost: [Low/Medium/High]
- Standardization: [Low/Medium/High]

CANDIDATE MODES:
□ Automation - because: [rationale]
□ Augmentation - because: [rationale]
□ Agency - because: [rationale]

SELECTED MODE: _______________

GOVERNANCE FOR THIS MODE:
- Oversight level: [Describe]
- Review process: [Describe]
- Quality checks: [Describe]
- Escalation criteria: [Describe]
```

---

## Mode Transitions

### When to Shift Modes

**Automation → Augmentation:**
- Error rates increase
- Edge cases become common
- Stakes increase
- Regulations change

**Augmentation → Automation:**
- Process becomes stable
- Human review adds little value
- Volume increases
- Confidence in AI quality

**Augmentation → Agency:**
- Human time is the bottleneck
- AI demonstrates reliability
- Goals can be clearly specified
- Results can be verified

**Agency → Augmentation:**
- Results are inconsistent
- Objectives are unclear
- Stakes increase
- More control needed

---

## Hybrid Patterns

### Multi-Mode Workflow

```markdown
EXAMPLE: Content Creation Pipeline

Stage 1 (Automation):
  - Topic categorization
  - Initial research compilation
  - Basic fact extraction

Stage 2 (Agency):
  - Draft creation to specification
  - Structure and organization
  - Reference integration

Stage 3 (Augmentation):
  - Human review and editing
  - Tone and voice adjustment
  - Final approval

Stage 4 (Automation):
  - Formatting
  - Publishing
  - Distribution
```

### Mode by Risk Level

```markdown
RISK-BASED MODE ASSIGNMENT

Low risk tasks → Automation
- Internal documentation
- Routine communications
- Data formatting

Medium risk tasks → Augmentation
- External communications
- Analysis and recommendations
- Decision support

High risk tasks → Augmentation with enhanced review
- Legal/compliance content
- Financial reporting
- Customer-facing commitments

Variable risk tasks → Agency with gates
- Research projects
- Complex analysis
- Multi-step workflows
```

---

## Practices

### Mode Audit

For existing AI use:

```markdown
MODE AUDIT

Current AI Applications:
| Task | Current Mode | Appropriate? | Recommended |
|------|--------------|--------------|-------------|
| [Task] | [Mode] | [Yes/No] | [Mode] |

Gaps identified:
1. [Gap]
2. [Gap]

Changes needed:
1. [Change]
2. [Change]
```

### Mode Governance Matrix

```markdown
GOVERNANCE BY MODE

| Element | Automation | Augmentation | Agency |
|---------|------------|--------------|--------|
| **Oversight** | Aggregate | Per-output | Per-objective |
| **Review** | Sampling | All outputs | Results |
| **Approval** | Exception-based | Before use | Before execution |
| **Accountability** | System owner | Human reviewer | Delegator |
| **Monitoring** | Dashboards | Review logs | Outcome tracking |
```

---

## Assessment Criteria

**Mode Selection Proficiency When:**
- [ ] Can identify appropriate mode for any task
- [ ] Understands governance requirements per mode
- [ ] Can design hybrid multi-mode workflows
- [ ] Recognizes when mode transitions are needed
- [ ] Has documented mode assignments for key workflows

---

## Common Mode Failures

### Failure 1: Automation of High-Stakes Tasks

**Wrong:** Automating decisions that require judgment
**Right:** Use augmentation with human review for significant decisions

### Failure 2: Augmentation Overhead

**Wrong:** Human review of every trivial AI output
**Right:** Automate routine tasks, focus human time on value

### Failure 3: Agency Without Boundaries

**Wrong:** "Just figure it out" without constraints
**Right:** Clear objectives, defined boundaries, approval gates

### Failure 4: Static Mode Assignment

**Wrong:** Same mode forever regardless of results
**Right:** Regular review and mode adjustment based on performance

---

## Related Skills

- [ai-workflow-integration](../ai-workflow-integration/SKILL.md) — Implementing modes in workflows
- [ai-system-governance](../ai-system-governance/SKILL.md) — Governance by mode
- [ai-cognitive-readiness](../ai-cognitive-readiness/SKILL.md) — Knowing when AI should act independently

---

## Learn More

- [Mode Selection Examples](references/mode-examples.md)
- [Governance Templates by Mode](references/mode-governance.md)
