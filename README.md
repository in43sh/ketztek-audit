# ketztek audit

Audit and design research for ketztek GmbH, a process analysis, automation and custom software consultancy in Winterthur, Switzerland, for industrial and construction companies.

The work covers the current website (ketztek.com) and a new design. The prototype built from it lives in the sibling repo [ketztek-demo](../ketztek-demo/), which is live at <https://ketztek-demo.vercel.app>.

## Folders

| Folder | What it holds | Shared with |
| --- | --- | --- |
| `client/` | Reports and design material written for ketztek: the website report, the design summary, the logo options and the design presentation | ketztek, after review |
| `internal/research/` | Working audits, research, the design brief, the design v2 spec and Stitch prompts | Internal only |

Git ignores `.playwright-mcp/` (browser captures from the audit sessions) and `scratch/` (temporary files).

## Documents

### Client

| Document | What it covers |
| --- | --- |
| [Website report](client/reports/ketztek-client-report.md) | Plain-language findings on the current site, with the three fixes to make first |
| [Design summary](client/reports/ketztek-design-summary.md) | How the current site looks and reads on phones and desktop |
| [Design presentation](client/design-presentation/index.html) | Static design proposal; open it in a browser |
| [Logo options](client/logo-options/preview.html) | Logo options A, B and C in light, dark, mono and icon versions |

### Audits and research

| Document | What it covers |
| --- | --- |
| [Web presence audit](internal/research/audit/ketztek-audit-report.md) | Site inventory, competitors, keywords, information architecture, roadmap and measurement plan |
| [UX audit](internal/research/ux-audit/ketztek-ux-audit.md) | Usability findings with evidence |
| [Visual design audit](internal/research/design-audit/ketztek-design-audit.md) | Design as built, template check, design direction and prioritized changes |
| [Design research](internal/research/design-brief/ketztek-design-research.md) | Audience, content inventory, category landscape, requirements and design directions |
| [Design brief](internal/research/design-brief/ketztek-design-prompt.md) | Palette, type, pages, copy bank and the "Do not" list; the demo follows it |
| [Prototype checks](internal/research/design-brief/ketztek-prototype-checks.md) | Acceptance checks run on the first prototype and their results |

### Design v2

| Document | What it covers |
| --- | --- |
| [Design v2 spec](internal/research/design-v2/ketztek-design-v2-spec.md) | Three directions, scoring, the chosen direction and the current status (section 5) |
| [Design v2 visual research](internal/research/design-v2/ketztek-visual-research.md) | Local visual culture, competitors and reference board |
| [Design v2 prompt](internal/research/design-v2/ketztek-design-v2-prompt.md) | The research and build brief for the design v2 work |
| [Stitch prompt, three directions](internal/research/design-v2/ketztek-stitch-prompt.md) | Prompt for generating three homepage concepts in Stitch |
| [Stitch prompt, blank page](internal/research/design-v2/ketztek-stitch-prompt-fresh.md) | Stitch prompt that starts from a blank page and leaves out the earlier design family |

## Where to start

Read section 5 of the [design v2 spec](internal/research/design-v2/ketztek-design-v2-spec.md) for what is done and what is still open. The website report is the document to share with ketztek once it has been reviewed.

## Conventions

Markdown follows the rules in `.markdownlint.json`, which turns off line-length checks. Lint a file with `npx --yes markdownlint-cli2 "<path>"`.

The working rules for this repo are in [CLAUDE.md](CLAUDE.md).
