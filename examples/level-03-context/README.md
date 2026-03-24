# Level 3: Context Engineering

## The Principle

Every token needs to fight for its place in the prompt. Noisy context is as bad as missing context.

## Getting Started

1. **Create your rules file.** Copy `CLAUDE.md.template` to your project root and fill it in. This is the single highest-leverage action you can take.

2. **Audit what your agent sees.** Before your next task, ask yourself: does the agent have the context it needs? Is it seeing anything irrelevant?

3. **Test information density.** Take a prompt that produced mediocre results. Rewrite it with half the words but the same information. Run it again. If the output improves, your original had noise.

## Level Up Checklist

- [ ] Rules file exists and is not empty boilerplate
- [ ] Rules file has been updated at least 3 times based on real experience
- [ ] You can explain the difference between "good context" and "more context"
- [ ] Your agent output quality improved measurably after adding the rules file
