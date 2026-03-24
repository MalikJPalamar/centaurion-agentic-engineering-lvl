# Level 9: Autonomous Deployment Pipeline

## The Goal
From a prompt on your phone to a live production URL, with no laptop required.

```
Phone prompt -> Agent generates page -> Git push -> CI tests ->
AI review -> Deploy -> Verify live -> Send notification
```

## Starter GitHub Actions Workflow

### .github/workflows/auto-deploy.yml

```yaml
name: Autonomous Deploy Pipeline

on:
  push:
    branches: [main]
    paths: ['src/pages/**', 'src/landing/**']

jobs:
  build-and-test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '20'
          cache: 'npm'
      - run: npm ci
      - run: npm run lint
      - run: npm run type-check
      - run: npm test

  lighthouse:
    needs: build-and-test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '20'
          cache: 'npm'
      - run: npm ci && npm run build
      - uses: treosh/lighthouse-ci-action@v12
        with:
          configPath: './lighthouserc.json'
          uploadArtifacts: true

  deploy:
    needs: [build-and-test, lighthouse]
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: amondnet/vercel-action@v25
        with:
          vercel-token: ${{ secrets.VERCEL_TOKEN }}
          vercel-org-id: ${{ secrets.VERCEL_ORG_ID }}
          vercel-project-id: ${{ secrets.VERCEL_PROJECT_ID }}
          vercel-args: '--prod'

  verify-and-notify:
    needs: deploy
    runs-on: ubuntu-latest
    steps:
      - name: Verify live site
        run: |
          sleep 30
          STATUS=$(curl -s -o /dev/null -w "%{http_code}" ${{ secrets.PRODUCTION_URL }})
          if [ "$STATUS" != "200" ]; then exit 1; fi
      - name: Notify via Slack
        if: success()
        uses: slackapi/slack-github-action@v1.26
        with:
          payload: '{"text": "Deployed: ${{ github.event.head_commit.message }}"}'
        env:
          SLACK_WEBHOOK_URL: ${{ secrets.SLACK_WEBHOOK }}
```

### lighthouserc.json
```json
{
  "ci": {
    "assert": {
      "assertions": {
        "categories:performance": ["error", { "minScore": 0.8 }],
        "categories:accessibility": ["error", { "minScore": 0.9 }],
        "categories:seo": ["error", { "minScore": 0.9 }]
      }
    }
  }
}
```

## Phone-First Triggers
- **Slack bot**: message a channel with the prompt
- **GitHub Issue**: create from mobile app, label triggers agent
- **Custom API**: POST to endpoint that starts the pipeline

## Level Up Checklist
- [ ] CI pipeline builds, tests, and deploys on push
- [ ] Quality gates block deploys below threshold
- [ ] A non-technical person has triggered a deploy
- [ ] Full cycle takes under 15 minutes
- [ ] You can trigger and approve from your phone
