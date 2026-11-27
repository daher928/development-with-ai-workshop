# Prompting Is the Easy Part. Making It Work Is the Skill.

Resources from workshops with Daher Daher. Everything here is open source and ready to use in your next project.

## The idea in one line

AI writes code fast. Fast is not the same as right. Building with AI you can trust needs two things: a standard (ACC) and a loop (spec-driven development).

## The ACC standard

Three questions to ask about anything you build with AI:

- **Accountability:** Can I explain every major decision, and why?
- **Control:** Do I know what was done, am I still on track, and do I know what comes next?
- **Confidence:** Would I sign off and deliver this as it is?

If any answer is no, go back and fix your definition before you build more.

## The loop

**Foundation (once per feature)**

1. **Define:** `/grill-me` interviews you until every open decision is made.
2. **Spec:** `/to-spec` saves those decisions as the spec, your source of truth.
3. **Roadmap:** `/to-tickets` breaks the spec into small tickets.

**Loop (one ticket at a time)**

4. **Plan:** the agent plans the current ticket. You approve.
5. **Build:** the agent implements only that ticket.
6. **Verify:** `/code-review` checks the code against the spec. Evidence, not claims.

**End of feature:** `/acc-check` runs the three ACC tests.

## What's in this repo

| Item | What it is |
| --- | --- |
| `skills/acc-check/SKILL.md` | The ACC final-gate skill |
| `AGENTS.md` | Workflow template: drop it at your repo root |
| `demo/prompt.md` | The opening prompt from the live demo |

## Setup (10 minutes)

**1. Install Matt Pocock's skills** (open source, MIT)

```bash
npx skills@latest add mattpocock/skills
```

Then, once per repo, run `/setup-matt-pocock-skills` in your agent. Choose GitHub Issues or local files as your tracker.

**2. Install acc-check**

Copy `skills/acc-check/` from this repo into your agent's skills folder (for Claude Code: `~/.claude/skills/`).

**3. Add the workflow**

Copy `AGENTS.md` to your project's root.

## Your first loop this week

1. Pick one small feature you own. An existing project is fine.
2. Describe the goal and constraints to your agent. Do not ask it to code yet.
3. Let it grill you. Answer every question; that is where your decisions get made.
4. Save the spec, cut tickets, and build one ticket only.
5. Run `/code-review`, then `/acc-check`. Ask yourself: would I sign this?

One full loop teaches more than any slide.

## Good to know

- Read a skill's `SKILL.md` before installing it. Skills are instructions your agent will follow.
- Install only from official sources: `mattpocock/skills` and this repo.
- These tools change fast. If a command moved, check the source repo's README.

## Links

- Matt Pocock's skills: https://github.com/mattpocock/skills
- Agent Skills standard: https://agentskills.io
- Arab AI Collective: https://chat.whatsapp.com/D0HJpdeNmFIKNtzBtt7wkL
- Daher on LinkedIn: https://www.linkedin.com/feed/foryou/
- Daher's Website: https://www.daherdaher.com
