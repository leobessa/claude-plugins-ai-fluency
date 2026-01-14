# AI Fluency

Most AI interactions feel like gambling. You prompt, hope, and check the output endlessly. This plugin provides systematic patterns for getting reliable results.

## Quick Start

```bash
# In Claude Code
/plugins add leobessa/claude-plugins-ai-fluency
```

Then enable the `ai-fluency` plugin in `/plugins`.

Try it: Ask "How should I structure this prompt?" and the relevant skill loads automatically.

## What This Does

13 skills that help you work with AI systematically. They load automatically when relevant, or you can invoke commands directly.

| Type | Count | Purpose |
|------|-------|---------|
| Skills | 13 | Automatic guidance based on context |
| Commands | 2 | Explicit assessment and diagnosis |
| Agents | 2 | Proactive coaching and pattern detection |

## When to Use This

- You waste time re-prompting to get usable output
- You can't tell when AI output is trustworthy
- You want repeatable processes, not one-off luck
- You're teaching others how to use AI effectively

## When NOT to Use This

- One-off creative brainstorming (just prompt directly)
- Tasks where AI errors don't matter
- You prefer learning by trial and error

## Skills Overview

Organized from foundational to strategic:

| Layer | Skill | What It Does |
|-------|-------|--------------|
| 0 | ai-cognitive-readiness | Know when NOT to use AI |
| 1 | ai-system-literacy | Understand why AI fails |
| 2 | ai-problem-framing | Structure problems before prompting |
| 3 | ai-instruction-design | Write prompts that work consistently |
| 4 | ai-reasoning-scaffolds | Guide AI's thinking process |
| 5 | ai-evaluation-verification | Verify output systematically |
| 6 | ai-workflow-integration | Build repeatable AI processes |
| 7 | ai-system-governance | Scale AI use across teams |
| 8 | ai-strategic-fluency | Use AI for competitive advantage |

Plus 4 supporting skills: anti-patterns, 4D framework, certification levels, collaboration modes.

See [SKILLS-REFERENCE.md](SKILLS-REFERENCE.md) for detailed descriptions.

## Commands

### /ai-fluency:assess-fluency

Evaluate your AI fluency across four dimensions.

```
/ai-fluency:assess-fluency self      # Personal assessment
/ai-fluency:assess-fluency team      # Team assessment
```

Returns scores, certification level (E through A), and specific improvements.

### /ai-fluency:diagnose-antipattern

Find problematic patterns in AI interactions.

```
/ai-fluency:diagnose-antipattern interaction    # Analyze specific interaction
/ai-fluency:diagnose-antipattern conversation   # Analyze current conversation
```

Returns detected anti-patterns with evidence and fixes.

## Agents

**fluency-coach** — Observes your AI work and suggests improvements. Triggers after significant tasks.

**antipattern-detector** — Alerts you early when problematic patterns emerge. Lightweight, minimal disruption.

## Author

Leo Bessa (leobessa@gmail.com)

## License

MIT
