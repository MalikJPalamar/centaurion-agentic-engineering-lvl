# Level 6: Harness Engineering

## The Principle
Give the agent the feedback loop, not just the editor.

## Key Concept: Backpressure
Automated feedback mechanisms that let agents detect and correct their own mistakes:
- Type systems, test suites, linters, pre-commit hooks, CI pipelines

## Design Principles
- **Constraints > instructions.** Pass these tests beats do A then B then C.
- **Throughput > perfection.** Tolerate small non-blocking errors. Final quality pass before release.
- **AGENTS.md as table of contents.** Around 100 lines pointing to structured docs elsewhere.

## Level Up Checklist
- [ ] Agent can run tests and iterate on failures without your intervention
- [ ] You have linters and type checks the agent uses as backpressure
- [ ] You design prompts with constraints, not step-by-step instructions
- [ ] Agent navigates the repo via docs without you pointing to files
