# Stitch prompt: ketztek homepage from a blank page

Date: 2026-11-21. Paste the prompt block into Stitch. It asks for three distinct directions, so the outputs differ in layout and type, not only colour. It keeps the requirements from the [visual research](ketztek-visual-research.md) and the [design v2 prompt](ketztek-design-v2-prompt.md).

Before running it, check the logo. Stitch cannot draw the wordmark from a file, so the prompt asks for a labelled placeholder. Replace that placeholder with the real SVG when you place the design in the prototype. Option B is still a proposal, so use the current wordmark if ketztek has not approved B.

```text
Design three alternative homepages for ketztek GmbH, a young process-automation and software consultancy in Winterthur, Switzerland. Create each direction from a blank page. The three directions must differ in layout system, typography and visual language, not only in colour. Do not reuse any earlier design's style or motif.

BUSINESS
ketztek does process analysis, automation (Microsoft 365 and Power Platform) and custom software for industrial and construction companies. The firm is young. It has no client logos, reviews, case studies, certifications, team photos or founding year yet. Do not show or imply any of them. Do not invent numbers, names or quotes.

AUDIENCE
Plant, site and operations managers at Swiss small and mid-sized companies. Often on a phone between site visits, then at a desktop to decide. They want to know quickly whether this small firm can fix one slow process, and then book a free 30-minute call.

SCREENS PER DIRECTION
1. Homepage, 390 x 844 phone: first screen, full page, and the menu open.
2. Homepage, 1440 x 900 desktop: first screen and full page.

FIRST SCREEN (visible without scrolling at 390 x 844 and at 1440 x 900)
- Headline: "Find the process that costs you time, and fix it with the tools you already have."
- Supporting line: "Analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland."
- Primary button: "Book a free 30-minute call". It is the strongest action on the screen.
- Secondary text link: "Send a message".
- Logo: a labelled placeholder box the size of the wordmark, reading "ketztek wordmark: black letters, yellow double z". Show it once.

BRAND
Keep only the brand colours: black #000000 and yellow #ebc34d. Use yellow for the primary button and at most one more accent. Do not use blue, teal, green or purple, and no gradients.

CONTENT (use verbatim, in this order)
1. Problem: "Most inefficiency isn't a software problem. It's the recurring and repetitive tasks piling up in the background."
2. How a project starts, four steps: Map ("We start by tracking the root of the problem."); Propose ("Then we propose how to solve it. Often the solution is smaller, faster, and cheaper than you expected."); Build ("The people who map your process are the people who build the fix."); Teach ("Then we teach them to run it.")
3. Services, each with one line: Process Analysis & Optimization ("We map your workflows end to end, work out where the time and money are going, and hand you a prioritized plan you can act on."); Automation & Digital Workflows ("Many bottlenecks disappear in weeks rather than months, using licences you already pay for."); Custom Software Engineering ("When standard tools reach their limit, we build."); Prototyping & Feasibility ("Before you commit a budget, find out whether the idea holds."); Workshops & Training ("We teach your team to get real value out of Microsoft 365 and the Power Platform.")
4. Sectors: Industry & Manufacturing ("Machine data nobody looks at. Quality reports assembled by hand. Maintenance that runs on experience because the records are incomplete. We connect what's already there and digitize what's still on paper."); Construction ("Site documentation spread across paper, Excel and messaging apps. Defect lists that never quite match the plan. We move site reporting onto something people will actually use with gloves on.")
5. Why work with us, six reasons: "We size the solution to the problem" ("Sometimes the honest answer is two weeks of work, and we'll tell you that."); "We work alongside you, not for you"; "A small team with a deep bench"; "Analysis and delivery from one team"; "You keep what we build"; "Swiss-based, on site when it matters" ("Process work can't be done over video calls alone. We come to the factory and to the building site.")
6. Closing: "Not sure where to start?" ("Most of our projects begin with one frustrating process. Tell us about yours. In half an hour, we'll give you an honest opinion on whether it's worth fixing and roughly what it would take, before any invoice exists."), the button "Book a free 30-minute call", and the text link "Send a message".

VISUAL RULES
- No photographs, stock images, device mock-ups, dashboards or floating cards.
- Where the work needs a picture, use drawings, process diagrams or document layouts. Do not draw people or machines.
- Left-aligned text throughout, except the closing block.
- One or two typefaces, licensed for self-hosting. Do not use Inter, Manrope or Montserrat.
- No cookie banner.
- Tone is plain, concrete and a little dry. Never salesy. Avoid "seamless", "innovative", "cutting-edge" and "digital transformation".

ACCESSIBILITY
WCAG 2.2 AA contrast: at least 4.5:1 for body text and 3:1 for large text and interface edges. Body text at least 17 px on phones and 18 px on desktop. Lines under 75 characters. Tap targets at least 44 x 44 px. Visible keyboard focus. No horizontal scrolling from 320 to 1440 px. Respect reduced motion.

FOR EACH DIRECTION, STATE
- The direction name and a one-sentence idea.
- The layout system, the typefaces and the palette, with hex values.
- Any signature device, and where it appears.
```

## Changes from the first version

- Asks for three directions that differ in layout, type and visual language, so the outputs can be compared.
- Adds the logo placeholder, since Stitch cannot draw the SVG.
- Forbids invented facts: no numbers, names, quotes, founding year or team photos.
- States the contrast ratios explicitly.
- Asks each direction to report its system, so the outputs can be compared.
