# Demo: opening prompt

The prompt gives only the goal and constraints. The workflow lives in AGENTS.md, so the agent should ask for /grill-me on its own.

```
I want to build a small expense splitter for a group trip. Friends add the expenses they paid, and the app shows who owes whom at the end.

Constraints: plain JavaScript on Node. Keep the split logic in its own module with unit tests using node:test. A simple HTML page for the UI. No frameworks, no backend.
```

Left open on purpose, for the grilling: equal vs custom splits, rounding and the leftover cent, multiple payers per expense, how balances are shown.
