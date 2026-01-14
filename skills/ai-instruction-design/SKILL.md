---
name: ai-instruction-design
description: "Control AI output through structured specifications: define roles, scope, format, decision rules, and abstraction levels. Prompts become contracts, not requests."
version: "1.0.0"
---

# Overview

**AI Instruction Design** is Layer 3 of AI fluency—the ability to control output quality through structured instruction rather than trial-and-error prompting. This isn't about "prompt hacks" but about treating prompts as specifications.

**Core Principle:** Your prompts should look like specifications, not requests.

**Fluency Signal:** Produce stable outputs across multiple runs and models.

---

## When to Use This Skill

- Writing any prompt for non-trivial tasks
- When outputs are inconsistent across runs
- When AI ignores important requirements
- When teaching others effective prompting
- When creating reusable prompt templates

---

## The RSFDA Framework

Structured instructions have five components:

### 1. Role Definition

**What it does:** Establishes the perspective, expertise, and behavior AI should adopt.

**Elements:**
- Identity (who the AI is acting as)
- Expertise (what knowledge to apply)
- Perspective (what viewpoint to take)
- Constraints on behavior

**Examples:**
```
Role: You are a senior technical writer with expertise in API documentation.

Role: Act as a skeptical reviewer looking for weaknesses in arguments.

Role: You are a data analyst explaining findings to non-technical stakeholders.
```

**Common mistake:** Generic roles ("You are a helpful assistant") add no value.

### 2. Scope Bounding

**What it does:** Defines what's in and out of bounds.

**Elements:**
- What to address
- What to exclude
- What to assume
- What to ask about (vs assume)

**Examples:**
```
Scope:
- Focus only on the authentication module
- Do not suggest architectural changes
- Assume the existing API contracts cannot change
- Ask if you need clarification on any requirement
```

**Common mistake:** Unbounded scope leads to unfocused output.

### 3. Format Enforcement

**What it does:** Specifies output structure.

**Format types:**
- **Structured**: Tables, lists, JSON, markdown sections
- **Length**: Word/character limits, number of items
- **Template**: Specific sections and headings
- **Examples**: Show desired format

**Example:**
```
Format your response as:
## Summary (2-3 sentences)
## Key Findings (bulleted list, max 5 items)
## Recommendations (numbered, with rationale for each)
## Risks (table with columns: Risk | Likelihood | Impact | Mitigation)
```

**Common mistake:** Accepting prose when structure would be more useful.

### 4. Decision Rules

**What it does:** Specifies how to handle judgment calls.

**Elements:**
- Priorities when trade-offs needed
- Thresholds for inclusion/exclusion
- Handling of uncertainty
- Escalation criteria

**Example:**
```
Decision rules:
- Prioritize accuracy over comprehensiveness
- Only include findings with >80% confidence
- If uncertain, state the uncertainty rather than guessing
- Flag any recommendation that requires >$10K investment
```

**Common mistake:** Leaving judgment calls implicit.

### 5. Abstraction Control

**What it does:** Sets the level of detail and technical depth.

**Dimensions:**
- Technical level (expert/intermediate/beginner)
- Detail level (overview/detailed/exhaustive)
- Assumed knowledge

**Example:**
```
Abstraction level:
- Write for a technical audience familiar with Python but new to async programming
- Include code examples for each concept
- Skip basic syntax explanations
- Explain non-obvious design decisions
```

**Common mistake:** Mismatched abstraction wastes time on basics or confuses with unexplained complexity.

---

## Instruction Patterns

### The Specification Pattern

```markdown
## Objective
[What you want to achieve]

## Role
[Who the AI is acting as]

## Context
[Background information needed]

## Scope
- In scope: [what to address]
- Out of scope: [what to exclude]

## Format
[Output structure requirements]

## Decision Rules
[How to handle judgment calls]

## Quality Criteria
[What makes the output acceptable]

## Examples
[If helpful, show desired output style]
```

### The Contract Pattern

Write prompts as if they're contracts:

```markdown
GIVEN:
- [Input/context you're providing]
- [Assumptions that apply]

WHEN:
- [The task to perform]

THEN:
- [Expected output format]
- [Quality standards]
- [Constraints to respect]
```

### The Template Pattern

For repeatable tasks, create fill-in templates:

```markdown
Analyze [DOCUMENT_TYPE] for [PURPOSE].

Focus on:
- [FOCUS_AREA_1]
- [FOCUS_AREA_2]
- [FOCUS_AREA_3]

Output format: [FORMAT_SPECIFICATION]

Constraints:
- [CONSTRAINT_1]
- [CONSTRAINT_2]
```

---

## Practices

### Rewrite Prompts as Contracts

Take a vague prompt and transform it:

**Before:**
> "Review this code and tell me what's wrong"

**After:**
> "Review this Python code as a senior developer focused on:
> 1. Security vulnerabilities (SQL injection, input validation)
> 2. Performance issues (O(n²) or worse operations)
> 3. Maintainability concerns
>
> For each issue found:
> - State the problem in one sentence
> - Show the problematic code snippet
> - Provide a corrected version
> - Rate severity: Critical/High/Medium/Low
>
> If no issues found in a category, explicitly state that."

### Schema-First Prompting

Define output schema before writing the prompt:

1. What fields/sections do I need?
2. What data type is each field?
3. Are there constraints (length, format)?
4. Then write prompt to produce that schema

### "Bad Output → Fix the Spec" Loop

When output is wrong:
1. Don't immediately re-prompt
2. Identify specifically what's wrong
3. Find the spec gap that allowed it
4. Fix the specification
5. Re-run

This builds transferable skill; "try again" doesn't.

---

## Instructional Sequencing

### Order Matters

```
Most important → First (prime position)
Context → Before tasks (available when needed)
Format → Before asking for output (shapes generation)
Examples → Near the end (concrete reference)
```

### Chunking Complex Instructions

For complex tasks, break into clear sections:

```markdown
# ROLE
[Role definition]

# TASK OVERVIEW
[High-level objective]

# DETAILED REQUIREMENTS
## Part 1: [First subtask]
[Specific requirements]

## Part 2: [Second subtask]
[Specific requirements]

# OUTPUT SPECIFICATIONS
[Format and structure]

# QUALITY STANDARDS
[Success criteria]
```

---

## Assessment Criteria

**Layer 3 Complete When:**
- [ ] Prompts contain explicit role, scope, format, and criteria
- [ ] Can transform vague requests into structured specifications
- [ ] Outputs are consistent across multiple runs
- [ ] Same prompt works across different AI models
- [ ] Has documented "bad output → fix spec" iterations

---

## Common Instruction Failures

### Failure 1: Implicit Role

**Wrong:** "Summarize this article"
**Right:** "As a news editor writing for busy executives, summarize this article in 3 bullet points focusing on business implications"

### Failure 2: Missing Format

**Wrong:** "List the key points"
**Right:** "List exactly 5 key points, each as a single sentence starting with an action verb, in priority order"

### Failure 3: Ambiguous Decisions

**Wrong:** "Focus on what's important"
**Right:** "Focus on points that would change a reader's decision; exclude background information and context they likely already know"

### Failure 4: No Quality Anchor

**Wrong:** "Write a good summary"
**Right:** "Write a summary that passes this test: someone who only reads the summary should be able to explain the main argument to a colleague"

---

## Related Skills

- [ai-problem-framing](../ai-problem-framing/SKILL.md) — The framing that instructions encode
- [ai-reasoning-scaffolds](../ai-reasoning-scaffolds/SKILL.md) — Structuring reasoning within instructions
- [ai-4d-framework](../ai-4d-framework/SKILL.md) — Description component of 4D Framework

---

## Learn More

- [Instruction Templates](references/instruction-templates.md)
- [Format Specification Examples](references/format-examples.md)
