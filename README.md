# The 11 Levels of Agentic Engineering

### A roadmap from tab-complete to controlling the physical world

<p align="center">
  <strong>Levels 1–8</strong> by <a href="https://www.bassimeledath.com/blog/levels-of-agentic-engineering">Bassim Eledath</a> (March 2026)<br>
  <strong>Levels 9–11</strong> extended by <a href="https://centaurion.me">Malik Palamar</a> — Centaurion.me / BuilderBee
</p>

---

## Why This Exists

AI's coding ability is outpacing our ability to wield it. When one team ships a product in 10 days and another can't move past a broken POC using the same models, the difference isn't the AI — it's the **practice gap** between capability and execution.

That gap closes in levels. Bassim Eledath mapped the first eight for software engineering teams. This repository extends the framework with three additional levels that push agentic engineering **beyond code** — into autonomous deployment, simulation-first development, and the physical world.

**This repo gives you:**

- A **self-assessment questionnaire** to find where you and your team sit today
- **Curated resources** for every level — articles, tools, repos, tutorials
- **Starter code and templates** to begin leveling up immediately
- A **roadmap** that works for solo developers, small teams, and organizations

---

## The Full Ladder

```
BEYOND CODE (Palamar Extension)
  Level 11  Physical-Digital Bridge
  Level 10  Simulation-First Development
  Level  9  Autonomous Deployment Pipelines

THE FRONTIER (Eledath Levels 6-8)
  Level  8  Autonomous Agent Teams
  Level  7  Background Agents
  Level  6  Harness Engineering & Feedback Loops

THE FOUNDATION (Eledath Levels 1-5)
  Level  5  MCP and Skills
  Level  4  Compounding Engineering
  Level  3  Context Engineering
  Level  2  Agent IDE
  Level  1  Tab Complete
```

---

## The Levels in Detail

### Foundation Tier (Levels 1-5)

These levels build the muscle memory. Skip them and everything above collapses.

**Level 1: Tab Complete** — Copilot-era autocomplete. You type, AI suggests the next line.

**Level 2: Agent IDE** — AI-focused IDEs (Cursor, Windsurf, Kiro) connect chat to your codebase for multi-file edits.

**Level 3: Context Engineering** — Curating what the model sees. Every token fights for its place. See [examples/level-03-context/](examples/level-03-context/)

**Level 4: Compounding Engineering** — Plan, delegate, assess, codify. Each session makes the next one better. See [examples/level-04-compounding/](examples/level-04-compounding/)

**Level 5: MCP and Skills** — The agent can act, not just think. MCPs, skills, and CLI tools give it access to databases, APIs, CI, Slack, browsers. See [examples/level-05-mcp/](examples/level-05-mcp/)

> **Critical Checkpoint:** Levels 3 through 5 are the building blocks for everything that follows. If your context is noisy, your prompts are misspecified, or your tools are poorly described, levels 6 through 11 just amplify the mess.

### Frontier Tier (Levels 6-8)

**Level 6: Harness Engineering** — Building the environment and feedback loops so agents self-correct without you. Key concept: **backpressure**. See [examples/level-06-harness/](examples/level-06-harness/)

**Level 7: Background Agents** — Work happens without you in the chair. Key pattern: different models for different jobs. Decouple implementer from reviewer. See [examples/level-07-background/](examples/level-07-background/)

**Level 8: Autonomous Agent Teams** — Agents coordinate with each other directly. Active frontier. Nobody has mastered this yet.

### Beyond Code (Levels 9-11) — The Palamar Extension

**Level 9: Autonomous Deployment Pipelines** — Intent to production without human assembly. Phone-first. See [examples/level-09-deployment/](examples/level-09-deployment/)

**Level 10: Simulation-First Development** — Replace "ship then learn" with "simulate then build." See [examples/level-10-simulation/](examples/level-10-simulation/)

**Level 11: Physical-Digital Bridge** — Agent actions have physical consequences. The IDE becomes a control surface for reality. See [examples/level-11-physical/](examples/level-11-physical/)

---

## Assessment

Take the self-assessment: [assessment/QUESTIONNAIRE.md](assessment/QUESTIONNAIRE.md)

Visualize your team: [assessment/team-radar.html](assessment/team-radar.html) (open in browser)

## Resources

- [resources/TOOLS.md](resources/TOOLS.md) — Tools, platforms, and open-source projects per level
- [resources/READING.md](resources/READING.md) — Articles, papers, and talks per level
- [resources/ORCHESTRATORS.md](resources/ORCHESTRATORS.md) — Comparison of agent orchestration platforms

## The Multiplayer Effect

Your output depends on your teammates' level more than you'd think. A Level 7 developer blocked by a Level 2 reviewer operates at Level 2. The team levels up together or not at all.

## Contributing

This is a living framework. If you're operating at a level not described here, or have resources that belong in this repo, open a PR or an issue.

## License

MIT — See [LICENSE](LICENSE)

## Attribution

Levels 1-8: [Bassim Eledath](https://www.bassimeledath.com/blog/levels-of-agentic-engineering) | Levels 9-11: [Malik Palamar](https://centaurion.me) — Centaurion.me / BuilderBee
