---
name: ub-mode
description: Apply a proportionate engineering workflow to code changes where behavior, design, or tests need care. Use when the user invokes ub-mode or asks for disciplined implementation.
---

# ub-mode

Make the requested behavior work, then improve the code enough to keep it clear and safe to change. Fit the amount of process to the size and risk of the task. Follow repository instructions and the user's chosen workflow.

## First make it work

1. Identify the observable outcome and inspect the relevant code before editing. For a bug, reproduce the failure when practical.
2. Choose the smallest coherent change that solves the actual problem. Check whether a new requirement belongs in the existing design before adding a special case. Keep each decision in one place.
3. Validate external data at the boundary. Use types or structures to rule out invalid states when that simplifies the code. Make retryable operations idempotent when partial execution is a real possibility.
4. For behavior changes with a clear testable outcome, prefer a failing test or reproduction before the fix. For a trivial edit, use a direct check. Do not create a test that only mirrors the implementation.

## Then make it right

1. Verify behavior through the public interface or the path its real user takes. Check the regression and relevant edge cases. A test should fail if the behavior it claims to protect is broken.
2. Refactor only where the change exposes a concrete problem, such as repeated decisions, tangled boundaries, or hard-to-test logic. Keep behavior stable while changing structure.
3. Use available quality tools when they support the project's language and the result can guide this change. Treat complexity, duplication, coverage, and mutation scores as diagnostic signals. Investigate findings before changing code to satisfy a number.
4. Run the relevant project checks. For a large change, verify in small units; for a small change, avoid a longer gate unless repository policy requires it.

## Practice

- Preserve existing work and follow the repository's branch and review conventions. Create commits or push only when the user requests it or the established task workflow calls for it.
- Clean up temporary work you created after checking it is no longer needed.
- Report what changed, how you verified it, and any material limitation. Keep the report concise; an action-by-action log is unnecessary.
