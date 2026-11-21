# ketztek GmbH: Design Research for a New Website

Run of `prompts/design-brief-prompt.md` on Saturday 2026-11-21 (Europe/Zurich). Readings 2026-11-21 10:32Z-12:07Z UTC. Internal file; the design prompt is [ketztek-design-prompt.md](ketztek-design-prompt.md).

| Input | Value used |
| --- | --- |
| Business | ketztek GmbH, Schulergasse 9, 8406 Winterthur, Switzerland |
| Current website | [ketztek.com](https://ketztek.com/) |
| Prior reports | Presence audit (2026-11-20), design audit and UX audit (2026-11-21) in this repository, read for facts, assets, failures and competitors only |
| What changes | Everything except the name and the logo |
| Target design tool | Coding agent building static HTML and CSS (default) |
| Pages | Home, one service page (Automation & Digital Workflows), Contact, phone menu, footer |
| Asset files | Logo only (default) |
| Competitors | Seven from the presence audit's list |
| Benchmarks | None |

Capabilities: `curl`, Node with Playwright and a full Chromium build, Python, the harness web search (leads only), the search engine's public suggestion endpoint. Languages read: English and German (not native German; German drafts are marked for native review).

Labels: `[FACT]` read on a source in this run or a prior report (date given), `[INFERENCE]` follows from facts (step stated), `[UNVERIFIED]` not confirmed.

## 1. Summary

ketztek is a young Winterthur GmbH that analyses, automates and builds software for industrial and construction companies, mostly with Microsoft 365 and the Power Platform, plus custom code. Its visitors are plant, site and operations managers at Swiss SMEs, mostly German-speaking, who want to know fast whether this small firm can fix one slow process, and then book the free 30-minute call.

**Recommended direction: "Rapport".** The site reads like a well-kept work report, the one document these managers already trust. It is text-led, so it can be built now from the existing copy, and the primary action sits inside its signature element. None of the seven competitors uses anything like it: 5 of 7 use cool blue, teal or green accents, and 4 of 7 open on a photo or video.

**Biggest content gaps:** any proof (case stories, client quotes, certifications, reviews), own photography, German copy, a phone number and hours, a response time, the team by role.

**Section 0.1:** no challenge. The logo's yellow and black carry all three directions.

## 2. Business and offer

| Fact | Source |
| --- | --- |
| [FACT] Offers "analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland." | [Home](https://ketztek.com/), 2026-11-21 10:32Z |
| [FACT] Five services: Process Analysis & Optimization; Automation & Digital Workflows (Microsoft 365, Power Platform); Custom Software Engineering; Prototyping & Feasibility (incl. AR/VR pilots); Workshops & Training | Home |
| [FACT] Two sectors: Industry & Manufacturing; Construction | Home |
| [FACT] Six technologies: Software Engineering, Artificial Intelligence, Cloud (Azure), Microsoft 365, Microsoft Power Platform, Augmented & Virtual Reality | [Expertise](https://ketztek.com/expertise/), 10:32Z |
| [FACT] Entry offer: a free 30-minute call, booked through Microsoft Bookings; the booking page lists "Demo Software", "Coffee Chat / Kennenlerngespräch", "Free Initial Consultation / Kostenloses Erstgespräch" and a one-hour M365 and Power Platform demo | Home; booking page read 10:34Z; UX audit |
| [FACT] Address Schulergasse 9, 8406 Winterthur; email `info@ketztek.ch`; no phone number on the site (0 `tel:` links) | Home and Contact footer, 10:32Z |
| [FACT] Commercial register status active (UID CHE-295.462.558); domain registered 2025-11-07 | Presence audit, 2026-11-20 |
| [FACT] 0 Google reviews; no case studies, client names, certifications or press on the site | Presence audit (F-05, F-07) |
| [FACT] Stated differentiators: sizes the solution to the problem ("Sometimes the honest answer is two weeks of work"); works alongside the client's people and teaches them; small core team plus a specialist network; analysis and delivery from one team; client keeps the code; on site at the factory and building site | Home, "Why work with us" |
| [INFERENCE] The honest-sizing stance is the strongest differentiator: no competitor home page read states it (from the seven fingerprints and screenshots) | 3.6 |

## 3. Audience and journeys

**Who arrives:** [INFERENCE] operations, plant, maintenance and site managers or owners of Swiss industrial and construction SMEs. Basis: the sector copy addresses "machine data", "maintenance", "site documentation" and "defect lists"; search suggestions in Switzerland centre on these documents (below).

**Device and context:** [INFERENCE] often a phone between site visits, then a desk computer to decide. Basis: the home copy's "something people will actually use with gloves on" and on-site work.

**Language:** [FACT] All 7 competitors' home pages are in German (`lang` de or de-CH). [FACT] All 25 German suggestion seeds returned Swiss-German work vocabulary (for example "regierapport vorlage excel"); the 3 English seeds returned generic results such as "process automation engineer" (2026-11-21 11:59Z). [FACT] The current site is English only. [INFERENCE] German first, English second.

**First ten seconds:**

1. A plant or site manager with one process that eats time arrives from a search or a referral.
2. They need to see that ketztek fixes slow processes in industry and construction, honestly sized, with tools they may already own.
3. They should book the free 30-minute call, or write a short message.

**Doubts and answers:**

| Doubt | What answers it |
| --- | --- |
| "Is this firm big enough to rely on?" | Small team plus specialist network (copy), named roles `[[supply]]`, proof `[[supply]]` |
| "Will they sell me a big project?" | "Sometimes the honest answer is two weeks of work" (copy) |
| "What does it cost?" | Free first call (copy); price cues `[[supply]]` |
| "Do they understand my site or my machines?" | Sector copy in the visitors' own terms; own photos `[[supply]]` |
| "What happens after I book?" | What the 30 minutes cover (copy); response time `[[supply]]` |

**Journeys:**

1. **Phone, from search:** lands on Home, reads the headline and the work-report block, taps "Book a free 30-minute call", picks the free consultation in Microsoft Bookings.
2. **Desk, comparing:** reads services and sectors, opens the service page, checks proof and "Why us", books or writes.
3. **Prefers to write:** opens Contact, sends name, email and a short message, expects a reply time.

## 4. Content inventory

**Copy bank (verbatim, Home, Expertise and Contact, 10:32Z).** Strong lines, specific and in the visitor's language:

| Topic | Line |
| --- | --- |
| Problem | "Most inefficiency isn't a software problem. It's the recurring and repetitive tasks piling up in the background." |
| Offer | "We offer analysis, automation, and custom software for industrial and construction companies. Based in Winterthur, working across Switzerland." |
| Method | "We start by tracking the root of the problem. Then we propose how to solve it. Often the solution is smaller, faster, and cheaper than you expected." |
| Tools | "Get the best out of the software you already own." / "Often that means you need less new software, not more." |
| Industry | "Machine data nobody looks at. Quality reports assembled by hand. Maintenance that runs on experience because the records are incomplete. We connect what's already there and digitize what's still on paper." |
| Construction | "Site documentation spread across paper, Excel and messaging apps. Defect lists that never quite match the plan. We move site reporting onto something people will actually use with gloves on." |
| Power Platform | "…everything currently held together by one critical Excel file and the person who understands it." |
| Honesty | "Sometimes the honest answer is two weeks of work, and we'll tell you that." |
| Working style | "We sit with your people, learn how they actually work, and build with them rather than at them. Then we teach them to run it." |
| Handover | "Documented code, clean architecture, and a handover your own IT can pick up. No lock-in by obscurity." |
| On site | "Process work can't be done over video calls alone. We come to the factory and to the building site." |
| Entry | "Most of our projects begin with one frustrating process. Tell us about yours. In half an hour, we'll give you an honest opinion on whether it's worth fixing and roughly what it would take — before any invoice exists." |
| Contact | "Let's talk about the process that annoys you most" / "There are two easy ways to start, and neither costs you anything." |

Filler, not to reuse as headlines: "Making your business run smoother.", "Seamlessly connect your digital tools.", "Make your tools work for you."

**Missing content (each a placeholder in the design prompt):** two or three case stories; client quotes; certifications or partner status; team by role with photos; price cues or typical project size; phone number and hours; reply time for messages; German copy for every page; own photographs; a privacy text for the new site (the current one is pasted from an old builder, F-11).

**Required pages:** Impressum (Swiss practice; the current site has one) and a privacy page. No legal advice.

## 5. Brand assets

| Asset | File | Source | Size | Colors (sampled in browser canvas, 8-step rounding) |
| --- | --- | --- | --- | --- |
| Wordmark (sampled 12:06Z) | `assets/logo-wordmark.png` | [4.1-no-bg_cropped.png](https://ketztek.com/wp-content/uploads/2026/07/4.1-no-bg_cropped.png) | 667 x 185 PNG, transparent | `#000000` 69.3%, `#e8c048` 30.7% |
| Icon (double "z", sampled 12:00Z) | `assets/logo-icon-270.png` | [cropped-6.1-no-bg-270x270.png](https://ketztek.com/wp-content/uploads/2026/07/cropped-6.1-no-bg-270x270.png) | 270 x 270 PNG, transparent | `#e8c048` 100% |

- [FACT] No vector logo is published (no SVG referenced in the page). `[[supply: SVG or PDF logo]]`.
- [FACT] Current fonts Inter and Instrument Sans, current sand `#ebe6d8` and an off-brand purple `#9b51e0`: reference only, not constraints (design audit).
- [FACT] Photography on Home: two Pexels stock images (`pexels-diva-29035509`, `pexels-anntarazevich-5963134`), one `construction.jpg` of unknown origin, five purple icon PNGs. No own photo of the team, premises or work. `[UNVERIFIED]` whether `construction.jpg` is the business's own.
- **Must survive:** the wordmark and icon, the Impressum content, the Microsoft Bookings link.

## 6. Category landscape

Home pages at 390 and 1440 px with the Appendix A script, 2026-11-21 11:58Z-12:01Z (full Chromium); `robots.txt` read first for each (IOZ and ketztek ask for a 10 s delay, kept). Script readings are measured; the columns marked (s) are read from the first-screen screenshots.

| Site | Fonts | Accent (s) | First screen (s) | Call to action on phone first screen (s) | H1 on first screen | Consent banner on phone |
| --- | --- | --- | --- | --- | --- | --- |
| [evolyze](https://www.evolyze.ch/) | Manrope | navy `#162b3e` | split: headline beside a dark meeting video | none (scroll arrow) | yes | none |
| [Theia Solutions](https://theiasolutions.ch/) | Montserrat | blue-teal gradient | gradient with floating dashboard mock-ups, caps eyebrow, gradient-colored word | two buttons | yes | 15% |
| [PowerAlps](https://www.poweralps.ch/) | Clash Display, Wix Madefor | green `#0ce696` on dark | full dark tech photo or video, check bullets | none | yes | none |
| [Stellar Automation](https://www.stellar-automation.ch/) | Inter, Satoshi | blue `#007ee5` | centered headline on abstract blue streaks | one (free process check) | yes | small notice |
| [KMUpower](https://kmupower.com/) | system sans | teal `#0b6e6d` | split: text beside a real flow screenshot | one (book a call) | yes | 25% |
| [IOZ](https://www.ioz.ch/) | Maven Pro | orange `#ea6212` | orange band, staff photo, AI search box, client logos | none (search box) | yes | 21% |
| [Noser Engineering](https://www.noser.com/) | Trade Gothic | warm photo | photo hero behind a cookie window | none visible | no | 63% |
| ketztek today | Inter, Instrument Sans | sand, purple | logo twice on stock marble | none | no | none |

**Category defaults (counted in code over the 7 competitors):**

- 5 of 7 use a cool accent (navy, blue, teal or green).
- 4 of 7 open on a photo or video; 2 on a blue gradient; 1 on a product screenshot.
- 7 of 7 use sans-serif type only; 7 of 7 are in German.
- 3 of 7 show a call to action on the first phone screen.
- 5 of 7 show a consent banner or notice on the first phone screen.
- 0 of 7 show their own work on a factory floor or building site, or use the visitors' documents as a visual idea.

**Baseline to meet:** KMUpower's text-led first screen with a real artifact and one clear button; Stellar's named free offer ("Kostenlosen Prozess-Check machen"); Theia's clear pair of primary and secondary actions. **Gap to own:** a warm, non-blue identity (the logo's yellow and black), the visitors' own documents and sites, and the honest-sizing stance.

## 7. Subject-matter vocabulary

| # | Item | Source | Visual or copy |
| --- | --- | --- | --- |
| 1 | Regierapport (+ "Vorlage Excel / Word / PDF") | Suggestions, `gl=ch hl=de`, 2026-11-21 | Visual: ruled report form |
| 2 | Bautagebuch (+ Vorlage, App) | Suggestions | Visual: dated log |
| 3 | Mängelliste (+ Vorlage) / Mängelmanagement Bau | Suggestions | Visual: checklist rows |
| 4 | Wartungsprotokoll (+ Vorlage) | Suggestions | Visual: inspection fields |
| 5 | Maschinendatenerfassung, Maschinendatenblatt | Suggestions | Copy |
| 6 | Baustellendokumentation (App, Vorlage, Software) | Suggestions | Copy |
| 7 | Prozesse digitalisieren (… Vorgehen, Beispiele) | Suggestions | Copy |
| 8 | Formulare digitalisieren; papierloses Büro | Suggestions | Copy |
| 9 | "Vorlage" (template) after almost every work document | Suggestions (rows 1-4) | Visual: the template as the starting point |
| 10 | "Quality reports assembled by hand" | Home | Copy |
| 11 | "Defect lists that never quite match the plan" | Home | Copy |
| 12 | "Site documentation spread across paper, Excel and messaging apps" | Home | Visual: paper, sheet, chat |
| 13 | "something people will actually use with gloves on" | Home | Visual: large targets, robust UI |
| 14 | "one critical Excel file and the person who understands it" | Expertise | Copy, signature line |
| 15 | Approvals, inspections, checklists, maintenance records | Expertise | Visual: check fields |
| 16 | Invoices, delivery notes, technical drawings | Expertise | Visual: documents |
| 17 | "a technician standing at the machine" | Expertise | Photo approach |
| 18 | "We come to the factory and to the building site." | Home | Photo approach |
| 19 | "before any invoice exists" | Home | Copy |
| 20 | Winterthur became an industrial town in the 19th century when Sulzer, Rieter and SLM built large plants | [Wikipedia: Winterthur](https://en.wikipedia.org/wiki/Winterthur), 12:00Z | Visual: machine-industry heritage |
| 21 | In the 1930s, 60% of the town's employees worked in the machine industry | Wikipedia | Copy context |
| 22 | "Winti", the local short name | Wikipedia | Copy, tone |
| 23 | "service and high-tech industrial satellite city" in the Zurich area | Wikipedia | Positioning |
| 24 | The logo's yellow double "z" on black text | Logo files | Visual: [INFERENCE] reads like the yellow-black marking on sites and machines |
| 25 | Half an hour; two weeks | Home | Copy: honest units of time |

Items 1-4, 9, 12, 13 and 15-16 can become a visual system (ruled fields, check marks, a template grid); 17, 18 and 24 a photographic or marking approach; the rest are copy.

## 8. Requirements

| Requirement | Value | Source |
| --- | --- | --- |
| Accessibility | WCAG 2.2 AA: text 4.5:1 (large 3:1), interface 3:1, focus visible, reflow at 320 px, reduced motion respected | [WCAG 2.2](https://www.w3.org/TR/WCAG22/), not re-fetched |
| Tap targets | 24 x 24 px minimum; 44 x 44 px for the menu button, primary buttons and form fields | WCAG 2.2 SC 2.5.8; "gloves on" (copy) |
| Reading | Body 16 px or more on phones, 18 px on desktop; 45-75 characters per line; one H1 per page | Design audit D-06, D-08 |
| First screen | Offer and "Book a free 30-minute call" visible without scrolling at 390 and 1440 px | Design audit D-02; prompt 3.8 |
| Fonts | At most two families, WOFF2, from a loadable source | Prompt 3.8; Google Fonts checks below |
| Performance | LCP 2.5 s or less, CLS 0.1 or less ([web.dev](https://web.dev/articles/vitals), not re-fetched); images with fixed dimensions | Presence audit F-12 |
| Languages | German first, English second, separate pages per language, layouts that hold German text about 30% longer | 3.2 |
| Editing | Content blocks editable without a developer (headless CMS later); address, email, phone and hours in one place | Section 0 |
| Booking | A button that opens the Microsoft Bookings free-consultation service in a new tab, not an embedded frame on phones | UX audit (booking findings) |
| Consent | No banner unless tracking is added; the current site loads no analytics | Presence audit F-13 |
| Legal | Impressum and privacy page in the footer | 3.4 |

Font sources checked on 2026-11-21 (HTTP 200 from `fonts.googleapis.com/css2`): Archivo (`wdth` 62-125, `wght` 100-900), Barlow (400, 600, 800), Barlow Condensed (600, 700), IBM Plex Sans (400, 600).

## 9. Lessons from the current site

**Keep:** the wordmark and icon; the copy voice (section 4); the free 30-minute call; Microsoft Bookings; the five services and two sectors.

**Never again (each measured in a prior report):**

1. A control on top of the phone menu button (F-01, D-01).
2. A button without a destination (F-03, D-04).
3. No call to action on the first screen; the logo shown twice (D-02).
4. Body text under 16 px on phones (D-08).
5. Pages without side margins; lines over 80 characters (D-06).
6. Text alignment switching between left, centre and right (D-07).
7. A second, unrelated accent color (D-05).
8. Stock photographs standing in for own work (D-11, F-05).
9. An unstyled form button; a form wider than the phone (D-10, D-03).
10. Menu links that work only on one page (F-06).
11. A machine-translation language switch instead of real pages (F-04).
12. Primary and secondary buttons that look the same (UX audit).
13. A 404 page with only a search box (D-17).

## 10. Design directions

### Direction A: "Rapport" (recommended)

- **Idea:** the site reads like a well-kept work report: ruled, dated, precise, and filled in with the visitor's own problem.
- **Roots:** vocabulary 1-4, 9-11, 15 (the Regierapport, Mängelliste and Wartungsprotokoll the visitors search templates for); 14; 24.
- **Palette:**

  | Name | Hex | Role |
  | --- | --- | --- |
  | Ink | `#000000` | Text, rules that matter, the logo's black |
  | Paper | `#ffffff` | Report sheets, content surfaces |
  | Desk | `#eeeeeb` | Page background behind sheets (neutral, not cream) |
  | Field line | `#6b6b66` | Input borders, form rules |
  | Ruling | `#b9b9b3` | Decorative ruled lines only |
  | Note | `#55554f` | Secondary text |
  | Marker | `#e8c048` | Logo yellow: primary button fill, the "next step" field |
  | Error | `#b42318` | Form errors |

- **Type:** Archivo (Google Fonts, variable `wdth` 62-125, `wght` 100-900): headlines at `wdth` 112 `wght` 700, body at `wdth` 100 `wght` 400, field labels at `wdth` 75 `wght` 500 in sentence case. Fallback `system-ui, -apple-system, "Segoe UI", Roboto, Arial, sans-serif`. One family, varied by width.
- **Layout:** one left-aligned text column (max 680 px) beside or above white "sheets" set on the desk color; ruled fields inside sheets; generous space between sheets. 12-column grid on desktop, one column on phones.
- **Signature:** the work-report block on the first screen: three ruled fields (Process, Today, Next step) filled with a real problem from the copy, and the "Next step" field holding the actual primary button in marker yellow.
- **Imagery:** none required to launch; own photos later as "attachments" pinned to sheets.
- **Motion:** none, or one marker fill under "Next step" on first load (off with reduced motion).

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

### Direction B: "Werkhalle"

- **Idea:** documentary: real people at real machines and on real sites, framed by the logo's yellow and black.
- **Roots:** vocabulary 13, 17, 18, 20, 21, 24.
- **Palette:** Black `#000000`; Yellow `#e8c048`; Concrete `#dcdad4`; White `#ffffff`; Steel `#3a3a37` (secondary text); Error `#b42318`.
- **Type:** Barlow Condensed 700 for headlines, Barlow 400 and 600 for text (Google Fonts). Fallback `"Arial Narrow", Arial, sans-serif`.
- **Layout:** full-width own photographs with text on concrete panels beside them, never over them; black used in narrow bands only.
- **Signature:** the double-"z" chevron as a yellow structural marker between sections and before the primary action.
- **Imagery:** own photography is essential: at least six to eight landscape photos from factories, sites and workshops `[[supply]]`.
- **Motion:** none.

```text
390 px                               1440 px
+------------------------------+     +-------------------------------------------------------------+
| wordmark              [menu] |     | wordmark       Services Sectors About Contact  [Book a call] |
| [own photo: technician at    |     | +---------------------------+  H1: We come to the factory  |
|  a machine, full width]      |     | | own photo, site or        |  and the building site.      |
| >> H1: We come to the factory|     | | factory, 60% width        |  Book a free 30-minute call  |
| and the building site.       |     | +---------------------------+  (yellow button)             |
| [Book a free 30-minute call] |     +-------------------------------------------------------------+
+------------------------------+
```

### Direction C: "Ablauf"

- **Idea:** one continuous drawn line carries the visitor from paper to a working tool: map, propose, build, teach.
- **Roots:** vocabulary 7, 8, 12, 15; the method copy.
- **Palette:** White `#ffffff`; Mist `#f2f3f4`; Graphite `#23272b`; Secondary `#4f555b`; Line `#8d9196`; Node `#e8c048`; Error `#b42318`.
- **Type:** IBM Plex Sans 400 and 600 (Google Fonts). Fallback `system-ui, Arial, sans-serif`.
- **Layout:** a single thin line runs down the home page, with yellow nodes at the four method steps; sections hang off the line.
- **Signature:** the process line itself.
- **Imagery:** line drawings of documents (paper form, sheet, app screen) instead of photos.
- **Motion:** the line draws once on first load (off with reduced motion).

### Review against defaults

| Direction | Risk found | Change made |
| --- | --- | --- |
| A | First draft used an ALL-CAPS "RAPPORT" label (template chrome) | Sentence-case "Work report" label |
| A | First draft set field labels in a monospace face (generic default) | Archivo at narrow width instead |
| A | First draft highlighted one headline word in marker yellow (single-word accent) | Marker only on the primary button and the "Next step" field |
| A | Ruled lines and square sheets risk the newspaper look | One text column, generous spacing between sheets, 2 px radius on sheets; rules only inside the report block and forms |
| A | Desk background close to the warm-cream default | Neutral `#eeeeeb` (no warm cast), sans-serif type, no terracotta |
| A | The block could read as a form to fill in (false affordance) | Printed text on rules, no input boxes; the only interactive element in it is the real button |
| B | Black backgrounds with one bright accent (generic default) | Black limited to narrow bands; page mostly white and concrete |
| B | Text over full-width photos (category default 4 of 7, contrast risk) | Text beside photos on concrete panels |
| B | Hazard-tape kitsch | Chevron used only as a marker, never as a striped band |
| C | Close to KMUpower's flow screenshot and Theia's mock-ups | No device or UI mock-ups; drawings of documents only |
| C | Graphite and grey drift toward the category's cool palette (5 of 7) | Yellow nodes carry the identity; still the closest to the category |

### Contrast (computed, WCAG formula)

| Direction | Pairing | Ratio |
| --- | --- | --- |
| A | Ink on Paper | 21:1 |
| A | Ink on Desk | 18.06:1 |
| A | Note on Paper / on Desk | 7.5:1 / 6.46:1 |
| A | Ink on Marker (primary button) | 12.06:1 |
| A | Field line on Paper (interface) | 5.36:1 |
| A | Error on Paper | 6.57:1 |
| A | Marker on Desk | 1.5:1, decoration only, never text |
| B | Black on Concrete / Steel on Concrete | 15.02:1 / 8.16:1 |
| B | Yellow on Black / Black on Yellow | 12.06:1 / 12.06:1 |
| C | Graphite on White / on Mist | 15.04:1 / 13.53:1 |
| C | Secondary on White; Line on White (interface) | 7.55:1; 3.17:1 |
| C | Graphite on Node yellow | 8.64:1 |

### Recommendation

**A, "Rapport".** It is built from the documents these visitors handle every day (they search for templates of exactly these reports), it differs from all seven competitors, it needs no photographs the business does not have, and its signature element is the primary action itself, which answers the measured "no next step on the first screen" failure. **Choose B** once the business can supply six to eight real photos from sites and factories; it is the strongest emotionally but empty without them. **Choose C** if the business wants a more software-product feel; it is the closest to the category.

### Ready-to-paste blocks for the alternatives

To generate an alternative design prompt, replace part 5 of the design prompt with one of these.

**B, "Werkhalle":** Your direction is documentary. The site shows real people at real machines and on real building sites, framed by the logo's yellow and black, because ketztek's promise is that it comes to the factory and the building site. Palette: Black `#000000` (text, narrow bands), Yellow `#e8c048` (primary button fill with black text, 12.06:1, and the chevron marker), Concrete `#dcdad4` (panels; black text 15.02:1), White `#ffffff`, Steel `#3a3a37` (secondary text on concrete, 8.16:1), Error `#b42318`. Type: Barlow Condensed 700 for headlines and Barlow 400/600 for text, from Google Fonts, fallback `"Arial Narrow", Arial, sans-serif`. Layout: full-width own photographs with text on concrete panels beside them, never on top; black only in narrow bands. Signature: the logo's double "z" used as a yellow chevron marker between sections and before the primary action, never as a striped band. Imagery: only the business's own photos `[[supply: six to eight landscape photos of the team at clients' machines and sites]]`. Motion: none. Do not drift into: dark full-bleed photo heroes with white text.

**C, "Ablauf":** Your direction is a process line. One continuous thin line runs down the home page from paper to a working tool, through four steps the business names: map the process, propose the fix, build it, teach the team. Palette: White `#ffffff`, Mist `#f2f3f4` (alternate sections), Graphite `#23272b` (text, 15.04:1 on white), Secondary `#4f555b` (7.55:1), Line `#8d9196` (the process line, 3.17:1), Node `#e8c048` (step nodes and the primary button with graphite text, 8.64:1), Error `#b42318`. Type: IBM Plex Sans 400/600 from Google Fonts, fallback `system-ui, Arial, sans-serif`. Imagery: simple line drawings of a paper form, a spreadsheet and an app screen, no device mock-ups. Motion: the line draws once on first load, off with reduced motion. Do not drift into: SaaS dashboards, floating UI cards, blue gradients.

## 11. Open questions

For the business:

1. Is a vector logo (SVG or PDF) available, and is `#e8c048` the official yellow?
2. Is `construction.jpg` your own photo, and are there photos from client sites, factories or workshops that may be shown?
3. Which projects may be described (even anonymously), with which results?
4. Who is on the team, by role, and may they appear with photos?
5. Phone number, hours, and the reply time to promise for messages.
6. German first, English second: correct? Who writes or approves the German copy?
7. Which booking service should the site link to (the free consultation), and should "Demo Software" stay on the booking page?
8. Any certifications or Microsoft partner status?

For the freelancer:

1. Present one direction (A) or all three to the business?
2. Build the first prototype with the existing English copy and German drafts, as the design prompt assumes?
3. Confirm the target tool; the prompt asks a coding agent for HTML and CSS.

## 12. Appendix

**Pages and readings (UTC, 2026-11-21):** ketztek pages (Home, Expertise, Contact, Privacy, 404) 10:32:13-10:32:57 (raw HTML, shared with the UX audit run); booking page 10:34; robots for 8 sites 11:58:46-11:58:50; fingerprints evolyze, Theia, PowerAlps, Stellar, KMUpower, IOZ, Noser, ketztek 11:58:56-12:01:05; search suggestions (28 seeds) 11:59:09-11:59:45; Wikipedia 12:00:07; logo files 12:00:37 and 12:00:47; icon sample 12:00:59; Google Fonts checks 12:03:09; wordmark sample 12:06:48.

**Scripts:** the prompt's Appendix A (fingerprint) and Appendix C (logo sampler), copied verbatim from the prompt and configured per site; contrast in Python with the WCAG formula; category counts in Python from the fingerprint JSON plus screenshot readings.

**Limitations:**

- The fingerprint script missed Stellar's gradient-filled button and counted IOZ's case-study cards and evolyze's scroll arrow as buttons; the counts above are corrected from the screenshots (noted for the prompt).
- Competitor inner pages not read; consent banners not clicked.
- German drafts are not by a native speaker.
- Prior-report facts older than today (UID, reviews, analytics) were not re-checked; none changes the design direction.
- Crawl delay: the logo downloads (12:00:37, 12:00:47) and the icon sample (12:00:59) ran while the ketztek fingerprint (12:00:41-12:01:05) was loading the same host, so a few requests came less than the 10 s `robots.txt` delay apart. The wordmark was re-sampled later with the delay kept.
