# Stitch prompt: ketztek homepage from a blank page

Date: 2026-11-21. This replaces [the first Stitch prompt](ketztek-stitch-prompt.md) for new runs. It keeps the facts, honesty rules, accessibility floor and local-market findings from the [visual research](ketztek-visual-research.md). It drops every visual decision made so far.

## Why the first two runs looked like the old design

The two Stitch projects produced six concepts: Swiss Industrial Grid, Editorial Monograph, High-Contrast Workshop, Shift Handover Board, Technical Calibration Sheet, and Plant Floor Plan. All six belong to one family: paper, documents and technical drawings on a white or grey page, in black and yellow. The earlier designs (Rapport, Drawing sheet, Measured, options A to D) come from the same family.

The old prompt caused this:

- Its "starting points" were all documents: a handover board, a maintenance tag, a calibration certificate, a floor plan and a site diary.
- It locked the palette to black and yellow and banned every other hue that would give a different mood.
- It banned photographs, so the only pictures left were drawings of documents.
- Its verbatim copy came in the old section order (problem, four steps, services, sectors, reasons), so every concept had the same page structure.
- At about 8,600 characters, it was long enough for Stitch to drop parts. One user on Google's forum reports that Stitch consistently leaves out components above roughly 5,000 characters ([Stitch Prompt Guide](https://discuss.ai.google.dev/t/stitch-prompt-guide/83844)). Google publishes no limit.

## How to run it

Each direction gets its own Stitch project and runs in three short steps. Each step is under 4,500 characters.

1. Create **one new Stitch project per direction** (A, B, C, and D if you want a fourth). Stitch carries one design system across a project's screens, so concepts made in one project pull together.
2. Upload only the logo (`logo-wordmark.png`, transparent background). Do not upload earlier screenshots, design files or a design system from the old projects.
3. **Step 1, design:** paste one direction block, then the core brief below it, as one prompt. The direction goes first so it leads.
4. **Step 2, copy:** when the layout looks right, paste the copy prompt in the same project. It fills in the text without changing the design.
5. **Step 3, German:** paste the German prompt to get the first phone screen in German.
6. If a result drifts back to paper, drawings or black and yellow, reply: "This looks like the earlier concepts. Go back to the direction and start again."

Then compare the projects with the [checklist](#checklist-for-comparing-the-results).

If a step goes wrong:

- **Step 2 changes the layout.** Forum users report that Stitch can break a working layout when content is added. Paste the copy one section at a time, or generate the filled page as a new screen and keep the step 1 screen.
- **Step 1 returns only the desktop page.** Select the desktop screen and ask: "Make the 390 px phone version of this screen."

Test with direction A or C first. They differ most from the earlier designs.

## Step 1: direction blocks

Paste exactly one, then the core brief.

### A. People and places

```text
Design a homepage for ketztek GmbH in Winterthur, Switzerland, in this direction:

PEOPLE AND PLACES
The promise is personal: the people who analyse a process are the people who build the fix, and they come to the factory and the building site. Lead with large, full-width photography of real working moments: an engineer and a foreman at a site table, a hand on a machine panel, a tablet used with work gloves, a street in Winterthur. Set text in calm, generous space beside or over the images, with strong contrast. Use a warm, confident page colour and a typeface with a human voice, such as a serif or a humanist sans. The feeling: a capable neighbour, not an agency.
```

### B. The tool itself

```text
Design a homepage for ketztek GmbH in Winterthur, Switzerland, in this direction:

THE TOOL ITSELF
ketztek builds working tools, so the homepage behaves like one. The first screen is a small, well-made instrument: the visitor picks a sector (Industry & Manufacturing or Construction) and the task that costs them time (quality reports, maintenance records, defect lists, site reporting, approvals by email). The page answers in plain words: which service fits and what ketztek would look at first, ending in the button "Book a free 30-minute call". The interface is the design: clear controls, satisfying states and one confident colour, like a modern piece of equipment rather than a software product. No dashboards, charts, data or software screenshots. Show the instrument in its default state and in one answered state.
```

### C. Colour and type

```text
Design a homepage for ketztek GmbH in Winterthur, Switzerland, in this direction:

COLOUR AND TYPE
Take the Swiss poster tradition, not the Swiss grid. Each section is one bold statement on a full-width field of strong, unexpected colour, set in very large type. Use two or three colours that no competitor uses. Shapes, if any, are big, simple and abstract, and not taken from the logo. Memorable at a glance and still calm to read: one idea per screen, plenty of space, body text at normal reading size. Pair a distinctive display typeface (not a condensed or expanded grotesque) with a quiet text face.
```

### D. Material and light (optional)

```text
Design a homepage for ketztek GmbH in Winterthur, Switzerland, in this direction:

MATERIAL AND LIGHT
Swiss precision manufacturing, shown as material. Use large close-up photography of surfaces from the clients' worlds: machined steel, poured concrete, timber formwork, a cable tray. Use a muted, premium palette drawn from those materials, a refined typeface and a lot of space. The feeling: quiet quality, like a Swiss toolmaker's catalogue, never luxury.
```

## Step 1: core brief

Paste this under the direction block.

```text
THE CLIENT
ketztek does process analysis, automation on Microsoft 365 and the Power Platform, and custom software for small and mid-sized industrial and construction companies. Its promise is honest sizing: "Sometimes the honest answer is two weeks of work, and we'll tell you that." The firm is young and small, and confident about it.

THE VISITOR
Plant, site and operations managers in German-speaking Switzerland. Practical, sceptical of consultants, allergic to hype. They read on a phone between site visits and decide on a desktop. In this market, professional means understatement and precision: concrete units such as "half an hour" and "two weeks", no superlatives, one calm next step.

STAND APART
Competitors use navy, bright blue, teal, neon green or orange; the fonts Inter, Manrope or Montserrat; dashboard and laptop mock-ups; stock photos of handshakes. Earlier ketztek concepts were technical drawings and documents on white paper in black and yellow. This concept must look like none of them.

BRAND
Use the uploaded logo (black "ketztek" with a yellow double z) as supplied, once, in the header on a light area. Never recolour it. On a dark or coloured area, show a white-letter version labelled "proposed logo variant". Its yellow #ebc34d may appear elsewhere only as one small accent. Choose the rest of the palette freely.

HONESTY
No client logos, reviews, case studies, figures, certificates or founding year. No invented names or quotes. Generated images are welcome as mood images: label each "Mood image, replaced by ketztek's own photo", and keep faces turned away or out of focus so nobody is taken for ketztek's team.

THE PAGE
Header with navigation, a "DE | EN" switch and a "Book a free 30-minute call" button. The first screen says what ketztek does, for whom and where. It carries the H1 "Find the process that costs you time, and fix it with the tools you already have." and shows the primary action on a phone without scrolling. Secondary action: "Send a message". Then, in an order that suits the concept: how we work (Map, Propose, Build, Teach), five services, two sectors (Industry & Manufacturing, Construction), why ketztek, a closing invitation ("Not sure where to start?") and a footer with the address, Impressum and Privacy. Leave room for German, which runs about 30 percent longer.

QUALITY
WCAG 2.2 AA contrast. Body text at least 17 px on phones and 18 px on desktop. Tap targets at least 44 px. Visible keyboard focus. No horizontal scrolling. No cookie banner. Avoid all-caps labels, middle-dot strings, numbering on things that are not a sequence, identical rounded cards with soft shadows, and a fade-in on every section.

Make the homepage at 1440 px and at 390 px. Name the concept and list its palette in hex.
```

## Step 2: copy

```text
Now put this copy into the homepage, word for word. Keep the layout, palette, type and images as they are. Change only the text, and add or remove a section only where the copy needs it. Add no new claims, numbers or names. In an interactive answer, use only the lines below.

Supporting line: "Analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland."

Problem: "Most inefficiency isn't a software problem. It's the recurring and repetitive tasks piling up in the background."

How we work: Map ("We start by tracking the root of the problem."). Propose ("Then we propose how to solve it. Often the solution is smaller, faster, and cheaper than you expected."). Build ("The people who map your process are the people who build the fix."). Teach ("Then we teach them to run it.")

Services: Process Analysis & Optimization ("We map your workflows end to end, work out where the time and money are going, and hand you a prioritized plan you can act on."). Automation & Digital Workflows ("Many bottlenecks disappear in weeks rather than months, using licences you already pay for."). Custom Software Engineering ("When standard tools reach their limit, we build."). Prototyping & Feasibility ("Before you commit a budget, find out whether the idea holds."). Workshops & Training ("We teach your team to get real value out of Microsoft 365 and the Power Platform.")

Sectors: Industry & Manufacturing ("Machine data nobody looks at. Quality reports assembled by hand. Maintenance that runs on experience because the records are incomplete. We connect what's already there and digitize what's still on paper."). Construction ("Site documentation spread across paper, Excel and messaging apps. Defect lists that never quite match the plan. We move site reporting onto something people will actually use with gloves on.")

Why ketztek: "We size the solution to the problem" ("Sometimes the honest answer is two weeks of work, and we'll tell you that."). "We work alongside you, not for you". "A small team with a deep bench". "Analysis and delivery from one team". "You keep what we build". "Swiss-based, on site when it matters" ("Process work can't be done over video calls alone. We come to the factory and to the building site.")

Closing: "Not sure where to start?" ("Most of our projects begin with one frustrating process. Tell us about yours. In half an hour, we'll give you an honest opinion on whether it's worth fixing and roughly what it would take, before any invoice exists.")

Footer: ketztek GmbH, Schulergasse 9, 8406 Winterthur, Switzerland. info@ketztek.ch. Impressum. Privacy.
```

## Step 3: German first screen

The H1 and button come from the demo and still need a native speaker's review. The supporting line and navigation are new drafts with the same status.

```text
Make one more phone screen at 390 px: the same first screen, in German, with the same design. Use Swiss spelling ("ss", never "ß") and «guillemets» for quotes. Do not shorten the text to fit; adjust the layout instead.

Navigation: Leistungen, Branchen, Über uns, Kontakt. Language switch: DE | EN.
H1: "Finden Sie den Ablauf, der Sie Zeit kostet, und lösen Sie ihn mit Ihren eigenen Werkzeugen."
Supporting line: "Analyse, Automatisierung und individuelle Software für Industrie- und Bauunternehmen. Mit Sitz in Winterthur, tätig in der ganzen Schweiz."
Primary action: "Kostenloses 30-Minuten-Gespräch buchen". Secondary action: "Nachricht senden".
```

## Checklist for comparing the results

This is for us, not for Stitch. Score each project yes or no.

| # | Question | How to check |
| --- | --- | --- |
| 1 | Is it outside the old family? | Nothing reads as paper, a document, a technical drawing, a hairline grid or a black-and-yellow page. |
| 2 | Is the next step on the first phone screen? | "Book a free 30-minute call" is visible at 390 x 844 without scrolling, in English and in German. |
| 3 | Does the German fit? | The German H1 and button fit without shrinking the type or breaking a word badly. |
| 4 | Would a Swiss plant manager trust it? | No hype, no invented proof, and nothing that looks like a template or a start-up landing page. |
| 5 | Does it stand apart from the competitors? | Open it beside KMUpower, PowerAlps and Stellar Automation: no shared colour, font or picture style. |
| 6 | Is the logo respected? | The logo is unchanged, appears once, and any white-letter variant is labelled. |
| 7 | Is it honest about images? | Every generated image is labelled as a mood image, and no face could pass for ketztek's team. |
| 8 | Is it readable and usable? | Body text is at least 17 px on the phone, contrast looks strong, and buttons look like buttons. |
| 9 | Is it buildable as a static site? | It needs no framework, video or 3D. Direction B's instrument is fine as a few lines of JavaScript. |
| 10 | Is it memorable? | After closing it, you can describe its one signature element in a sentence. |

A direction is worth taking forward only if it passes 1, 2, 4 and 6, and most of the rest.

## Changes from the first Stitch prompt

- Splits the run into three short steps (design, copy, German), each under 4,500 characters, so Stitch does not drop parts.
- Puts the direction first in every prompt.
- Cuts the excluded ideas to one line and describes the wanted look in positive terms, so the prompt does not repeat the old vocabulary.
- Runs one direction per Stitch project, so no shared design system pulls the concepts together.
- Assigns four directions outside the old family: people and places, an interactive tool, colour-field poster type, and material close-ups (optional).
- Allows generated mood images, labelled and without recognisable faces, instead of grey placeholder boxes.
- Frees the palette. Yellow and black stay in the logo, and a white-letter logo variant may sit on dark or coloured areas, labelled as proposed.
- Frees the page structure and order. The copy stays verbatim and claims stay limited to what ketztek has said.
- Tests the first phone screen in German.
- Adds a checklist for comparing the results.
