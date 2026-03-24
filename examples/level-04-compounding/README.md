# Level 4: Compounding Engineering

## The Loop

```
Plan → Delegate → Assess → Codify
                              ↓
                    Update CLAUDE.md / docs/
                              ↓
                    Next session is better
```

## The Codify Journal

After every significant agent interaction, log:

```markdown
# Codify Log

## 2026-03-23 — [Task description]
**What worked:** [What the agent got right]
**What broke:** [What the agent got wrong]
**Root cause:** [Missing context? Wrong tool? Ambiguous instruction?]
**Codified:** [What you added to CLAUDE.md or docs/ to prevent recurrence]
```

## Anti-Patterns

- **Codify everything** — Too many rules is as bad as none.
- **Codify the symptom, not the cause** — "Don't use lodash" is a symptom. "Prefer native JS methods" is a cause.
- **Never prune** — Rules that no longer apply create noise. Review monthly.

## Level Up Checklist

- [ ] You have a codify log that you update after agent sessions
- [ ] Your CLAUDE.md has been refined at least 5 times from real lessons
- [ ] You can point to a specific codified rule that prevented a repeat mistake
- [ ] You've pruned at least one rule that became stale
