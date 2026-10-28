# ub-mode

A lightweight engineering skill for coding agents. It keeps the original [unclebob/ub-mode](https://github.com/unclebob/ub-mode) sequence: first make the requested behavior work, then make the code clear and safe to change.

This fork makes the workflow proportional to the task:

- Use a failing test or reproduction for meaningful behavior changes; use a direct check for trivial edits.
- Apply complexity, duplication, coverage, and mutation tools when they fit the project and can guide a decision. Their scores are diagnostic signals, not universal gates.
- Refactor when there is a concrete design problem to solve.
- Follow the user's Git workflow. The skill does not require commits, pushes, or an action-by-action log.

The skill is in [`SKILL.md`](SKILL.md). It contains no executable code or bundled dependencies.

## Install for Codex

From a Codex environment with the built-in skill installer:

```bash
python3 ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo Amadur92/ub-mode --ref master --path . --name ub-mode --method git
```

The skill becomes available on the next turn. Invoke it as `$ub-mode` or ask for its disciplined coding workflow.
