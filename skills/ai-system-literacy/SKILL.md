---
name: ai-system-literacy
description: "Build accurate mental models of AI behavior: understand context windows, probabilistic generation, hallucination causes, and predict failure modes before they occur."
version: "1.0.0"
---

# Overview

**AI System Literacy** is Layer 1 of AI fluency—building accurate mental models of how AI systems actually work. This isn't about knowing model architectures but understanding behavior patterns that affect your work.

**Core Principle:** Predict failure modes *before* they occur.

**Fluency Signal:** Can anticipate likely errors before running a prompt.

---

## When to Use This Skill

- When AI output seems wrong but you're not sure why
- When designing prompts for complex tasks
- When debugging unexpected AI behavior
- When explaining AI capabilities to others
- When deciding what tasks to delegate

---

## Core Concepts

### 1. Reasoning vs Pattern Completion

**Critical distinction:** AI does not reason. It predicts likely next tokens based on training patterns.

**Implications:**
- Novel problems may get plausible-sounding but wrong answers
- Step-by-step reasoning improves output (gives patterns to follow)
- AI can "show its work" without actually doing the work
- Logical errors persist if training data contained them

**Test:** Ask AI to solve a problem it couldn't have seen. Check the reasoning, not just the answer.

### 2. Context Windows

**What it is:** The maximum text AI can "see" at once (e.g., 100K-200K tokens).

**Implications:**
- Information at context edges may be deprioritized
- Very long contexts dilute attention on specifics
- Conversation history competes with instructions
- "Lost in the middle" effect: mid-context information forgotten

**Best practices:**
- Put critical information at the start
- Summarize context instead of dumping raw text
- Refresh important instructions in long conversations
- Structure context with clear sections

### 3. Probabilistic Generation

**What it is:** Each token is sampled from a probability distribution; output is non-deterministic.

**Implications:**
- Same prompt can produce different outputs
- "Temperature" controls randomness
- AI doesn't "know" what it will say next
- Confident tone doesn't indicate certainty

**Best practices:**
- Run important queries multiple times
- Lower temperature for factual tasks
- Higher temperature for creative/brainstorming tasks
- Don't assume consistency across runs

### 4. Hallucination Mechanisms

**Why AI hallucinates:**

| Cause | Description | Example |
|-------|-------------|---------|
| **Overgeneralization** | Applies patterns where they don't fit | Making up citations that "sound right" |
| **Confidence inheritance** | Training on confident text produces confident output | Stating false facts authoritatively |
| **Gap-filling** | Completes patterns even without information | Inventing plausible details |
| **Recency bias** | Overwights recent context | Contradicting earlier information |
| **Anchoring** | First framing persists even when wrong | Accepting user's false premise |

**High-risk scenarios:**
- Specific facts, numbers, dates, citations
- Niche topics with limited training data
- Questions that assume facts (leading questions)
- Requests for exhaustive lists

### 5. Model vs Tool Boundaries

**The model** = the AI's pattern-matching capability
**The tool** = the interface, context, instructions wrapped around it

**Implications:**
- Many "AI features" are tool-level prompts, not model capabilities
- Tool design dramatically affects output quality
- Same model behaves differently in different tools
- Failures may be tool-level, not model-level

---

## Failure Mode Prediction

### When to Expect Errors

| Situation | Likely Error Type |
|-----------|-------------------|
| Specific facts (dates, numbers) | Hallucination |
| Long-form reasoning | Logic gaps in middle |
| Multi-step tasks | Dropped steps |
| Ambiguous instructions | Assumption-filling |
| Requests for completeness | False exhaustiveness |
| Edge cases | Overgeneralization |
| Recent events | Training cutoff errors |
| Obscure topics | Confident fabrication |

### Prediction Practice

Before running a prompt, ask:
1. What type of knowledge does this require?
2. Is this in-distribution or novel?
3. What could AI plausibly get wrong?
4. How would I detect that error?

---

## Practices

### Prompt → Predict → Compare

1. Write a prompt
2. Before running, predict:
   - What will AI likely say?
   - What might it get wrong?
   - Where will it struggle?
3. Run the prompt
4. Compare prediction to reality
5. Update mental model

### Deliberate Ambiguity Testing

1. Write intentionally ambiguous prompts
2. Observe how AI resolves ambiguity
3. Note patterns in default assumptions
4. Use findings to write clearer prompts

### Hallucination Detection Drills

1. Ask about topics you're expert in
2. Include verifiable facts in context, then query them
3. Request citations and verify them
4. Ask the same question multiple ways

---

## Assessment Criteria

**Layer 1 Complete When:**
- [ ] Can explain why AI hallucinates (mechanisms, not just "it makes stuff up")
- [ ] Predicts likely error types before running prompts
- [ ] Understands context window implications for long tasks
- [ ] Distinguishes model capabilities from tool features
- [ ] Has documented correct predictions of AI failures

---

## Common Misconceptions

### "AI Understands What I Mean"

**Reality:** AI predicts likely completions. It doesn't "understand" intent—it follows patterns. Clarity in prompts isn't optional.

### "Longer Context = Better Results"

**Reality:** More context means more noise. AI attention is limited. Curated, structured context beats raw volume.

### "AI Will Say If It Doesn't Know"

**Reality:** Default behavior is confident completion. Uncertainty acknowledgment requires explicit prompting—and even then isn't reliable.

---

## Related Skills

- [ai-cognitive-readiness](../ai-cognitive-readiness/SKILL.md) — Foundation for this layer
- [ai-instruction-design](../ai-instruction-design/SKILL.md) — Applying literacy to prompt construction
- [ai-evaluation-verification](../ai-evaluation-verification/SKILL.md) — Verifying against known failure modes

---

## Learn More

- [Failure Mode Reference](references/failure-modes.md)
- [Context Window Optimization](references/context-optimization.md)
