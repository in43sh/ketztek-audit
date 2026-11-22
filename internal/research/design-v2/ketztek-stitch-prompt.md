# Stitch prompt: ketztek homepage, three creative directions

Date: 2026-11-21. Paste the prompt block into Stitch. The prompt gives goals, facts and hard limits. It leaves layout, grid, navigation, typography and visual language to Stitch, so the three concepts can differ from one another and from our earlier designs. It keeps the requirements from the [visual research](ketztek-visual-research.md) and the [design v2 prompt](ketztek-design-v2-prompt.md).

Before running it, check the logo. Stitch cannot draw the wordmark from a file, so the prompt asks for a labelled placeholder. Replace it with the real SVG later. Option B is still a proposal, so use the current wordmark if ketztek has not approved B.

```text
Create three homepage concepts for ketztek GmbH, a young process-automation and software firm in Winterthur, Switzerland. Each concept should be a different answer to one question: how can a page make a plant or site manager feel that a small firm understands their daily work and can fix one slow process? Make the three ideas genuinely different. Do not produce three variations of one idea.

WHO IT IS FOR
Plant, site and operations managers at small and mid-sized Swiss industrial and construction companies. Their days are paper forms, Excel files, defect lists, maintenance logs and site visits. They are sceptical of consultants and of anything that looks like a template. They read on a phone between visits and decide on a desktop.

WHAT ketztek DOES
Process analysis, automation on Microsoft 365 and the Power Platform, and custom software for industrial and construction companies. The promise is honest scale: "Sometimes the honest answer is two weeks of work, and we'll tell you that." The firm is young. It has no client logos, reviews, case studies, certifications, team photos or founding year. Do not show or imply any of them. Invent no numbers, names or quotes.

WHAT THE PAGE MUST DO
- Say at a glance what ketztek does, for whom, and where.
- Offer one clear next step that is visible on a phone without scrolling: a free 30-minute call.
- Make the small-scale, honest promise feel credible.
- Look made in 2026 by a serious, modest firm.

STARTING POINTS (ideas to explore, not requirements)
A shift handover board. A maintenance tag on a machine. A calibration certificate. A plant floor plan with one route marked. A site's daily diary. The industrial heritage of Winterthur. Pick, combine or ignore them.

HARD LIMITS
- Logo: a labelled placeholder reading "ketztek wordmark: black letters, yellow double z". Show it once.
- Colour: black #000000 and yellow #ebc34d are the fixed brand colours. Yellow is for the logo and the main action. Do not use blue, teal, green or purple, and no gradients.
- Imagery: no photographs, stock images or device mock-ups. Any picture must be drawn: diagrams, documents, process maps.
- Accessibility: WCAG 2.2 AA contrast. Body text at least 17 px on phones and 18 px on desktop. Tap targets at least 44 x 44 px. Visible keyboard focus. No horizontal scrolling from 320 to 1440 px. Respect reduced motion.
- Language: the German copy will replace the English later and runs about 30 percent longer. Leave room for it.
- No cookie banner.
- Avoid generated-design tells: all-caps labels, middle-dot strings, meaningless numbering, identical shadowed cards, and fade-ins on every section.

RETURN FOR EACH CONCEPT
- A name and the single metaphor that carries the idea.
- One sentence on why it suits a plant or site manager.
- The layout, typefaces and palette, with hex values.
- How the first screen looks at 390 x 844 and at 1440 x 900.
- The one signature element and where it appears.
- The full homepage at 390 px and at 1440 px.

COPY (use verbatim)
- Headline: "Find the process that costs you time, and fix it with the tools you already have."
- Supporting line: "Analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland."
- Primary action: "Book a free 30-minute call". Secondary: "Send a message".
- Problem: "Most inefficiency isn't a software problem. It's the recurring and repetitive tasks piling up in the background."
- Four steps: Map ("We start by tracking the root of the problem."); Propose ("Then we propose how to solve it. Often the solution is smaller, faster, and cheaper than you expected."); Build ("The people who map your process are the people who build the fix."); Teach ("Then we teach them to run it.")
- Services, each with one line: Process Analysis & Optimization ("We map your workflows end to end, work out where the time and money are going, and hand you a prioritized plan you can act on."); Automation & Digital Workflows ("Many bottlenecks disappear in weeks rather than months, using licences you already pay for."); Custom Software Engineering ("When standard tools reach their limit, we build."); Prototyping & Feasibility ("Before you commit a budget, find out whether the idea holds."); Workshops & Training ("We teach your team to get real value out of Microsoft 365 and the Power Platform.")
- Sectors: Industry & Manufacturing ("Machine data nobody looks at. Quality reports assembled by hand. Maintenance that runs on experience because the records are incomplete. We connect what's already there and digitize what's still on paper."); Construction ("Site documentation spread across paper, Excel and messaging apps. Defect lists that never quite match the plan. We move site reporting onto something people will actually use with gloves on.")
- Reasons: "We size the solution to the problem" ("Sometimes the honest answer is two weeks of work, and we'll tell you that."); "We work alongside you, not for you"; "A small team with a deep bench"; "Analysis and delivery from one team"; "You keep what we build"; "Swiss-based, on site when it matters" ("Process work can't be done over video calls alone. We come to the factory and to the building site.")
- Closing: "Not sure where to start?" ("Most of our projects begin with one frustrating process. Tell us about yours. In half an hour, we'll give you an honest opinion on whether it's worth fixing and roughly what it would take, before any invoice exists.")
- Footer: ketztek GmbH, Schulergasse 9, 8406 Winterthur, Switzerland; info@ketztek.ch; links to Impressum and Privacy.
```

## Changes in this version

- Removes the prescribed header, menu, footer, screen plan and grid. Stitch has to propose them.
- Replaces the instruction to use a fixed set of links with one goal per page.
- Adds starting points to explore and asks for a metaphor per concept.
- Keeps the hard limits, the copy and the accessibility floor, so the outputs stay honest and usable.
