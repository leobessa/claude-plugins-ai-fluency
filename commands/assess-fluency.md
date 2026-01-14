---
description: "Conduct a comprehensive AI fluency assessment using the 4D Framework and certification criteria"
argument-hint: "[self|team|workflow:{name}]"
allowed-tools: ["Read", "Write", "Glob", "Grep", "AskUserQuestion"]
---

# AI Fluency Assessment Command

Conduct a structured assessment of AI fluency proficiency. This command guides through a comprehensive evaluation using the 4D Framework dimensions and produces a certification-level recommendation.

## Assessment Types

Based on the argument provided:

- **`self`** (default): Personal AI fluency self-assessment
- **`team`**: Team-level AI fluency assessment
- **`workflow:{name}`**: Assessment of a specific AI workflow's fluency characteristics

## Assessment Process

### For Self-Assessment

1. **Initialize Assessment**
   - Record date and context
   - Set up assessment workspace

2. **Dimension Evaluation**

   For each of the four dimensions, evaluate current proficiency:

   **Delegation Assessment:**
   - Ask about task selection practices
   - Probe understanding of AI capabilities and limitations
   - Evaluate decomposition skills
   - Rate: E(1) through A(5)

   **Description Assessment:**
   - Ask about prompt structure practices
   - Request examples of prompts used
   - Evaluate template development
   - Rate: E(1) through A(5)

   **Discernment Assessment:**
   - Ask about verification practices
   - Probe error detection capabilities
   - Evaluate confidence calibration
   - Rate: E(1) through A(5)

   **Diligence Assessment:**
   - Ask about iteration practices
   - Probe learning capture methods
   - Evaluate improvement systems
   - Rate: E(1) through A(5)

3. **Evidence Collection**
   - Ask user to provide or point to evidence for each dimension
   - Document evidence quality and gaps

4. **Certification Level Determination**
   - Calculate composite score
   - Determine certification level (E through A)
   - Identify primary gaps

5. **Generate Assessment Report**

   Use this format:
   ```markdown
   # AI Fluency Assessment Report

   Date: [Date]
   Assessment Type: Self-Assessment

   ## Dimension Scores

   | Dimension | Score | Level | Evidence |
   |-----------|-------|-------|----------|
   | Delegation | X/5 | [Level] | [Brief] |
   | Description | X/5 | [Level] | [Brief] |
   | Discernment | X/5 | [Level] | [Brief] |
   | Diligence | X/5 | [Level] | [Brief] |

   **Total Score:** XX/20

   ## Certification Level: [E/D/C/B/A]

   ### Justification
   [Why this level is appropriate based on evidence]

   ## Strengths
   1. [Strength 1]
   2. [Strength 2]

   ## Development Areas
   1. [Gap 1] - [Recommended action]
   2. [Gap 2] - [Recommended action]

   ## Recommended Next Steps
   1. [Priority action for improvement]
   2. [Secondary action]
   3. [Tertiary action]

   ## Resources
   - [Relevant skill from ai-fluency plugin]
   - [Relevant skill from ai-fluency plugin]
   ```

### For Team Assessment

1. **Gather Team Information**
   - Number of team members
   - Roles and AI usage patterns
   - Current AI practices and tools

2. **Aggregate Assessment**
   - Either assess each member individually and aggregate
   - Or assess team-level practices directly

3. **Team Distribution Analysis**
   - Calculate distribution across certification levels
   - Identify team-wide gaps
   - Determine team composite level

4. **Generate Team Report**

   Use this format:
   ```markdown
   # Team AI Fluency Assessment

   Team: [Name]
   Date: [Date]
   Members Assessed: [N]

   ## Individual Distribution

   | Level | Count | Percentage |
   |-------|-------|------------|
   | A | X | X% |
   | B | X | X% |
   | C | X | X% |
   | D | X | X% |
   | E | X | X% |

   ## Team Composite Level: [Level]

   ## Dimension Analysis

   | Dimension | Team Avg | Strongest | Weakest |
   |-----------|----------|-----------|---------|
   | Delegation | X.X | [Name] | [Name] |
   | Description | X.X | [Name] | [Name] |
   | Discernment | X.X | [Name] | [Name] |
   | Diligence | X.X | [Name] | [Name] |

   ## Team Gaps
   1. [Gap 1]
   2. [Gap 2]

   ## Recommendations
   1. [Team development action]
   2. [Training recommendation]
   ```

### For Workflow Assessment

1. **Identify Workflow**
   - Get workflow name and description
   - Understand workflow purpose and steps

2. **Assess Workflow Fluency**

   For each workflow component:
   - **Delegation**: Is the task appropriate for AI?
   - **Description**: Are prompts well-structured?
   - **Discernment**: Is verification adequate?
   - **Diligence**: Does the workflow improve?

3. **Generate Workflow Report**

   Use this format:
   ```markdown
   # Workflow AI Fluency Assessment

   Workflow: [Name]
   Date: [Date]

   ## Workflow Overview
   [Brief description]

   ## Component Analysis

   | Component | Delegation | Description | Discernment | Diligence |
   |-----------|------------|-------------|-------------|-----------|
   | [Step 1] | [Rating] | [Rating] | [Rating] | [Rating] |
   | [Step 2] | [Rating] | [Rating] | [Rating] | [Rating] |

   ## Overall Workflow Score: [X/20]

   ## Weakest Dimension: [Dimension]

   ## Recommendations
   1. [Improvement for workflow]
   2. [Improvement for workflow]
   ```

## Interaction Style

- Use AskUserQuestion tool to gather information at each stage
- Be conversational but structured
- Provide concrete examples of what each level looks like
- Be honest about gaps while remaining constructive
- Reference specific ai-fluency skills for development

## Quality Standards

- Assessment should take 10-15 minutes for self, longer for team
- Every rating must be justified with evidence or observation
- Recommendations must be specific and actionable
- Output report should be saved to a file for reference

## Tips

- Start with the dimension the user feels strongest in to build confidence
- Use the anti-patterns skill to identify specific areas of weakness
- Reference the certification skill for detailed level criteria
- For team assessments, consider using anonymous aggregation if appropriate
