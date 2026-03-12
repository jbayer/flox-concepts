## Forge Planning Context

This project uses Forge for structured planning.
Planning artifacts live in `.forge-context/`.

- `/forge:explore` - Discover and frame problems
- `/forge:work` - Build and deliver solutions
- `/forge:retro-note` - Capture process observations
- `/forge:improve` - Apply notes as improvements
- `/forge:audit` - Verify context accuracy
- `/forge:digest` - Summarize recent planning activity
- `/forge:reviewable` - Restructure commits for review

Context files in `.forge-context/context/` describe
the project, team, and guidelines. Keep these updated
as the project evolves, or run `/forge:audit` to
check for drift.

If `.forge-context/overrides/terminology.md` exists
and has non-empty mappings, use the team's preferred
terms in all output. When the user says their term,
understand it as the Forge term. When producing
output, use their term instead.
