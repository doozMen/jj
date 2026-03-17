---
name: block-upstream-pr
enabled: true
event: bash
pattern: gh\s+pr\s+create(?!.*--repo\s+doozMen/)
action: block
---

🚫 **PR targeting upstream detected**

You are in a fork. PRs must target the fork owner's repo, not upstream.

Use `--repo doozMen/<repo>` to target the correct repository.

Example:
```
gh pr create --repo doozMen/jj --base main --head my-branch
```

Never open PRs against upstream from a fork unless explicitly instructed.
