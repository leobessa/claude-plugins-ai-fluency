---
name: ai-evaluation-verification
description: "Retain epistemic control by validating AI outputs against logic, first principles, and reality. Detect confident nonsense, false completeness, and category errors."
version: "1.0.0"
---

# Overview

**AI Evaluation & Verification** is Layer 5 of AI fluency—the ability to maintain epistemic control over AI outputs. AI fluency requires governance, not trust.

**Core Principle:** Treat AI output as a drafted hypothesis, not an answer.

**Fluency Signal:** Can reject plausible but incorrect AI output with justification.

---

## When to Use This Skill

- After any AI output you plan to use
- Before sharing AI-generated content
- When AI output "feels" right but isn't verified
- When stakes of error are significant
- When building verification into workflows

---

## Verification Framework

### The Three Validation Gates

Every AI output should pass three gates:

#### Gate 1: Logic Check

**Question:** Does the reasoning make sense?

**Checks:**
- Do conclusions follow from premises?
- Are there logical jumps or gaps?
- Is the reasoning circular?
- Are cause-effect claims valid?

**Red flags:**
- Conclusions stated without supporting reasoning
- "Because it's best practice" without explanation
- Jumps from observation to recommendation

#### Gate 2: First Principles Check

**Question:** Does this align with fundamental truths?

**Checks:**
- Consistent with domain knowledge?
- Violates any known constraints?
- Contradicts established facts?
- Makes physically/mathematically possible claims?

**Red flags:**
- Claims that seem too good to be true
- Violations of basic domain principles
- Numbers that don't add up

#### Gate 3: Reality Check

**Question:** Does this match external evidence?

**Checks:**
- Verifiable against authoritative sources?
- Consistent with observable reality?
- Can be independently confirmed?

**Red flags:**
- Specific facts without citations
- Claims about recent events (training cutoff)
- "All experts agree" statements

---

## Error Detection Patterns

### 1. Confident Nonsense

**What it is:** Fluently stated information that is factually wrong.

**Detection:**
- Check specific facts, especially dates, numbers, names
- Verify citations actually exist
- Cross-reference with authoritative sources
- Ask for sources and verify them

**Example:**
> AI: "According to Smith (2022), the algorithm has O(log n) complexity..."
> Verification: Does Smith (2022) exist? Does it make this claim?

### 2. False Completeness

**What it is:** Output presented as comprehensive when it's partial.

**Detection:**
- Ask: "What did you NOT include?"
- Check if obvious items are missing
- Compare against known complete lists
- Request exhaustiveness check

**Example:**
> AI: "The main programming paradigms are: object-oriented, functional, procedural"
> Missing: Logic programming, concurrent, aspect-oriented, etc.

### 3. Category Errors

**What it is:** Mixing categories or applying concepts incorrectly.

**Detection:**
- Check if terms are used correctly
- Verify categorizations make sense
- Look for inappropriate analogies
- Check if advice fits the category

**Example:**
> AI: "To improve database performance, refactor your frontend components"
> Error: Mixing frontend/backend categories

### 4. Anchoring on False Premises

**What it is:** Building correct reasoning on user's incorrect assumptions.

**Detection:**
- Review your input for errors
- Check if AI questioned problematic premises
- Test by deliberately introducing errors

**Example:**
> User: "Explain why Python is faster than C"
> AI: [Provides explanation for a false premise]

### 5. Temporal Confusion

**What it is:** Mixing past, present, future inappropriately.

**Detection:**
- Verify timelines
- Check if claims about "current state" are current
- Watch for stale information

**Example:**
> AI: "The current CEO of [Company] is X"
> Reality: X left two years ago

---

## Verification Methods

### Method 1: Spot-Check Verification

Sample specific claims for verification:

1. Identify 3-5 verifiable claims
2. Check each against authoritative source
3. If any fail, distrust entire output
4. Calculate trust discount based on failure rate

### Method 2: Falsification Testing

Try to prove the output wrong:

1. Ask: "What would make this conclusion false?"
2. Check if any of those conditions exist
3. Look for evidence that contradicts
4. If falsification attempts fail, increase confidence

### Method 3: Counter-Prompting

Ask AI to argue against itself:

1. Get initial output
2. Ask: "Now argue the opposite position"
3. Ask: "What's wrong with your first answer?"
4. Synthesize the views

### Method 4: Source Verification

For factual claims:

1. Ask AI for sources
2. Verify sources exist
3. Verify sources say what AI claims
4. Check source credibility

### Method 5: Consistency Testing

Check for internal contradictions:

1. Ask the same question different ways
2. Ask follow-up questions that would expose inconsistency
3. Compare answers across queries
4. Flag any contradictions for investigation

---

## Stopping Rules

### When to Stop Iterating

Iteration should end when:

1. **Success criteria met**: Output passes all verification gates
2. **Diminishing returns**: Additional iterations yield marginal improvement
3. **Resource limit**: Time/cost exceeds value of improvement
4. **Fundamental mismatch**: Task requires human judgment, not more AI

### How to Decide

```markdown
STOPPING CHECKLIST:
□ Output meets stated success criteria
□ All critical claims verified
□ No logical errors detected
□ Consistent with domain knowledge
□ Additional iteration won't improve key dimensions

If all checked → Stop
If any unchecked → Iterate or escalate to human
```

---

## Confidence Scoring

### Rate Every Output

| Level | Definition | Action |
|-------|------------|--------|
| **High** | Verified, consistent, logical | Use as-is |
| **Medium** | Partially verified, minor concerns | Use with caveats |
| **Low** | Unverified, concerns present | Verify before use |
| **Unreliable** | Failed verification | Do not use |

### Document Confidence

```markdown
OUTPUT CONFIDENCE ASSESSMENT:

Claim: [The AI's output]
Confidence: [High/Medium/Low/Unreliable]

Verification performed:
- [Check 1]: [Result]
- [Check 2]: [Result]
- [Check 3]: [Result]

Remaining concerns:
- [Concern 1]
- [Concern 2]

Recommendation: [Use as-is / Use with modifications / Reject]
```

---

## Practices

### Red-Team Prompts

After getting output, attack it:

```markdown
Now act as a critical reviewer:
- What errors might be in your previous response?
- What claims are weakest?
- What did you assume that might be wrong?
- How would an expert in this field critique this?
```

### Falsification Tests

```markdown
Your previous response concluded [X].

What evidence would prove this conclusion wrong?
Does any of that evidence exist?
How confident should I be in this conclusion?
```

### Confidence Scoring Prompts

```markdown
Rate your confidence in each part of your response:
- [Claim 1]: confidence and why
- [Claim 2]: confidence and why
- [Claim 3]: confidence and why

What would make you more or less confident?
```

---

## Assessment Criteria

**Layer 5 Complete When:**
- [ ] Applies verification gates to AI outputs by default
- [ ] Can detect and articulate specific error types
- [ ] Has documented rejected outputs with reasoning
- [ ] Uses stopping rules to end iteration appropriately
- [ ] Assigns confidence scores and documents basis

---

## Common Verification Failures

### Failure 1: Verification Theater

**Wrong:** "This looks right" (no actual verification)
**Right:** "I verified claim X against source Y, which confirms Z"

### Failure 2: Trusting AI's Self-Assessment

**Wrong:** Asking AI "are you sure?" and trusting "yes"
**Right:** External verification independent of AI

### Failure 3: Verification Fatigue

**Wrong:** Thorough verification on first output, none on subsequent
**Right:** Consistent verification protocol regardless of prior accuracy

### Failure 4: Unfalsifiable Acceptance

**Wrong:** Accepting because you can't prove it wrong
**Right:** Active falsification attempts before acceptance

---

## Related Skills

- [ai-system-literacy](../ai-system-literacy/SKILL.md) — Understanding why errors occur
- [ai-cognitive-readiness](../ai-cognitive-readiness/SKILL.md) — Skepticism as default stance
- [ai-fluency-antipatterns](../ai-fluency-antipatterns/SKILL.md) — Output Authority Bias

---

## Learn More

- [Verification Checklists](references/verification-checklists.md)
- [Error Pattern Examples](references/error-examples.md)
