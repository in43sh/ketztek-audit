# CLAUDE.md

Audit and design research for ketztek GmbH, a consultancy in Winterthur, Switzerland. The layout is in [README.md](README.md). The workspace rules in `../../../CLAUDE.md` also apply, and the prompts that produce these reports live in `docs/atlant-pro-max-research/` of the workspace, not here.

## What may be shared

- `client/` can go to ketztek after review. Write it in plain, client-ready language. Leave out internal reasoning, speculation about the freelancer's process, and notes about who wrote what.
- `internal/` is for the freelancer only. Predictions and open questions are fine there, but label them as such.
- Never invent facts about ketztek: no clients, figures, quotes, reviews, certifications, founding year, team photos or prices. Each claim needs a public source or ketztek's own material, cited in the document.
- Research is passive. Do not contact ketztek, log in anywhere or submit a form. Say so in each report, as the existing ones do.
- Keep personal data out of documents. The business's public contact details are fine.

## Where things go

- New audits and research go in `internal/research/<topic>/`. Create a topic folder for new work instead of adding to an unrelated one.
- Design status and open items are recorded in section 5 of `internal/research/design-v2/ketztek-design-v2-spec.md`. Update that section when the status changes.
- Prototypes and their code live in the sibling `../ketztek-demo` repo. This repo holds the design source and the spec. The demo's rules come from `internal/research/design-brief/ketztek-design-prompt.md`; if you change those rules, name the demo pages they affect.
- Do not commit `.playwright-mcp/` or `scratch/`; both are git-ignored and should stay that way.
- Before renaming or moving a file, search the repo for links to it (README, spec, reports) and update them.

## Gotchas

- The demo's `CLAUDE.md` cites `internal/research/design-brief/ketztek-design-prompt.md` by path. Renaming or moving that file breaks the reference there.

## Commands

There is no build, test or dependency setup. The only tool is markdownlint, which `npx` fetches on first run (this needs network access):

```bash
npx --yes markdownlint-cli2 --fix "<path>.md"   # auto-fix
npx --yes markdownlint-cli2 "<path>.md"         # check; must report 0 issues
```

## Markdown

- Follow the markdownlint rules in the workspace guidance. `.markdownlint.json` turns off MD013 (line length) and sets MD024 to `siblings_only`.
- Lint every `.md` file you write with the commands above: fix first, then check.
- Use `[text](url)` or `<url>` for links; never a bare URL.

## Git

- Commit and push only when the user asks.
- Ask before merging a branch into `main` or pushing to `main`. Say which branch and which commit would change.
- Keep commit messages short. When a change touches `client/`, leave out internal reasoning.
