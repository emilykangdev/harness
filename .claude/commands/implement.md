# /implement

You are entering the implementation phase. The plan is finalized. Now you execute it.

## prerequisites

- A reviewed and approved `/plan` with no open questions
- Clear task ordering and dependency map

## process

1. **Review the plan** - Re-read the full plan. Confirm you understand every task and its dependencies.
2. **Execute in order** - Work through tasks respecting the dependency graph. For parallelizable tasks, spawn subagents if possible.
3. **Follow the plan precisely** - Don't improvise. If you hit something the plan didn't account for, STOP and flag it rather than making assumptions.
4. **Verify each task** - After completing each task, run the verification step from the plan. Don't move on until it passes.
5. **Build verification** - After all tasks are complete:
   - Run the build/compile step
   - Run relevant tests
   - Check for type errors, lint issues, and warnings
   - Fix any issues found
6. **Self-review** - Review the full diff of your changes:
   - Does every change serve the plan?
   - Are there any leftover debug statements, TODOs, or commented-out code?
   - Does the code follow existing project conventions?
   - Are there any obvious edge cases you missed?
7. **Prepare the result** - Summarize what was done, any deviations from the plan (and why), and any follow-up items.

## rules

- Follow the plan. If the plan is wrong, go back to `/plan` and fix it. Don't silently deviate.
- Verify before moving on. Each task has a verification step for a reason.
- No TODO comments in shipped code. Either do it now or add it to follow-up items.
- No dead code. Don't comment things out "just in case." Use version control.
- If you encounter an unexpected error or blocker, describe it clearly and ask for guidance. Don't guess.

## output

When implementation is complete, provide:
- **Summary** of changes made
- **Deviations** from the plan (if any) with reasoning
- **Verification results** - build status, test results, lint output
- **Follow-up items** - anything that should be addressed next
