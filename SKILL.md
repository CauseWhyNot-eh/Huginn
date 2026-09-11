---
name: huginn
description: Sharpen vague ideas into buildable specs.
version: 0.2.0
author: Nachi, Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [Ideas, Specs, Planning]
    related_skills: [shrimp-brainstorming]
---

# Huginn Skill

Takes a vague idea and returns a spec with features, build steps, and working. Does not write code or validate markets. Needs the raw idea text to start.

## When to Use

- User gives a vague app, site, skill, or workflow idea to clarify.
- User asks to list features, build steps, or inner working for an idea.
- Don't use for: one-off facts, debugging, or coding tasks.

## Prerequisites

- Raw idea in 1-3 lines.

## How to Run

- Start when user says sharpen, clarify my idea, or gives a vague build idea.

## Procedure

1. **Record.** Save raw idea verbatim with date.
   Done when: raw text stored and echoed back.
2. **Gap-check.** Answer from context first, drop solved items, ask at most 3 gaps (user, scope, mode).
   Done when: at most 3 open gaps listed with current guesses.
3. **Options.** Propose 2-3 directions with differences in scope.
   Done when: 2-3 options exist with scope differences stated.
4. **Sharpen.** Expand picked option into features V1 vs later, build steps, user flow plus system flow, open unknowns.
   Done when: spec contains features V1 vs later, build steps, user flow plus system flow, unknowns.
5. **Lock.** State spec version and next single action.
   Done when: version plus next action recorded.
6. **Learn.** Scan the run for learning signals; write only on a hit, never filler. Signals: "like this, not like this" (format) goes to prefs.md; "also do this when doing that" (scope add) goes to procedure or pitfalls; "don't need this kind of info" (scope cut) goes to procedure or pitfalls; direct "remember this" saves at once; same point made twice saves the pattern; one-off noise is ignored.
   Done when: each hit saved to the right layer, or no hit and files untouched.

## Pitfalls

- Asking more than 3 questions causes stall; ask at most 3 with guesses.
- Mixing V1 and later causes bloat; separate V1 vs later lists.
- Skipping unknowns causes rework; list unknowns explicitly.

## Verification

- [ ] Raw idea echoed before questions.
- [ ] Open gaps 3 or fewer.
- [ ] Spec has V1 vs later, build steps, user flow, system flow, unknowns.
- [ ] Next action is one item.
- [ ] Learning hits saved, or no-hit run left files untouched.
