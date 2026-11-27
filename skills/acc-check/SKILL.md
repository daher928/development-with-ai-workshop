---
name: acc-check
description: Final gate before calling AI-assisted work done. Checks Accountability, Control, and Confidence against the project's definition, plan, and changes. Use when finishing a task or feature, before merge, or when the user says "acc check" or asks whether the work is ready to sign off.
---

# ACC Check

AI helps build. A human owns the result. This skill checks whether that is true.
It never signs off for the user.

## 1. Gather evidence first (read before you ask)

- The definition or design doc, and the plan or task list. Look in docs/, specs/, or ask where they are.
- The changes: `git diff` against the base branch.
- Verification output: run the project's tests or checks if the commands are known, otherwise ask.

## 2. Run the three tests

**Accountability: can the human explain the major decisions?**
List the 3-5 biggest decisions in the changes (technology, structure, dependencies, behavior).
For each, mark whether it came from the definition/plan (human-decided) or was introduced by the agent.
Flag every agent-introduced decision the user has not approved.
Then ask the user to explain the top two in their own words. Do not answer for them.

**Control: is the work on track, and does the user know everything that was done?**
Compare plan vs changes: tasks done, tasks missing, changes no task mentions (scope drift).
Surface anything the user may not know about: new dependencies, deleted files, config changes.

**Confidence: does the result match the intent?**
Map each "done" criterion to evidence. Mark it:
- Verified: you observed a passing test or real output.
- Claimed only: the agent said so, nothing observed.
- Unchecked: no evidence either way.
Run checks where you can. Never mark Verified without something observed.

## 3. Report

| Test | Status | Gaps |
|---|---|---|
| Accountability | pass / gaps | ... |
| Control | pass / gaps | ... |
| Confidence | pass / gaps | ... |

Then give a verdict: **READY TO SIGN** or **NOT YET**, with the specific gaps.

## 4. Rules

- Evidence over claims. Fluent output is not proof.
- Do not fix anything here. List gaps. Fixes go back to the loop: update the definition, re-plan, rebuild.
- End by asking: "Would you sign this as is?" The user's answer is the result.
