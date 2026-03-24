# Level 5: MCP and Skills

## The Principle

The agent can now **act**, not just think. MCPs and skills connect it to databases, APIs, CI, browsers, and Slack.

## Getting Started

1. **Start with one MCP.** Don't connect 15 tools at once.
2. **Consider CLI over MCP.** MCPs inject full schemas on every turn. CLIs only inject output when called.
3. **Share skills with your team.** Skills get the same treatment as code: PRs, reviews, version history.

## Starter MCP Config (Claude Code)

```json
{
  "mcpServers": {
    "github": {
      "command": "gh",
      "args": ["mcp"]
    }
  }
}
```

## Level Up Checklist

- [ ] Agent has at least one external tool connected
- [ ] You've built or customized a skill
- [ ] You've shared a skill with a teammate
- [ ] You understand the MCP vs CLI trade-off for token efficiency
