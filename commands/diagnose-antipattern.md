---
description: "Diagnose AI fluency anti-patterns from a problematic AI interaction or workflow"
argument-hint: "[interaction|workflow|conversation]"
allowed-tools: ["Read", "Write", "Glob", "Grep", "AskUserQuestion"]
---

# AI Anti-Pattern Diagnosis Command

Diagnose which AI fluency anti-patterns are present in a problematic AI interaction, workflow, or the current conversation. This command systematically checks against all 15 anti-patterns and provides specific remediation guidance.

## Diagnosis Modes

Based on the argument provided:

- **`interaction`** (default): Analyze a specific AI interaction the user describes
- **`workflow`**: Analyze an AI workflow for structural anti-patterns
- **`conversation`**: Analyze the current conversation for anti-patterns

## Anti-Pattern Categories

The diagnosis covers five categories of anti-patterns:

### Cognitive Anti-Patterns
1. **Automation Complacency** - Reduced vigilance because "AI is handling it"
2. **Output Authority Bias** - Treating AI output as more authoritative than warranted
3. **Sunk Cost Prompting** - Continuing bad prompts due to effort invested

### Process Anti-Patterns
4. **Vague Intent Delegation** - Asking AI without specifying what you want
5. **Prompt Magic Thinking** - Believing in secret prompt formulas
6. **Iteration Without Learning** - Repeating without systematic change
7. **Context Dumping** - Overwhelming AI with uncurated context

### Verification Anti-Patterns
8. **Verification Theater** - Going through motions without verifying
9. **First-Draft Acceptance** - Using AI output without review
10. **Overconfident Calibration** - Being more confident than evidence supports

### Structural Anti-Patterns
11. **Single-Shot Complex Tasks** - Trying to do too much in one prompt
12. **No Scaffold for Reasoning** - Expecting good reasoning without structure
13. **Role-Free Prompting** - Not establishing perspective or expertise

### Organizational Anti-Patterns
14. **Inconsistent Application** - Applying practices inconsistently
15. **Learning Plateau** - Stopping improvement at "good enough"

## Diagnosis Process

### For Interaction Analysis

1. **Gather Context**
   - Ask user to describe the problematic interaction
   - What was the task?
   - What was the prompt (if available)?
   - What was the output?
   - What went wrong?

2. **Systematic Check**

   Work through each anti-pattern category:

   ```markdown
   COGNITIVE CHECK:
   □ Automation Complacency - Were you less vigilant than usual?
   □ Output Authority Bias - Did you accept output without questioning?
   □ Sunk Cost Prompting - Did you keep iterating on a failing approach?

   PROCESS CHECK:
   □ Vague Intent - Was the request clear and specific?
   □ Prompt Magic - Were you hoping for a magic formula?
   □ Iteration Without Learning - Did iterations have specific hypotheses?
   □ Context Dumping - Did you provide curated or raw context?

   VERIFICATION CHECK:
   □ Verification Theater - Did you actually verify or just skim?
   □ First-Draft Acceptance - Did you use the first output directly?
   □ Overconfident Calibration - Were you overconfident about accuracy?

   STRUCTURAL CHECK:
   □ Single-Shot Complex - Was the task too complex for one prompt?
   □ No Scaffold - Did you provide reasoning structure?
   □ Role-Free - Did you establish a role/perspective?
   ```

3. **Identify Primary Anti-Patterns**
   - Rank anti-patterns by likelihood and impact
   - Focus on the 2-3 most significant

4. **Generate Diagnosis Report**

   Use this format:
   ```markdown
   # AI Anti-Pattern Diagnosis

   Date: [Date]
   Analysis Type: Interaction

   ## Interaction Summary
   [Brief description of what went wrong]

   ## Anti-Patterns Detected

   ### Primary: [Anti-pattern name]
   **Category:** [Category]
   **Evidence:** [What indicates this pattern]
   **Impact:** [How it affected the outcome]
   **Remediation:**
   - [Specific action 1]
   - [Specific action 2]

   ### Secondary: [Anti-pattern name]
   **Category:** [Category]
   **Evidence:** [What indicates this pattern]
   **Impact:** [How it affected the outcome]
   **Remediation:**
   - [Specific action 1]

   ## Root Cause Analysis
   [Deeper analysis of why these patterns occurred]

   ## Recommended Actions
   1. **Immediate:** [Fix for current problem]
   2. **Short-term:** [Habit to develop]
   3. **Long-term:** [Systematic change]

   ## Related Skills
   - [ai-fluency skill that addresses this]
   - [ai-fluency skill that addresses this]
   ```

### For Workflow Analysis

1. **Understand Workflow**
   - Get workflow description
   - Identify AI touchpoints
   - Understand current performance

2. **Check Each Stage**
   - For each workflow stage, check for applicable anti-patterns
   - Pay special attention to:
     - Verification Theater (quality gates)
     - Inconsistent Application (process adherence)
     - Learning Plateau (improvement mechanisms)

3. **Generate Workflow Diagnosis**

   ```markdown
   # Workflow Anti-Pattern Analysis

   Workflow: [Name]

   ## Stage Analysis

   | Stage | Anti-Patterns | Severity | Fix |
   |-------|---------------|----------|-----|
   | [Stage 1] | [Patterns] | [H/M/L] | [Brief fix] |
   | [Stage 2] | [Patterns] | [H/M/L] | [Brief fix] |

   ## Systemic Issues
   [Patterns that appear across multiple stages]

   ## Priority Fixes
   1. [Highest impact fix]
   2. [Second priority]
   ```

### For Conversation Analysis

1. **Review Conversation**
   - Read through the current conversation
   - Identify AI interactions within it
   - Note patterns in prompting and response handling

2. **Self-Diagnosis**
   - Check user's prompting patterns
   - Check response handling patterns
   - Check iteration patterns

3. **Generate Conversation Diagnosis**

   ```markdown
   # Conversation Anti-Pattern Analysis

   ## Patterns Observed

   In this conversation, I observed:

   1. **[Pattern]** at [point in conversation]
      - Evidence: [What showed this pattern]
      - Impact: [How it affected outcomes]

   2. **[Pattern]** at [point in conversation]
      - Evidence: [What showed this pattern]
      - Impact: [How it affected outcomes]

   ## Recommendations for Remainder of Conversation
   - [Specific adjustment]
   - [Specific adjustment]
   ```

## Interaction Style

- Be diagnostic, not judgmental
- Focus on patterns, not personal criticism
- Provide specific, actionable remediation
- Use examples from the anti-patterns skill
- Reference relevant ai-fluency skills for deeper learning

## Quality Standards

- Every detected pattern must have evidence
- Severity ratings must be justified
- Remediation must be specific and actionable
- Link to appropriate ai-fluency skills for each pattern

## Tips

- Start with the most obvious patterns before subtle ones
- Check for pattern combinations (patterns often occur together)
- Distinguish root cause patterns from symptom patterns
- Use the 4D Framework to organize findings (which dimension is weakest?)
- Be constructive - the goal is improvement, not criticism
