# Agentic Engineering Self-Assessment

## How to Use
Answer each question based on your **current, consistent practice** - not what you have tried once. For teams, have each member complete independently, then compare. Your level is the **highest level where you answer Yes to most questions** AND all levels below are solid.

---

## Section 1: Foundation (Levels 1-5)

### Level 1 - Tab Complete
- [ ] I use AI-powered autocomplete when writing code
- [ ] I can recognize when autocomplete suggestions are correct vs wrong
- [ ] I feel more productive with autocomplete than without it

**Score: ___ / 3**

### Level 2 - Agent IDE
- [ ] I use an AI-connected IDE or chat agent (Cursor, Claude Code, Kiro, etc.)
- [ ] I describe changes in natural language and the agent edits multiple files
- [ ] I use plan mode to outline work before the agent executes
- [ ] I know how to provide context by mentioning files or project references

**Score: ___ / 4**

### Level 3 - Context Engineering
- [ ] I maintain a CLAUDE.md, .cursorrules, or equivalent rules file
- [ ] I have consciously edited those rules to improve agent output quality
- [ ] I think about what context the agent can see before blaming its intelligence
- [ ] I am aware of how tool schemas and conversation history consume the context window
- [ ] I have experienced the difference between noisy context and clean context

**Score: ___ / 5**

### Level 4 - Compounding Engineering
- [ ] After an agent makes a mistake, I update my rules or docs to prevent recurrence
- [ ] I maintain project documentation that agents can discover and use
- [ ] I follow a plan, delegate, assess, codify loop
- [ ] My rules files have grown and been refined over weeks or months
- [ ] I can show specific examples where a codified lesson prevented a repeat mistake

**Score: ___ / 5**

### Level 5 - MCP and Skills
- [ ] My agent has access to at least one external tool beyond the filesystem
- [ ] I have used or built a custom skill
- [ ] I have shared a skill or MCP configuration with a teammate
- [ ] I understand the trade-off between MCP tool schemas and CLI tools
- [ ] My team has a shared registry of skills or MCPs

**Score: ___ / 5**

### Foundation Score: ___ / 22

| Score | Assessment |
|-------|------------|
| 0-8 | Early stage. Focus on Levels 1-3. |
| 9-15 | Building momentum. Level 4 is your unlock. |
| 16-22 | Solid foundation. Ready for the Frontier tier. |

---

## Section 2: Frontier (Levels 6-8)

### Level 6 - Harness Engineering
- [ ] My agent can run tests, get results, and iterate without my intervention
- [ ] I have automated feedback loops the agent uses as backpressure
- [ ] I design prompts with constraints rather than step-by-step instructions
- [ ] My agent can navigate the repo using documentation without me pointing to files
- [ ] I have seen the agent self-correct by detecting its own failure

**Score: ___ / 5**

### Level 7 - Background Agents
- [ ] I run agent tasks asynchronously and come back to results
- [ ] I use more than one agent instance in parallel
- [ ] I have used different models for different purposes
- [ ] I decouple the agent that writes code from the agent that reviews it
- [ ] I have at least one automated agent triggered by CI/CD
- [ ] I use an orchestration tool to manage multiple agents

**Score: ___ / 6**

### Level 8 - Autonomous Agent Teams
- [ ] I have run multiple agents that coordinate with each other
- [ ] I have used Claude Code Agent Teams or equivalent multi-agent framework
- [ ] I have experienced failure modes: risk-averse agents, regressions, churning
- [ ] I have CI pipelines designed as safety nets for multi-agent coordination
- [ ] I can articulate when Level 7 is better than Level 8 for a given task

**Score: ___ / 5**

### Frontier Score: ___ / 16

---

## Section 3: Beyond Code (Levels 9-11)

### Level 9 - Autonomous Deployment
- [ ] I have a pipeline where code goes from agent-written to deployed without manual steps
- [ ] Non-technical team members can trigger creation and deployment
- [ ] The pipeline includes automated quality gates (Lighthouse, accessibility)
- [ ] An AI reviewer checks output before deployment
- [ ] The whole process can be triggered and approved from a phone
- [ ] The agent can diagnose and fix deployment failures

**Score: ___ / 6**

### Level 10 - Simulation-First Development
- [ ] I test product ideas against synthetic user personas before writing production code
- [ ] I have built or used a simulation that models user behavior
- [ ] I use simulation to eliminate hypotheses before committing resources
- [ ] I calibrate synthetic results against real-world data
- [ ] I have used agent-based market simulation
- [ ] My development loop starts with simulate not build MVP

**Score: ___ / 6**

### Level 11 - Physical-Digital Bridge
- [ ] My agent reads data from physical sensors
- [ ] My agent can control physical devices
- [ ] I use Home Assistant or equivalent as a bridge between agents and hardware
- [ ] I have physical safety constraints in my agent pipeline
- [ ] I have created a digital twin of a physical system
- [ ] My agent has triggered a 3D print or produced a physical artifact

**Score: ___ / 6**

### Beyond Code Score: ___ / 18

---

## Overall Profile

```
Foundation (Levels 1-5):   ___ / 22
Frontier  (Levels 6-8):   ___ / 16
Beyond Code (Levels 9-11): ___ / 18
Total:                     ___ / 56
```

### Archetypes

| Profile | Description | Next Move |
|---------|-------------|----------|
| **Coder** (Foundation 15+, Frontier <5) | Strong basics, has not automated yet | Invest in Level 6 harness engineering |
| **Automator** (Frontier 10+, Beyond <5) | Runs agents well, has not extended beyond code | Try Level 9 deploy from phone |
| **Visionary** (Beyond 10+, Foundation <15) | Exploring frontier but skipped foundations | Go back to Level 3-5. Your advanced work is fragile. |
| **Full Stack Agentic** (All tiers strong) | Operating across the full spectrum | Teach others. Multiplayer bottleneck is your constraint. |

## Team Assessment
1. Have each member complete individually
2. Use team-radar.html to visualize the team shape
3. Find the bottleneck: team effective level is its lowest common level
4. The team levels up together or not at all
