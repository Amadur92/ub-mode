# ub-mode

`ub-mode` is an agent skill that enforces disciplined software engineering principles when writing or changing code:

1. **First Make it Work** — Laziness Protocol, Foundational Thinking, TDD, Redesign From First Principles, Attack the Premise, Subtract Before You Add, Outcome-Oriented Execution, Build the Lever, and Architecture (Model the Domain, Boundary Discipline, Type System Discipline, Make Operations Idempotent, Separate Before Serializing Shared State).
2. **Then Make it Right** — Fix Root Causes, Sequence Work into Verifiable Units, Test Behavior (Not Implementation), [Crapper](https://github.com/unclebob/crapper) ($\text{CRAP} < 10$), [Dryer](https://github.com/unclebob/dryer) (duplication $< 0.8$), [Mutator](https://github.com/unclebob/mutator) (cover the uncovered, kill the survivors, delete dead code), and Refactoring.
3. **Practice** — Keep a Log, Guard the Context Window, Worktree Cleanup, and Commit and Push in small ordered commits.

## Companion Tools

- [crapper](https://github.com/unclebob/crapper) — Cyclomatic complexity, test coverage, and CRAP score analysis.
- [dryer](https://github.com/unclebob/dryer) — Structural duplication detector.
- [mutator](https://github.com/unclebob/mutator) — Mutation testing tool.
- [uml-viewer](https://github.com/unclebob/uml-viewer) — Component, metric, and dependency visualizer.

## Installation

Copy `SKILL.md` into your agent's skills directory as `ub-mode/SKILL.md` (for example `~/.grok/skills/ub-mode/SKILL.md`, `~/.claude/skills/ub-mode/SKILL.md`, or `~/.cursor/skills/ub-mode/SKILL.md`), then invoke `/ub-mode`.
