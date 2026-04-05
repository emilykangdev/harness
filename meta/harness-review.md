# Harness Review

Use this prompt periodically to review and improve the harness itself. Run it after completing a significant project or when you feel the workflow is getting stale.

---

## the prompt

You are reviewing a development harness - a collection of AI prompts, slash commands, and configurations used to build software with AI agents. Your job is to identify what's working, what's not, and what should change.

### context to provide

1. The current harness files (this repo)
2. Recent project outcomes - what went well, what didn't
3. Current AI model capabilities (what's new since last review)
4. Any friction points you've noticed

### review dimensions

1. **Effectiveness** - Are the slash commands producing good results? Are the prompts specific enough? Are there gaps in the pipeline?
2. **Efficiency** - Are there redundant steps? Can commands be consolidated? Are you fighting the workflow instead of flowing with it?
3. **Model fit** - Are the prompts tuned for current model capabilities? Are you over-specifying things the model handles well now? Under-specifying things it still struggles with?
4. **Portability** - Can you drop this into a new project and go? What assumptions does it make about project structure?
5. **Evolution** - Look at `EVOLUTION.md`. Is the harness trending in the right direction? Are changes compounding or just churn?

### output format

```
## Harness Review - [date]

### What's working
- [specific thing and why it works]

### What's not working
- [specific thing and what goes wrong]

### Recommendations
- [specific change with rationale]
- [priority: high/medium/low]

### Model capability notes
- [what's changed in model capabilities since last review]
- [how the harness should adapt]
```

### when to run this

- After every 3-5 significant features built using the harness
- When you upgrade to a new model version
- When something feels consistently off about the workflow
- Monthly at minimum
