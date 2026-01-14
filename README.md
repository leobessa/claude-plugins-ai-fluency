# AI Fluency Plugin

AI Fluency skills for reliably thinking, deciding, and acting with AI systems while retaining human judgment, accountability, and strategic clarity.

## Overview

AI Fluency is the ability to work effectively with AI systems while maintaining epistemic control. This plugin provides a comprehensive curriculum organized into 9 layers, plus supporting frameworks for anti-patterns, certification, and collaboration modes.

**Core Philosophy:** AI fluency is not about knowing AI tricks—it's about maintaining human judgment while leveraging AI capabilities.

## The 9-Layer Curriculum

| Layer | Skill | Focus |
|-------|-------|-------|
| **Layer 0** | ai-cognitive-readiness | Pre-fluency cognitive habits and mindset |
| **Layer 1** | ai-system-literacy | Understanding AI capabilities and limitations |
| **Layer 2** | ai-problem-framing | Structuring problems for AI delegation |
| **Layer 3** | ai-instruction-design | Crafting effective prompts and specifications |
| **Layer 4** | ai-reasoning-scaffolds | Structuring AI's reasoning process |
| **Layer 5** | ai-evaluation-verification | Verifying and validating AI outputs |
| **Layer 6** | ai-workflow-integration | Building repeatable AI-assisted workflows |
| **Layer 7** | ai-system-governance | Scaling fluency through organizational systems |
| **Layer 8** | ai-strategic-fluency | Using AI for strategic advantage |

## Supporting Skills

| Skill | Purpose |
|-------|---------|
| **ai-fluency-antipatterns** | Recognize and avoid 15 common AI fluency mistakes |
| **ai-4d-framework** | Apply Anthropic's 4D Framework (Delegation, Description, Discernment, Diligence) |
| **ai-fluency-certification** | Assess proficiency using 5-level certification (A through E) |
| **ai-collaboration-modes** | Choose between Automation, Augmentation, and Agency modes |

## Commands

### /ai-fluency:assess-fluency

Conduct a comprehensive AI fluency assessment.

```
/ai-fluency:assess-fluency self          # Personal self-assessment
/ai-fluency:assess-fluency team          # Team-level assessment
/ai-fluency:assess-fluency workflow:X    # Assess specific workflow
```

Produces a detailed report with:
- Dimension scores (Delegation, Description, Discernment, Diligence)
- Certification level recommendation (E through A)
- Strengths and development areas
- Recommended next steps

### /ai-fluency:diagnose-antipattern

Diagnose AI fluency anti-patterns in problematic interactions.

```
/ai-fluency:diagnose-antipattern interaction   # Analyze specific interaction
/ai-fluency:diagnose-antipattern workflow      # Analyze workflow
/ai-fluency:diagnose-antipattern conversation  # Analyze current conversation
```

Produces a diagnosis with:
- Primary and secondary anti-patterns detected
- Evidence and impact analysis
- Specific remediation actions

## Agents

### fluency-coach

Proactive coaching agent that observes AI interactions and provides constructive feedback. Triggers after significant AI-assisted work to reinforce good practices and guide improvements.

### antipattern-detector

Monitoring agent that detects problematic AI usage patterns early. Provides brief alerts when anti-patterns are detected, with quick-fix suggestions.

## Skills Reference

### Layer 0: AI Cognitive Readiness

**Trigger:** Questions about AI mindset, when to use AI, automation bias

Develops pre-fluency cognitive habits:
- Recognize when NOT to use AI
- Separate thinking from generation
- Resist automation bias and output authority
- Maintain epistemic humility

### Layer 1: AI System Literacy

**Trigger:** Questions about how AI works, why AI hallucinates, AI limitations

Builds accurate mental models:
- Context windows and attention
- Probabilistic generation
- Hallucination mechanisms
- Failure mode prediction

### Layer 2: AI Problem Framing

**Trigger:** Structuring tasks for AI, decomposition, delegation decisions

Transforms fuzzy intent into structured problems:
- Explicit objectives
- Clear constraints
- Success criteria
- Human vs AI responsibility

### Layer 3: AI Instruction Design

**Trigger:** Prompt engineering, prompt structure, consistent results

Controls output through specifications:
- RSFDA framework (Role, Scope, Format, Decision rules, Abstraction)
- Prompt as specification, not request
- Format enforcement
- Decision rule codification

### Layer 4: AI Reasoning Scaffolds

**Trigger:** Complex analysis, structured thinking, reasoning quality

Structures AI's reasoning process:
- Checklists
- Reasoning trees
- Critique loops
- Stepwise reasoning
- Multi-perspective analysis

### Layer 5: AI Evaluation & Verification

**Trigger:** Verifying AI output, catching errors, hallucination detection

Maintains epistemic control:
- Three validation gates (Logic, First Principles, Reality)
- Error detection patterns
- Verification methods
- Confidence scoring

### Layer 6: AI Workflow Integration

**Trigger:** Repeatable AI processes, systematic AI use, workflow design

Converts fluency into throughput:
- Workflow components
- Quality gates
- Iteration and improvement
- Metrics and monitoring

### Layer 7: AI System Governance

**Trigger:** AI policies, standards, audit, organizational AI use

Scales fluency through systems:
- Standards and guardrails
- Audit trails
- Policies and compliance
- Team/org governance

### Layer 8: AI Strategic Fluency

**Trigger:** AI strategy, competitive advantage, AI business impact

AI as strategic lever:
- Constraint identification
- Competitive positioning
- Value chain transformation
- Business model innovation

### AI Fluency Anti-Patterns

**Trigger:** AI mistakes, what not to do, problematic patterns

Catalogs 15 anti-patterns across 5 categories:
- Cognitive (Automation Complacency, Output Authority Bias, Sunk Cost Prompting)
- Process (Vague Intent, Prompt Magic, Iteration Without Learning, Context Dumping)
- Verification (Verification Theater, First-Draft Acceptance, Overconfident Calibration)
- Structural (Single-Shot Complex, No Scaffold, Role-Free Prompting)
- Organizational (Inconsistent Application, Learning Plateau)

### AI 4D Framework

**Trigger:** 4D framework, AI assessment framework, delegation framework

Anthropic's model for AI delegation:
- **Delegation:** What tasks to give AI
- **Description:** How to specify what you want
- **Discernment:** How to evaluate AI output
- **Diligence:** How to systematically improve

### AI Fluency Certification

**Trigger:** AI fluency levels, certification, assessment criteria

5-level certification system:
- **Level E:** Emerging - Beginning AI use
- **Level D:** Developing - Building practices
- **Level C:** Competent - Systematic practices
- **Level B:** Proficient - Teaching and scaling
- **Level A:** Advanced - Strategic leadership

### AI Collaboration Modes

**Trigger:** Automation vs augmentation, human-AI collaboration, AI modes

Three collaboration patterns:
- **Automation:** AI acts independently
- **Augmentation:** AI assists human work
- **Agency:** AI takes delegated responsibility

## Installation

Add as a marketplace in Claude Code:

```bash
# Add the marketplace
/plugins add leobessa/claude-plugins-ai-fluency

# Enable the ai-fluency plugin
/plugins
# Then toggle ai-fluency to enabled
```

Or clone and test locally:

```bash
git clone https://github.com/leobessa/claude-plugins-ai-fluency.git
cc --plugin-dir ./claude-plugins-ai-fluency
```

## Usage

Skills are automatically invoked when relevant questions arise. For example:

- "How should I structure this prompt?" → ai-instruction-design
- "Why does AI keep making mistakes?" → ai-system-literacy, ai-fluency-antipatterns
- "How do I verify this AI output?" → ai-evaluation-verification
- "What level is my AI fluency?" → ai-fluency-certification

Commands are invoked explicitly:
```
/ai-fluency:assess-fluency self
/ai-fluency:diagnose-antipattern interaction
```

## Author

Leo Bessa (leobessa@gmail.com)

## License

MIT
