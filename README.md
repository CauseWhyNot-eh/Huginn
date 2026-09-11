# Huginn

Huginn is named after Odin's raven — the bird that flew out every morning and came back with what it saw.

This one does the same for your ideas. You give it something vague and half-formed. It flies around it, looks at it from a few angles, and comes back with something you can actually build from. Not motivation. A spec.

## What it does

Takes a vague app, site, skill, or workflow idea — the kind you'd explain badly at 1am — and sharpens it into:

- what it actually is and who it's for,
- features split into V1 vs later,
- concrete build steps,
- how it works for the user *and* behind the scenes,
- open unknowns you're still guessing at,
- exactly one next action.

## What it doesn't do

No code. No market validation, no "TAM is $40B" theater. If you want your idea grilled until it proves useful, that's a different bird. Huginn assumes the idea is worth building and focuses on making it *buildable*.

## How a run goes

Six steps. Each one has a finish line — a run isn't done because the text looks nice, it's done because each step's check passed.

**1. Record.** Your raw idea gets saved word-for-word with the date, then echoed back. Nothing gets "cleaned up" before you agree that's what you meant.

**2. Gap-check.** At most 3 questions, and only the ones that actually change the answer — usually who it's for, what scope, and what shape (app, site, skill, workflow). Anything answerable from context gets answered, not asked. Guesses are shown, not hidden.

**3. Options.** 2–3 directions with genuinely different scopes. Not three flavors of the same thing.

**4. Sharpen.** The picked direction gets expanded: V1 vs later features, build steps in order, user flow plus system flow (input → logic → output), and unknowns listed explicitly instead of smoothed over.

**5. Lock.** Spec version plus one next action. One. If everything is the next action, nothing is.

**6. Learn.** This is the part that makes Huginn different from a prompt template. After each run it scans for learning signals — and writes back *only* on a hit:

| You say something like | It learns | Where it goes |
|---|---|---|
| "like this, not like that" | format correction | `prefs.md` |
| "also do this when doing that" | scope addition | procedure or pitfalls |
| "don't need this kind of info" | scope cut | procedure or pitfalls |
| "remember this" | direct instruction | saved at once |
| same point twice, reworded | pattern | saved |
| one-off remark | noise | ignored, files untouched |

Quiet runs write nothing. A learning file full of filler is worse than an empty one, so the rule is: no signal, no write.

## Repo layout

- `SKILL.md` — the workflow core. Frozen steps, checkable finish lines, no style talk.
- `prefs.md` — the style layer. Plain words, short paragraphs, tables for comparison. Capped at 10 lines by design; if it grows past that, something gets merged or cut.
- `learnings.md` — lessons from real runs. Ships empty. Fills only through step 6.
- `templates/spec.md` — the blank spec shape every run fills in.
- `templates/example.md` — one worked example so you can see what "done" looks like.

The split is deliberate: the core almost never changes, the style layer changes slowly, and the learnings change whenever reality teaches something. Three speeds, one skill.

## Requirements

A host that can run skills in this format (built for Hermes Agent), plus 1–3 lines of raw idea to start. No API keys, no installs, no dependencies.

## Verification

A finished run must pass all of these:

- [ ] raw idea echoed before any questions,
- [ ] 3 or fewer open gaps,
- [ ] spec has V1 vs later, build steps, user flow, system flow, unknowns,
- [ ] next action is one item,
- [ ] learning hits saved, or a quiet run left the files untouched.

## Version

0.2.0 — MIT.
