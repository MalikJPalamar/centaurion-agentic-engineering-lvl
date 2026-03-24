# The 11 Levels of Agentic Engineering

### A roadmap from tab-complete to controlling the physical world

<p align="center">
  <strong>Levels 1-8</strong> by <a href="https://www.bassimeledath.com/blog/levels-of-agentic-engineering">Bassim Eledath</a> (March 2026)<br>
  <strong>Levels 9-11</strong> extended by <a href="https://centaurion.me">Malik Palamar</a> - Centaurion.me / BuilderBee
</p>

---

## Why This Exists

AI's coding ability is outpacing our ability to wield it. When one team ships a product in 10 days and another can't move past a broken POC using the same models, the difference isn't the AI - it's the **practice gap** between capability and execution.

That gap closes in levels. Bassim Eledath mapped the first eight for software engineering teams. This repository extends the framework with three additional levels that push agentic engineering **beyond code** - into autonomous deployment, simulation-first development, and the physical world.

**This repo gives you:**

- A **self-assessment questionnaire** to find where you and your team sit today
- **Curated resources** for every level - articles, tools, repos, tutorials
- **Starter code and templates** to begin leveling up immediately
- A **roadmap** that works for solo developers, small teams, and organizations

---

## The Full Ladder

```
BEYOND CODE (Palamar Extension)

  Level 11  Physical-Digital Bridge
  Level 10  Simulation-First Development
  Level  9  Autonomous Deployment Pipelines

  - - - - - - - - - - - - - - - - - - - - -

THE FRONTIER (Eledath Levels 6-8)

  Level  8  Autonomous Agent Teams
  Level  7  Background Agents
  Level  6  Harness Engineering & Feedback Loops

  - - - - - - - - - - - - - - - - - - - - -

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

| Level | Name | Core Shift | Key Metric |
|-------|------|-----------|------------|
| 1 | Tab Complete | AI suggests as you type | Keystrokes saved |
| 2 | Agent IDE | Chat connected to codebase | Multi-file edits per session |
| 3 | Context Engineering | Information density per token | Signal-to-noise ratio |
| 4 | Compounding Engineering | Each session improves the next | Lessons codified per week |
| 5 | MCP and Skills | Agent can act, not just think | Tools connected and shared |

See [`examples/level-03-context/`](examples/level-03-context/) through [`examples/level-05-mcp/`](examples/level-05-mcp/) for starter templates.

### Critical Checkpoint

**Levels 3 through 5 are the building blocks for everything that follows.** If your context is noisy, your prompts are misspecified, or your tools are poorly described, levels 6 through 11 just amplify the mess. Do not skip ahead.

### Frontier Tier (Levels 6-8)

| Level | Name | Core Shift | Key Metric |
|-------|------|-----------|------------|
| 6 | Harness Engineering | Agent self-corrects via feedback loops | Human interventions per task |
| 7 | Background Agents | Work happens without you in the chair | Tasks completed while sleeping |
| 8 | Autonomous Agent Teams | Agents coordinate with each other | PRs shipped per agent-day |

Key concepts: **backpressure** (automated feedback that lets agents self-correct), **constraints over instructions** (boundaries beat checklists), **decouple implementer from reviewer** (same model grading its own work is biased).

See [`examples/level-06-harness/`](examples/level-06-harness/) and [`examples/level-07-background/`](examples/level-07-background/) for patterns.

### Beyond Code (Levels 9-11) - The Palamar Extension

| Level | Name | Core Shift | Key Metric |
|-------|------|-----------|------------|
| **9** | **Autonomous Deployment** | Intent to production without human assembly | Minutes from prompt to live URL |
| **10** | **Simulation-First Development** | Learn before you build, not after you ship | Hypotheses eliminated before first commit |
| **11** | **Physical-Digital Bridge** | Agent actions have physical consequences | Atoms moved per agent instruction |

**Level 9** closes the last mile: from agent-written code to live production URL, triggered from a phone. The pipeline: Generate, Commit, CI Gate, AI Review, Deploy, Verify, Report.

**Level 10** inverts the Lean Startup loop. Instead of build-ship-learn, it is simulate-learn-build. Synthetic user panels from real CRM data test product concepts before any code is written. Harvard Business Review reports these tools are expected to disrupt the $140 billion market research industry in 2026.

**Level 11** crosses from bits to atoms. Agents control lights, trigger 3D prints, read physical sensors. The safety profile changes fundamentally: physical kill switches that cannot be software-bypassed.

See [`examples/level-09-deployment/`](examples/level-09-deployment/), [`examples/level-10-simulation/`](examples/level-10-simulation/), and [`examples/level-11-physical/`](examples/level-11-physical/) for starter code.

---

## Assessment

**Don't know where you are?** Take the self-assessment:

- [`assessment/QUESTIONNAIRE.md`](assessment/QUESTIONNAIRE.md) - 56-point diagnostic for individuals and teams
- [`assessment/team-radar.html`](assessment/team-radar.html) - Interactive radar chart visualization (open in browser)

---

## The Multiplayer Effect

Your output depends on your teammates' level more than you think. If you are at Level 7 raising PRs with background agents while you sleep, but your colleague is at Level 2 manually reviewing every PR, their bottleneck becomes your bottleneck. It is in your best interest to pull your team up.

---

## Resources

- [`resources/TOOLS.md`](resources/TOOLS.md) - Tools, platforms, and open-source projects per level
- [`resources/READING.md`](resources/READING.md) - Articles, papers, and talks per level
- [`resources/ORCHESTRATORS.md`](resources/ORCHESTRATORS.md) - Comparison of agent orchestration platforms

---

## Full Framework Deep Dive

For the complete detailed write-up of all 11 levels with examples and references, see [`docs/FRAMEWORK.md`](docs/FRAMEWORK.md).

---

## Contributing

This is a living framework. If you are operating at a level not described here, or have resources that belong in this repo, open a PR or an issue.

## License

MIT - See [LICENSE](LICENSE)

## Attribution

The foundation of this framework (Levels 1-8) is the work of [Bassim Eledath](https://www.bassimeledath.com/blog/levels-of-agentic-engineering). The extensions (Levels 9-11) are by [Malik Palamar](https://centaurion.me) through the Centaurion human-AI augmentation framework and BuilderBee advisory practice.
