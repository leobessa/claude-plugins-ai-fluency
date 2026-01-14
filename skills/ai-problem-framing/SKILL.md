---
name: ai-problem-framing
description: "Turn vague intent into solvable structures with explicit objectives, constraints, success criteria, and clear human vs AI responsibility boundaries."
version: "1.0.0"
---

# Overview

**AI Problem Framing** is Layer 2 of AI fluency—the ability to transform fuzzy intent into structured problems that AI can solve well. This is the highest-leverage skill because AI amplifies your framing, not your intent.

**Core Principle:** AI doesn't solve problems—it amplifies the framing you give it.

**Fluency Signal:** Get high-quality output on the *first* iteration.

---

## When to Use This Skill

- Before any significant AI delegation
- When AI output keeps missing the mark
- When iteration feels random rather than directional
- When defining AI-assisted workflows
- When training others on effective AI use

---

## The Framing Framework

Every AI task requires three elements:

### 1. Explicit Objectives

**What you actually want**, not what you're asking for.

| Weak (Vague Intent) | Strong (Explicit Objective) |
|---------------------|----------------------------|
| "Analyze this data" | "Identify the 3 metrics most correlated with customer churn" |
| "Write about X" | "Draft a 500-word explanation of X for non-technical readers" |
| "Help me think about Y" | "Generate 5 distinct strategic options for Y with trade-offs" |
| "Improve this code" | "Reduce the time complexity of this function from O(n²) to O(n log n)" |

**Test:** Would two different AIs produce similar outputs from this objective?

### 2. Constraints

**Boundaries that shape the solution space.**

Types of constraints:
- **Format**: Length, structure, output type
- **Scope**: What's in/out of bounds
- **Style**: Tone, voice, technical level
- **Resources**: What information to use (or not use)
- **Quality**: Standards that must be met

**Example:**
```
Objective: Write a product description
Constraints:
- Maximum 150 words
- Include price and 3 key features
- Match brand voice (casual, confident)
- Do not mention competitors
- Must include call-to-action
```

### 3. Success Criteria

**How you'll know the output is good.**

Success criteria should be:
- **Specific**: Measurable or evaluable
- **Complete**: Cover all important dimensions
- **Prioritized**: Which matter most if trade-offs needed

**Example:**
```
Success criteria (in priority order):
1. Factually accurate (all claims verifiable)
2. Addresses all 3 user questions
3. Under 500 words
4. Professional tone
5. Includes recommended next steps
```

---

## Problem Decomposition

### Breaking Work into AI-Appropriate Chunks

Large problems require decomposition:

1. **Identify sub-tasks** - What distinct pieces of work exist?
2. **Sequence them** - What depends on what?
3. **Assign ownership** - Human, AI, or hybrid?
4. **Define interfaces** - What moves between steps?

### Decomposition Pattern

```
[Original Problem]
    ↓
[Sub-task 1: Research] → AI (good at synthesis)
    ↓
[Sub-task 2: Analysis] → Human (requires judgment)
    ↓
[Sub-task 3: Drafting] → AI (good at generation)
    ↓
[Sub-task 4: Review] → Human (requires accountability)
    ↓
[Sub-task 5: Refinement] → AI + Human (iteration)
```

### Artifact Mapping

For each sub-task, define:
- **Input artifact**: What goes in
- **Output artifact**: What comes out
- **Verification method**: How to check quality

---

## Human vs AI Responsibility

### What Must Stay Human

- **Final decisions**: AI advises, humans decide
- **Accountability**: You own the output
- **Value judgments**: Ethics, priorities, trade-offs
- **Verification**: Checking against reality
- **Context integration**: Understanding full situation

### What AI Does Well

- **Pattern synthesis**: Combining information
- **Variation generation**: Multiple options
- **Format transformation**: Restructuring content
- **Search augmentation**: Finding relevant information
- **Draft creation**: First-pass content

### The Boundary Decision

For each task element, ask:
1. Can AI do this reliably? (Capability)
2. Can I verify the output? (Verifiability)
3. Do I understand it enough to catch errors? (Expertise)
4. What's the cost of AI error? (Risk)

If any answer is unfavorable, keep it human.

---

## Practices

### Problem Statement Template

Before delegating, complete:

```markdown
## Problem Statement

**Objective:** [What I actually want to achieve]

**Context:** [Background AI needs to understand]

**Constraints:**
- [Constraint 1]
- [Constraint 2]
- [Constraint 3]

**Success Criteria:**
1. [Most important criterion]
2. [Second most important]
3. [Third most important]

**Out of Scope:** [What I don't want]

**Artifacts:**
- Input: [What I'm providing]
- Output: [What I expect back]

**Verification:** [How I'll check quality]
```

### Task → Artifact Mapping

For complex work:

| Task | Input | Output | Owner | Verification |
|------|-------|--------|-------|--------------|
| Research competitors | Industry list | Competitor profiles | AI | Spot-check 2-3 |
| Identify gaps | Profiles + our features | Gap analysis | Human | N/A (judgment) |
| Draft positioning | Gap analysis | Positioning options | AI | Review all options |
| Select positioning | Options | Decision + rationale | Human | N/A (decision) |

### Constraint-First Framing

Instead of starting with what you want, start with what you don't want:

1. List everything that would make output unacceptable
2. Convert to positive constraints
3. Prioritize constraints
4. Then add objectives

This prevents scope creep and ensures critical requirements aren't missed.

---

## Assessment Criteria

**Layer 2 Complete When:**
- [ ] Can write task specs that multiple AIs would handle consistently
- [ ] Distinguishes objectives from activities
- [ ] Specifies measurable success criteria before delegation
- [ ] Correctly assigns tasks to human vs AI ownership
- [ ] Has reduced iteration cycles through better framing

---

## Common Framing Failures

### Failure 1: Activity vs Outcome

**Wrong:** "Analyze customer feedback"
**Right:** "Identify the top 3 complaints and their frequency in customer feedback"

### Failure 2: Implicit Constraints

**Wrong:** "Write a blog post about AI"
**Right:** "Write a 800-word blog post about AI for marketing professionals, avoiding jargon, in our brand voice (examples attached)"

### Failure 3: Missing Success Criteria

**Wrong:** "Make this better"
**Right:** "Improve clarity for non-technical readers; success = a 10th grader can understand the main point"

### Failure 4: Unbounded Scope

**Wrong:** "Help me plan my project"
**Right:** "Create a 10-item task list for the research phase of the project, with dependencies and estimated durations"

---

## Related Skills

- [ai-instruction-design](../ai-instruction-design/SKILL.md) — Translating framing into prompts
- [ai-cognitive-readiness](../ai-cognitive-readiness/SKILL.md) — Knowing when to frame vs not delegate
- [ai-fluency-antipatterns](../ai-fluency-antipatterns/SKILL.md) — Vague Intent Delegation anti-pattern

---

## Learn More

- [Problem Statement Templates](references/problem-templates.md)
- [Decomposition Examples](references/decomposition-examples.md)
