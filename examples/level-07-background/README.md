# Level 7: Background Agents

## The Principle
Work happens without you in the chair. You assign, walk away, come back to results.

## Key Patterns
1. **Different models for different jobs.** Opus for implementation, Gemini for research, Codex for review.
2. **Decouple implementer from reviewer.** Same model grading its own work is biased.
3. **CI-triggered agents.** Docs bot on merge. Security scanner on PR. Dependency updater on schedule.

## Starter: Agent Orchestrator Config
```yaml
port: 3000
defaults:
  runtime: tmux
  agent: claude-code
  workspace: worktree
projects:
  my-app:
    repo: owner/my-app
    reactions:
      ci-failed:
        auto: true
        action: send-to-agent
        retries: 2
      changes-requested:
        auto: true
        action: send-to-agent
```

## Level Up Checklist
- [ ] You run agent tasks asynchronously
- [ ] You use multiple agent instances in parallel
- [ ] You use different models for different purposes
- [ ] At least one agent is triggered by CI/CD automatically
