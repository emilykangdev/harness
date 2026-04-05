# /plan

You are entering the planning phase. The discussion is done. Now you're creating a structured, executable implementation plan.

## prerequisites

- A completed `/discussion` phase with a summary in the context file
- Shared understanding of the problem, approach, and constraints

## process

1. **Research** - Do any additional codebase exploration or external research needed to ground the plan. Look at existing patterns, conventions, and dependencies.
2. **Draft the plan** - Create a structured implementation plan that includes:
   - Task list in execution order
   - For each task: files to touch, pseudocode or detailed description, error handling, edge cases
   - Dependencies between tasks (what must happen before what)
   - Parallelization opportunities (what can happen simultaneously)
3. **Self-review** - Before presenting the plan, review it yourself:
   - Are there any open questions? (There shouldn't be. Resolve them or flag them.)
   - Is every task scoped to be completable in one pass?
   - Are instructions concrete and specific, not aspirational?
   - Are you replacing things cleanly or shimming on top of existing code?
   - Does the plan respect existing codebase conventions?
4. **Present for review** - Show the plan to the human. Ask targeted questions about anything you're uncertain about.
5. **Iterate** - Incorporate feedback, re-review, repeat until the plan is solid.

## plan format

```
## Implementation Plan: [feature/fix name]

### Summary
[1-2 sentences on what this plan accomplishes]

### Tasks

#### Task 1: [name]
- **Files**: [list of files to create/modify]
- **Dependencies**: [which tasks must complete first, or "none"]
- **Details**: [specific implementation steps with pseudocode]
- **Error handling**: [how failures are handled]
- **Verification**: [how to confirm this task is done correctly]

#### Task 2: [name]
...

### Parallelization
[Which tasks can run simultaneously]

### Risk areas
[Anything that might go wrong and mitigation strategies]
```

## rules

- No open questions in the final plan. Everything must be resolved.
- Scope each task to one agent session. If a task is too big, break it down.
- Write instructions, not aspirations. "Add error handling" is bad. "Wrap the API call in a try/catch that returns a 500 with the error message" is good.
- Replace completely, don't shim. If you're modifying existing code, prefer clean replacement over patching.
- Include verification steps for every task. How do you know it worked?
