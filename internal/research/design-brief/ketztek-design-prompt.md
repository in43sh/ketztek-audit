# Design prompt: ketztek website

## 1. Your role and the job

You are designing a completely new website for ketztek GmbH, a small Winterthur firm that finds where industrial and construction companies lose time to manual processes and fixes them with automation on Microsoft 365 and the Power Platform, or custom software. The site's one job: a plant, site or operations manager understands within seconds what ketztek does, trusts it to size the work honestly, and books a free 30-minute call. Design Home, the service page "Automation & Digital Workflows", Contact, the phone menu and the footer, from 320 to 1440 px. It must feel made from its visitors' own work reports, checklists and sites, not from a consultancy template.

## 2. The business

- ketztek GmbH, Schulergasse 9, 8406 Winterthur, Switzerland. Email `info@ketztek.ch`. `[[supply: phone number and office hours, if they should be public]]`
- Works across Switzerland and on site: at the factory and on the building site.
- Clients: industrial and manufacturing companies, and construction companies.
- Services: Process Analysis & Optimization; Automation & Digital Workflows (Microsoft 365, Power Platform); Custom Software Engineering; Prototyping & Feasibility (including AR/VR pilots); Workshops & Training.
- Technologies: software engineering, AI, cloud (Microsoft Azure), Microsoft 365, Microsoft Power Platform, augmented and virtual reality.
- Way of working: sizes the solution to the problem, works alongside the client's people and teaches them, a small core team with a network of specialists, analysis and delivery by the same people, the client keeps documented code.
- First step for a client: a free 30-minute call, booked through Microsoft Bookings, or a written message.
- The firm is young and has no published reviews, case studies or certifications yet. Do not imply any.

## 3. Who the site is for

1. A plant, maintenance, site or operations manager (or owner) of a Swiss industrial or construction SME arrives, often on a phone between site visits, with one process that eats time.
2. They need to see at once that ketztek fixes slow processes in industry and construction, honestly sized, often with tools they already own.
3. They should book the free 30-minute call, or write a short message.

Their doubts, and what answers each:

- Big enough to rely on? The small team plus specialist network; `[[supply: team roles and photos]]`.
- Will they upsell? "Sometimes the honest answer is two weeks of work, and we'll tell you that."
- Cost? The first call is free; `[[supply: price cue, if wanted]]`.
- Do they know my site or machines? The sector texts; `[[supply: own photos from sites and factories]]`.
- What happens next? What the 30 minutes cover; `[[supply: reply time for messages]]`.

Languages: German first, English second, as separate pages. Only English copy exists today, so build the prototype in English, and make every heading, button and label hold the German drafts in this prompt (German runs about 30% longer). Use Swiss German spelling: "ss", never "ß".

## 4. What the site must say

**Core message:** ketztek finds the process that costs you time and fixes it, often with the software you already own, sized honestly.

**Supporting messages:**

1. Most inefficiency is not a software problem; it is recurring, repetitive work piling up in the background.
2. We start with one frustrating process and tell you honestly whether it is worth fixing, before any invoice exists.
3. Often the fix is smaller, faster and cheaper than expected, using licences you already pay for.
4. We work on site, with your people, and teach them to run what we build.
5. You keep what we build: documented, with a handover your own IT can pick up.

**Tone:** plain, concrete, a little dry, never salesy. Two lines that set it: "Sometimes the honest answer is two weeks of work, and we'll tell you that." and "…everything currently held together by one critical Excel file and the person who understands it."

**Use:** process, report, checklist, defect list, maintenance record, site documentation, on paper, Excel, gloves, factory, building site, half an hour, honest. In German: Ablauf, Rapport, Mängelliste, Wartungsprotokoll, Baustelle, Vorlage.

**Avoid:** seamless, innovative, cutting-edge, digital transformation, solutions (as a noun on its own), "Making your business run smoother", any number, client name, award or guarantee that is not supplied.

## 5. Design direction: "Rapport"

**Idea.** The site reads like a well-kept work report, filled in with the visitor's own problem. Plant and site managers live with Regierapporte, Mängellisten and Wartungsprotokolle, and search for templates of them; ketztek turns those paper and Excel templates into tools people use. Borrow the clarity of a good printed report, not its clutter.

**Palette.** Use exactly these colors:

| Name | Hex | Role | Contrast |
| --- | --- | --- | --- |
| Ink | `#000000` | All text, important rules, the logo's black | 21:1 on Paper, 18.06:1 on Desk |
| Paper | `#ffffff` | Report sheets and content surfaces | |
| Desk | `#eeeeeb` | Page background behind the sheets | |
| Field line | `#6b6b66` | Input borders and form rules | 5.36:1 on Paper (interface) |
| Ruling | `#b9b9b3` | Decorative ruled lines inside the report block only | decoration |
| Note | `#55554f` | Secondary text | 7.5:1 on Paper, 6.46:1 on Desk |
| Marker | `#e8c048` | The logo's yellow: primary button fill (Ink text) and the "Next step" field | Ink on Marker 12.06:1 |
| Error | `#b42318` | Form error text and borders | 6.57:1 on Paper |

Marker is never used for text and never on Desk as a text background (1.5:1). It appears in at most two places per screen: the primary button and the "Next step" field.

**Type.** One family, Archivo, from Google Fonts (variable axes `wdth` 62-125 and `wght` 100-900). Download the WOFF2 files and serve them from the site's own folder with `@font-face`; never link to `fonts.googleapis.com`, which sends every visitor's IP address to Google. If you cannot download the files, use the fallback stack below. Headlines: `wdth` 112, `wght` 700, line height 1.1. Body: `wdth` 100, `wght` 400, line height 1.5. Field labels in the report block and form labels: `wdth` 75, `wght` 500, sentence case. Fallback stack: `system-ui, -apple-system, "Segoe UI", Roboto, Arial, sans-serif`.

Type scale (px), phone / desktop: H1 36 / 52; H2 28 / 36; H3 22 / 26; body 17 / 18; small and labels 15 / 15. Never below 15 px.

**Layout principles.**

- One left-aligned text column, at most 680 px wide (about 70 characters), sharing its left edge with the logo on every page. 20 px side margins on phones, 40 px on tablets, a centred 1200 px frame on desktop.
- Content that belongs together sits on a white sheet on the Desk background; sheets have a 2 px radius and no shadow, or a 1 px Ruling outline. Space between sheets: 48 px on phones, 80 px on desktop. Inside a sheet: 24 px.
- Ruled lines appear only in the report block, forms and ruled lists. Everything else is separated by space.
- All text is left-aligned. The only centred element allowed is the closing call-to-action block.
- Lists of services, reasons and steps are ruled lists, not cards.

**Signature element: the work report.** On the first screen of Home, a white sheet titled "Work report" holds three ruled fields, set like a printed form:

```text
Work report
Process     Quality reports
Today       assembled by hand
Next step   [ Book a free 30-minute call ]   <- the real primary button, Marker fill
```

The values are printed text taken from the site's own copy, not input boxes; the only interactive element in it is the real button. On the service page, the same block names that service's typical process (see section 7). Use it once per page, no more.

First screen at 390 px and 1440 px:

```text
390 px                             1440 px
+------------------------------+   +--------------------------------------------------------------+
| ketztek              [menu]  |   | ketztek   Services  Sectors  About  Contact  DE|EN  [Book a call] |
|------------------------------|   |--------------------------------------------------------------|
| H1: Find the process that    |   | H1: Find the process that costs   +------------------------+ |
| costs you time, and fix it   |   | you time, and fix it with the     | Work report            | |
| with the tools you already   |   | tools you already have.           | Process    Quality     | |
| have.                        |   | Analysis, automation, software.   |            reports     | |
| Winterthur, on site in CH.   |   | Winterthur, on site in CH.        | Today      assembled   | |
| +--------------------------+ |   | Send a message (text link)        |            by hand     | |
| | Work report              | |   |                                   | Next step [Book a free | |
| | Process    Quality       | |   |                                   |  30-minute call]       | |
| |            reports       | |   |                                   +------------------------+ |
| | Today      assembled     | |   +--------------------------------------------------------------+
| |            by hand       | |
| | Next step [Book a free   | |
| |  30-minute call]         | |
| +--------------------------+ |
+------------------------------+
```

**Imagery.** No photographs at launch and never stock photographs. Own photos, when supplied, appear as "attachments" to a sheet with a one-line caption set like a field. No icons in the services list.

**Motion.** At most one: the Marker fill draws in under "Next step" on first load (300 ms, once, off under `prefers-reduced-motion`).

**Do not drift into:** a newspaper or spreadsheet look, a beige "warm paper" look, or a form the visitor thinks they must fill in.

## 6. Fixed brand elements

- Wordmark: `assets/logo-wordmark.png` (667 x 185 px, transparent PNG; black wordmark with the yellow double "z"). Header height 32 px on phones, 36 px on desktop. Keep clear space equal to the height of the "z" on all sides. `[[supply: SVG or PDF of the logo; replace the PNG when it arrives]]`
- Icon: `assets/logo-icon-270.png` (270 x 270 px, the yellow double "z" alone). Use for the favicon and touch icon only.
- Logo colors: black `#000000`, yellow `#e8c048` (sampled from the files; `[[supply: confirm the official yellow]]`).
- Show the logo once per screen. Never repeat it large in the hero.
- Required in the footer: Impressum and Privacy pages.

## 7. Pages and sections

Sitemap: Home; Services (one page per service; design "Automation & Digital Workflows"); Sectors (sections on Home for now); About `[[supply: team by role]]`; Contact; Impressum; Privacy. German pages under `/de/` mirror the English ones.

Marking used below: plain text in quotes is the business's existing copy, use it verbatim; `[[draft]]` is new wording built only from facts in this prompt, for the business to approve; `[[draft, native review]]` is German wording a native speaker must check; `[[supply: ...]]` is content only the business can provide.

### Home

1. **Header.** Wordmark left; on desktop the links Services, Sectors, About, Contact, the language switch "DE | EN", and a small primary button "Book a call" `[[draft]]`. On phones: wordmark, then the menu button (44 x 44 px); the language switch lives inside the phone menu.
2. **First screen.** H1 "Find the process that costs you time, and fix it with the tools you already have." `[[draft]]` (German: "Finden Sie den Ablauf, der Sie Zeit kostet, und lösen Sie ihn mit den Werkzeugen, die Sie schon haben." `[[draft, native review]]`). Supporting line: "Analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland." (adapted from "We offer analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland."). Then the work-report block with the primary button "Book a free 30-minute call" (German: "Kostenloses 30-Minuten-Gespräch buchen" `[[draft, native review]]`). Secondary text link: "Send a message" `[[draft]]`. Purpose: say what, for whom and where, and offer the next step.
3. **The problem.** H2 "Start with your processes." Text: "Most inefficiency isn't a software problem. It's the recurring and repetitive tasks piling up in the background." Purpose: name the visitor's real pain.
4. **How it works.** H2 "How a project starts" `[[draft]]`. A numbered, ruled list of four steps (a real sequence): 1 Map ("We start by tracking the root of the problem."), 2 Propose ("Then we propose how to solve it. Often the solution is smaller, faster, and cheaper than you expected."), 3 Build ("The people who map your process are the people who build the fix."), 4 Teach ("Then we teach them to run it."). Purpose: make the engagement feel small and safe.
5. **Services.** H2 "What we offer". A ruled list of the five services, each with its name, one line, and a link "More" `[[draft]]` to its page:
   - Process Analysis & Optimization: "We map your workflows end to end, work out where the time and money are going, and hand you a prioritized plan you can act on."
   - Automation & Digital Workflows: "Many bottlenecks disappear in weeks rather than months, using licences you already pay for."
   - Custom Software Engineering: "When standard tools reach their limit, we build."
   - Prototyping & Feasibility: "Before you commit a budget, find out whether the idea holds."
   - Workshops & Training: "We teach your team to get real value out of Microsoft 365 and the Power Platform."
6. **Sectors.** Two sheets side by side on desktop, stacked on phones. "Industry & Manufacturing": "Machine data nobody looks at. Quality reports assembled by hand. Maintenance that runs on experience because the records are incomplete. We connect what's already there and digitize what's still on paper." "Construction": "Site documentation spread across paper, Excel and messaging apps. Defect lists that never quite match the plan. We move site reporting onto something people will actually use with gloves on." Each may hold one attachment photo `[[supply: own photo, factory / building site]]`; the layout must also work without it.
7. **Proof.** H2 "Work we've done" `[[draft]]`. Room for two or three short case stories as report sheets (client type and region, the process, what changed) `[[supply: two or three projects, anonymised if needed, with a result]]`. If none are supplied, the section is hidden; design both states.
8. **Why us.** H2 "Why work with us". A ruled list of the six reasons with their existing headings and one-line texts: "We size the solution to the problem" (end on "Sometimes the honest answer is two weeks of work, and we'll tell you that."); "We work alongside you, not for you"; "A small team with a deep bench"; "Analysis and delivery from one team"; "You keep what we build"; "Swiss-based, on site when it matters".
9. **Closing.** The one centred block: H2 "Not sure where to start?" Text: "Most of our projects begin with one frustrating process. Tell us about yours. In half an hour, we'll give you an honest opinion on whether it's worth fixing and roughly what it would take — before any invoice exists." Primary button "Book a free 30-minute call", secondary link "Send a message" `[[draft]]`.
10. **Footer.** See section 8.

### Service page: Automation & Digital Workflows

1. Header as on Home, "Services" marked as the current section.
2. **First screen.** H1 "Automation with the licences you already pay for" `[[draft]]`. Text: "Many bottlenecks disappear in weeks rather than months, using licences you already pay for. We build automated workflows, apps and dashboards on Microsoft 365 and the Power Platform." Work-report block: Process "Approvals and inspections" / Today "held together by one critical Excel file" / Next step: the primary button.
3. **Where it fits.** H2 "Where it fits" `[[draft]]`. Text: "Power Apps, Power Automate and Power BI let us deliver working tools in weeks at a fraction of custom-build cost. The natural fit for approvals, inspections, checklists, maintenance records and reporting — and for everything currently held together by one critical Excel file and the person who understands it." Then a ruled list: approvals, inspections, checklists, maintenance records, reporting.
4. **Microsoft 365 as the backbone.** Text: "You almost certainly own more capability than you're using. We turn Teams, SharePoint and the surrounding services into a working operational backbone: structured document handling, collaboration that no longer depends on email attachments, and enough governance to keep it tidy two years from now."
5. **How a project runs.** The same four steps as on Home, shortened.
6. **Proof.** One case story sheet `[[supply: one automation project with its result]]`; hidden if none.
7. **Closing** as on Home.

### Contact

1. **First screen.** H1 "Let's talk about the process that annoys you most". Text: "There are two easy ways to start, and neither costs you anything." Two sheets, side by side on desktop, stacked on phones with the booking sheet first.
2. **Book a call (sheet).** H2 "Book a call". Text: "Half an hour is usually enough for us to tell you whether there's something worth doing, roughly what it would involve, and whether we're the right people for it. No preparation needed." Primary button "Book a free 30-minute call", opening the Microsoft Bookings free-consultation page in a new tab, with "(opens Microsoft Bookings)" `[[draft]]` in Note color under it. `[[supply: direct link to the free consultation service]]`. No embedded calendar frame.
3. **Write to us (sheet).** H2 "Write to us". Text: "Prefer to type a few sentences first and see who answers? That works too. Tell us roughly what's going on and we'll come back to you with a real answer, not a brochure." Form: Name (required), E-mail (required), Company (optional), Message (required, up to 2,000 characters with a counter). Required fields marked "required" `[[draft]]` in the label. Button "Send message" `[[draft]]` in the primary style. Under the form: "We reply within `[[supply: reply time]]`." `[[draft]]` and a link to the privacy page.
4. **Address sheet.** ketztek GmbH, Schulergasse 9, 8406 Winterthur; `info@ketztek.ch`; `[[supply: phone and hours]]`.

## 8. Components and states

- **Phone menu.** Full-screen Paper sheet: 22 px links in 56 px rows, current page in bold with a 4 px Marker bar, the language switch, the primary button at the bottom. Open and close buttons 44 x 44 px, nothing on top of them; Escape closes it; focus moves into it.
- **Desktop navigation.** Current page: Ink text with a 2 px Ink underline. Hover: 2 px underline. Focus: 2 px Ink outline, 2 px offset.
- **Primary button.** Marker fill, Ink text, Archivo 600, 17 px, 48 px tall, 4 px radius, no shadow. Hover: Ink fill, Marker text (12.06:1). Focus: 2 px Ink outline, 2 px offset. Disabled: Desk fill, Note text.
- **Secondary action.** A text link with a 1 px underline (2 px on hover), never a second filled button next to the primary.
- **Links in text.** Ink, underlined.
- **Ruled list.** Rows with a 1 px Ruling line above and 16 px padding; the label left of the text on desktop, above it on phones.
- **Work-report block.** White sheet, title "Work report" `[[draft]]` in the field-label style, three rows on 1 px Ruling lines, "Next step" row with a Marker band behind the button area.
- **Form fields.** 48 px tall, 1 px Field line border, 4 px radius, full width of the sheet (`width: 100%`, `box-sizing: border-box`), labels above. Focus: 2 px Ink border. Error: 2 px Error border, an error message under the field in Error color starting with what to do ("Enter an email address like <name@company.ch>" `[[draft]]`). Success: the form is replaced by a confirmation sheet "Thanks. We'll reply within `[[supply: reply time]]`." `[[draft]]`.
- **Footer.** Paper background with a 1 px Ruling line above. Address and email; links to Book a call, Contact, Impressum, Privacy; language switch. Every link at least 44 px tall.
- **404 page.** H1 "This page doesn't exist" `[[draft]]`, one line, and two links: Home and "Book a free 30-minute call".

## 9. Requirements

- WCAG 2.2 AA: text 4.5:1 (3:1 at 24 px and up), interface 3:1, visible focus on every control, reflow at 320 px, no motion under `prefers-reduced-motion`.
- Tap targets 44 x 44 px for the menu button, buttons, form fields and footer links; 24 x 24 px for anything else.
- Body text 17 px on phones, 18 px on desktop; lines at most 75 characters; one H1 per page, headings in order.
- The H1 and "Book a free 30-minute call" visible without scrolling at 390 and 1440 px on all three pages.
- Nothing wider than the viewport at 320, 360, 390, 768, 1024 and 1440 px.
- Archivo only, self-hosted WOFF2, `font-display: swap`, weights 400, 500, 600 and 700; no request to `fonts.googleapis.com` or `fonts.gstatic.com`.
- LCP 2.5 s or less and layout shift 0.1 or less on a mid-range phone; every image with fixed width and height.
- Headings, buttons and labels hold the German drafts without breaking.
- Texts, case stories and contact details are separate editable blocks; contact details come from one source.
- No consent banner unless tracking is added later.

## 10. Do not

1. Put anything on top of the phone menu button, or use menu links that only work on one page.
2. Leave a button or link without a working destination.
3. Open with the logo, a slogan or a texture instead of the offer and the booking button, or show the logo twice.
4. Let text touch the screen edge, run lines over 75 characters, or switch alignment between left, centre and right.
5. Add a second accent: no purple, blue, teal or green (5 of 7 competitors are cool blue or green).
6. Use stock photos, device mock-ups, floating dashboard cards or gradients (4 of 7 competitors open on photo or video, 2 on blue gradients).
7. Style the secondary action like the primary one, or leave the form button unstyled.
8. Embed the booking calendar on phones, or build a machine-translation language switch.
9. Use ALL-CAPS eyebrows, middle-dot meta strings, arrows on every button, one recolored headline word, monospace labels, numbering on non-sequences, identical shadowed cards, fade-ins on every section, cream-serif-terracotta or dark-with-neon looks.
10. Invent client names, figures, quotes, certifications, prices, years or photos, or copy any competitor's layout, copy or imagery.

## 11. Deliverables

- Static HTML and CSS for Home, the service page "Automation & Digital Workflows", Contact, the phone menu state and the 404 page, responsive from 320 to 1440 px.
- CSS custom properties for every color, font size, space and radius in this prompt; no hard-coded values outside them.
- Real copy as given, with every `[[draft]]` and `[[supply: ...]]` marker visible in the page (for example in a dashed Note-colored box), so the business can see what is missing.
- Screenshots of each page at 390 px and 1440 px, first screen and full page, plus the phone menu open.
- A short note listing each acceptance check (section 13) with pass or fail and how you checked it.

## 12. Process

1. **Plan.** Write the token sheet and sketch each first screen at 390 and 1440 px. Check it against sections 3, 5 and 10; revise anything that would look at home on a competitor's site, and say what changed.
2. **Build** phone-first: Home, then Contact, then the service page.
3. **Check** the screenshots against section 13, fix what fails, repeat once.

## 13. Acceptance checks

1. At 390 px and at 1440 px, the H1 and the "Book a free 30-minute call" button are visible without scrolling on Home, the service page and Contact.
2. The logo appears exactly once on each first screen.
3. The phone menu opens with a tap at the centre of its button at 360 px and 390 px, and closes with its close button and Escape.
4. Every link and button has a working destination or action; the booking buttons open Microsoft Bookings in a new tab.
5. Body text is at least 17 px at 390 px and 18 px at 1440 px.
6. No line of running text exceeds 75 characters at 1440 px.
7. Every text and background pairing meets the contrast in section 5; Marker is never a text color.
8. No page scrolls sideways at 320, 360, 390, 768, 1024 or 1440 px, including Contact with its form.
9. All text is left-aligned except the closing block.
10. Every interactive element shows a visible focus outline when reached by Tab, in a logical order.
11. Tap targets for the menu button, buttons, form fields and footer links are at least 44 x 44 px.
12. Only the palette in section 5 is used; there is no purple, blue, teal or green.
13. No stock photograph, device mock-up, gradient or card-with-shadow appears.
14. The work-report block appears once per page and contains exactly one interactive element, the primary button.
15. With the German drafts swapped in, no heading or button breaks its layout.
16. Under `prefers-reduced-motion: reduce`, nothing animates.
17. Every `[[draft]]` and `[[supply: ...]]` marker from this prompt is visible on the page or listed in the note.

## 14. Appendix

### Assets

| Local path | Source | Format and size | Use |
| --- | --- | --- | --- |
| `assets/logo-wordmark.png` | `https://ketztek.com/wp-content/uploads/2026/07/4.1-no-bg_cropped.png` | PNG, 667 x 185, transparent | Header and footer logo |
| `assets/logo-icon-270.png` | `https://ketztek.com/wp-content/uploads/2026/07/cropped-6.1-no-bg-270x270.png` | PNG, 270 x 270, transparent | Favicon, touch icon |
| Font | Archivo on Google Fonts (download only, `wdth` 62-125, `wght` 100-900) | Variable WOFF2, self-hosted | All text |

### Copy bank (verbatim)

- "Most inefficiency isn't a software problem. It's the recurring and repetitive tasks piling up in the background."
- "We offer analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland."
- "We start by tracking the root of the problem. Then we propose how to solve it. Often the solution is smaller, faster, and cheaper than you expected."
- "Get the best out of the software you already own." / "Often that means you need less new software, not more."
- The five service descriptions and the two sector texts, as quoted in section 7.
- "Sometimes the honest answer is two weeks of work, and we'll tell you that."
- "We sit with your people, learn how they actually work, and build with them rather than at them. Then we teach them to run it."
- "Documented code, clean architecture, and a handover your own IT can pick up. No lock-in by obscurity."
- "Process work can't be done over video calls alone. We come to the factory and to the building site."
- "Most of our projects begin with one frustrating process. Tell us about yours. In half an hour, we'll give you an honest opinion on whether it's worth fixing and roughly what it would take — before any invoice exists."
- "Let's talk about the process that annoys you most" / "There are two easy ways to start, and neither costs you anything."
- The Contact texts for "Write to us" and "Book a call", as quoted in section 7.

### Placeholders to be supplied

1. Phone number and office hours, if public.
2. Reply time for messages.
3. Direct link to the free-consultation service in Microsoft Bookings.
4. SVG or PDF logo; confirmation of the official yellow.
5. Team by role, with photos if they may be shown.
6. Two or three case stories (one for automation), anonymised if needed, with results.
7. Own photos from factories and building sites (landscape).
8. A price cue or typical project size, if they want to show one.
9. German copy for every page.

### Draft lines to approve

1. H1 "Find the process that costs you time, and fix it with the tools you already have." / German draft (native review).
2. "Analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland." (adapted from existing copy).
3. Button "Book a free 30-minute call" (German draft "Kostenloses 30-Minuten-Gespräch buchen", native review); header button "Book a call".
4. "Send a message"; "Send message"; "More".
5. "Work report", "Process", "Today", "Next step" (German drafts "Arbeitsrapport", "Ablauf", "Heute", "Nächster Schritt", native review).
6. Section titles "How a project starts", "Work we've done", "Where it fits".
7. Service-page H1 "Automation with the licences you already pay for"; work-report values "Approvals and inspections" / "held together by one critical Excel file".
8. Form texts: "required", the error example, the confirmation, "(opens Microsoft Bookings)", "We reply within …".
9. 404 H1 "This page doesn't exist".

## 15. Short version

Design a new website for ketztek GmbH, a small Winterthur firm that finds where industrial and construction companies lose time to manual processes and fixes them with Microsoft 365, the Power Platform or custom software, sized honestly. Visitors are plant, site and operations managers, often on phones; they must see the offer and a "Book a free 30-minute call" button on the first screen. Pages: Home, the service page "Automation & Digital Workflows", Contact, phone menu, footer; 390 to 1440 px.

Direction "Rapport": the site reads like a well-kept work report. White sheets (`#ffffff`) on a neutral grey page (`#eeeeeb`), Ink `#000000` text, the logo's yellow `#e8c048` only as the primary button fill (with black text) and one "Next step" field. Type: Archivo (self-hosted WOFF2 from Google Fonts), wide and bold for headlines, normal for body (17 px minimum on phones), narrow for labels. Signature: a "Work report" block on the first screen with ruled fields "Process / Today / Next step", the last holding the real booking button. Everything left-aligned, ruled lists instead of cards.

Do not: use stock photos, gradients, mock-ups or cards with shadows; add blue, teal, green or purple; put anything over the phone menu button; show the logo twice; invent clients, numbers or claims (use `[[supply: ...]]` placeholders).
