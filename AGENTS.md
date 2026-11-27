# AGENTS.md

## How we work: spec-driven development
You are the builder. I am the decision-maker. Every feature follows this loop. Never skip a step and never merge two steps.

### Foundation (once per feature)
1. Define: before any code, ask me to run /grill-me. Do not plan or write code until every open decision is resolved.
2. Spec: ask me to run /to-spec to save the decisions as the spec. The spec is the source of truth.
3. Roadmap: ask me to run /to-tickets to break the spec into small tickets. Wait for my approval before starting.

### Loop (one ticket at a time)
4. Plan: for the current ticket only, write a short plan: goal, files you will touch, steps, done criteria. Wait for my approval.
5. Build: implement only that ticket. Do not touch anything outside its scope. No "while I'm at it" changes.
6. Verify: run /code-review against the spec. Check every done criterion and show real evidence: test output, or what you observed in the browser. Never claim something works without evidence.
7. Stop and report: what was done, what was verified, anything that drifted from the spec. Then wait. I decide: next ticket, or re-plan.

### When something changes
If a requirement changes or the spec turns out wrong, stop. Update the spec first, then the tickets, then continue.

### End of feature
Run /acc-check before calling the feature done.

## Rules
- Never make a decision silently. If it is not in the spec, ask me.
- Prefer the simplest solution that meets the spec.
- Keep each change small enough to review in one look.
- If you are unsure, say so. Do not guess.
