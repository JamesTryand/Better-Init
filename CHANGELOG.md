## [1.3.1] - 2026-11-11
### Changes
- Reworded `## How to work here` so it can be copied verbatim into any project: one "ask or assume, out loud" rule (ask when the readings lead to different results or the choice is hard to undo; otherwise pick one, say so and record it) that applies mid-work as well as at the start; re-check what was built on an assumption that proves wrong; simplicity merged into scope; an explicit "use judgment for small, obvious changes".
- Project-specific locations (where assumptions, plans and gaps are recorded) now go in a separate `## Where things go` section, so the block itself never drifts between projects.
- When merging, an older version of the block is replaced with the current one, and the draft points out the change.

## [1.3.0] - 2026-11-11
### Features
- Every drafted `CLAUDE.md` now includes a `## How to work here` block of standing rules adapted from Andrej Karpathy's LLM coding guidelines: ask when a request is ambiguous, raise assumptions openly, push back when warranted, write plan steps with checks, change only what was asked, keep it simple, don't invent facts, and count something as done only once it is verified.
- When merging into an existing `CLAUDE.md`, an existing `## How to work here` block is kept, never dropped or weakened.

### Design Rationale
- Project templates (e.g. pmt issue templates) carry these rules. Better Init can rewrite their `CLAUDE.md`, so it must keep the rules rather than silently remove them.
- Each rule is phrased so a reviewer can see whether it was followed, rather than as general advice.

## [1.2.0] - 2026-03-31
### Features
- Added an optional "Claude reply efficient mode" that inserts the approved instruction block into generated `CLAUDE.md` only when the user explicitly opts in.
- Embedded the verbatim block directly in `better-init/SKILL.md` so the installed skill remains self-contained.
- Updated `README.md` to document the new option, default-off behavior, downstream naming expectations, and source acknowledgement.

### Design Rationale
- Keep Better Init's default behavior unchanged while allowing users to opt into a stricter response style.
- Embed the block in the skill so installation still works when only the `better-init` folder is copied into `~/.claude/skills/`.
- Use a user-facing mode name in skill behavior instead of leaking a temporary source-file name.
- Preserve the exact provided wording of the optional block instead of rewriting it.

### Notes & Caveats
- "Claude reply efficient mode" is included only on explicit opt-in.
- Downstream generated instructions do not mention temporary source-file names.
- The temporary source file remains in this repo only as source material for the embedded block.
