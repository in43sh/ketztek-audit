# ketztek GmbH (ketztek.com): Visual Design Audit

## About this run

| Item | Value |
| --- | --- |
| Site | `https://ketztek.com/` (WordPress 7.1.5, block theme Calm Canvas, child of "Bakery and Pastry") |
| Audit date | Saturday 2026-11-21, Europe/Zurich. Measurements 2026-11-21 10:00Z to 10:17Z. |
| Pages | Home, Expertise, Contact, Privacy Policy (legal template), Maintenance Page (published placeholder), a 404 URL. Impressum skipped: same template as Privacy with 10 words. |
| Viewports | 360 and 390 px (iPhone user agent, touch), 768 and 1440 px on every page; 600 and 1024 px on Home; 320 px reflow and a 640 px (200% zoom) layout on Home and Contact (Appendix C) |
| Prior audit | `internal/research/audit/ketztek-audit-report.md` (2026-11-20). Its design-related findings are cited by ID (F-01, F-03, F-04, F-05, F-06, F-09, F-10, F-12, F-15, F-16) and not re-reported. |
| Competitors | evolyze (Winterthur), Theia Solutions (Zürich), Stellar Automation (Dübendorf): the closest group-a alternatives in the prior audit. Home pages at 390 and 1440 px. |
| Method | The prompt's Appendix A extraction (summary mode), Appendix B merge and Appendix C checks, run with the Node runner and a cached headless Chromium; one extra probe for side margins, heading markup and color use. 47 page loads on ketztek.com, 10 s apart (its `Crawl-delay: 10`). |
| Brand material | None supplied. Logo yellow sampled from the logo file: `#e8c048`. |
| Screenshots | Kept in the session scratch folder only ("Keep screenshots": no). Cited by file name. |

Business context, written before measuring:

1. **Visitors:** operations managers and owners of Swiss industrial and construction SMEs, mostly German-speaking, often on a phone between site visits, comparing a few consultancies.
2. **Their job:** understand quickly that ketztek fixes slow processes with Microsoft tools or custom software, then book the free 30-minute call.
3. **What they should feel:** that a small, young Winterthur firm is competent, honest and safe to let into their factory or building site.

Labels: `[FACT]` measured or read in this run, `[INFERENCE]` follows from facts (step stated; for taste, the visitor it affects), `[UNVERIFIED]` not confirmed.

## 1. Executive summary

**Context.** A cautious plant or site manager must trust a young two-to-few-person firm with a core process. The site has to show competence fast and make the free call easy, mostly on a phone.

**Verdict.** The identity is calm and distinctive (wordmark, sand and near-black, Inter with Instrument Sans) and every text color passes WCAG contrast. The build around it is unfinished: broken phone controls, no next step on the first screen, inner pages without margins, an off-brand WordPress purple and template parts carry most of the page.

**Top 5 problems:** D-01 phone menu covered; D-02 no call to action on the first screen at any width; D-03 contact form too wide for phones; D-04 dead closing booking button; D-06 inner pages lose their margins.

**Top 5 strengths:** the wordmark and its yellow; a quiet sand and near-black palette with 0 contrast failures; reduced motion respected; 200% zoom and 320 px reflow pass on Home; specific, honest copy.

**Fix or redesign:** fix in place. Every finding is a token, component, layout or content change in the existing block theme; the identity can carry the positioning (Output §7).

**Section 0.1 challenge:** none.

## 2. Scorecard

| Category | Score | Justification |
| --- | --- | --- |
| Typography | 5 | Sound pairing, but 14.5 px body on phones on three key pages (D-08), H1 and H2 the same size, mixed heading weights (D-09). |
| Color and contrast | 7 | 0 computed contrast failures across 26 page-width readings; calm palette. Off-brand purple (D-05), four near-blacks. |
| Spacing and layout | 3 | 0 px side margins on Expertise at all widths (D-06), zig-zag alignment (D-07), lines up to 155 characters. |
| Visual hierarchy | 4 | Offer sentence reaches the first screen, but no call to action there at 390 or 1440 px and the logo appears twice (D-02); no H1 on Home (D-09). |
| Responsiveness | 3 | Menu unreachable by touch on every page (D-01); contact form forces a 390-392 px layout (D-03). Zoom and Home reflow pass. |
| Components and consistency | 4 | One consistent black primary button, but a dead button (D-04), an unstyled Submit (D-10), clickable-looking boxes that are not links (D-12). |
| Imagery | 3 | Stock marble hero, stock factory and construction photos, purple stock icons; no real work or people (D-11). |
| Motion | 6 | Reduced motion respected (0 hidden elements with it on); fade-in on every Home section without it (D-14). |
| Distinctiveness | 5 | The wordmark and palette stand apart from Theia's template look; the card stack, WordPress purple and theme defaults pull it back (D-05, D-12). |
| Written content | 6 | Specific, honest copy; the same action has three names (D-13); English only (F-04). |

## 3. Design as built

Computed by the Appendix B merge from 26 readings (6 pages, 4 to 6 widths each), 2026-11-21 10:01Z-10:09Z.

### Type

| Role | 360 / 390 px | 768 px | 1440 px | Family, weight |
| --- | --- | --- | --- | --- |
| Body (Home, Expertise, Contact) | 14.3 / 14.5 | 17.1 | 20 | Inter 400, line height 1.4 |
| Body (Privacy) | 16.1 / 16.2 | 17.0 | 18 | Inter 400, line height 1.4 |
| H1 | 32.7 / 33.3 | 40.1 | 48 | Instrument Sans 600 |
| H2 | 32.7 / 33.3 | 40.1 | 48 | Instrument Sans 600 |
| H3 | 22.7-24.4 / 23.2-24.6 | 28.1-29.2 | 32-36 | Instrument Sans 600 (900 where wrapped in `strong`) |
| H4 | 18.1 / 18.2 | 19.0 | 20 | Instrument Sans 600, line height 1.0 |
| Primary button | 16 | 16-17 | 16-18 | Inter 600 |
| Form label | 14.3 / 14.5 | 17.1 | 20 | Inter 400 |

Fonts loaded: Inter (variable, TTF) and Instrument Sans (variable, TTF), `font-display: fallback`, not preloaded; Inter carries 90.5% of characters. Distinct sizes per width: 7 to 9, with near-duplicates within 1 px at every phone and tablet width (14.09/14.27, 17.02/17.06).

### Color

| Role | Hex | Use |
| --- | --- | --- |
| Background, sand | `#ebe6d8` | 42.4% of painted area |
| Background, white | `#ffffff` | 57.5% |
| Text, near-blacks | `#0f0f0f` 45.3%, `#2c2c2c` 42.8%, `#1c1c1c` 0.3% | Body and links |
| Headings | `#3a3228` | 9.2% of characters |
| Purple | `#9b51e0` | 1.5% of characters, 37.5% of borders, 5 icon images |
| Logo yellow | `#e8c048` (sampled) | Logo only |

### Spacing, shape, components

| Token | In use |
| --- | --- |
| Spacing | 26 distinct values; 69.8% of uses on a 4 px grid; most used 24, 20, 40, 10, 5, 31 px |
| Side margins | Home 20 px (390) and 120 px (1440); Contact 20 and 60; Privacy 0 and 60 left / 0 right; Expertise 0 at every width |
| Radii | 10 px (42 uses), 14 px (4); buttons 5 px; 404 search button 10 px |
| Shadow | One: `rgba(0,0,0,0.05) 0 1px 2px` (34 uses) |
| Buttons | Primary black `#1c1c1c`, white text, 5 px radius (24 uses, Home); 404 search variant at 10 px; Contact Submit unstyled browser default `#efefef`, 13.3 px |
| Fixed layers | Header (6-11% of the first screen); the language switcher `gt_switcher_wrapper`, fixed over the header on every page |

### Pages and screenshots

| Page | Template | Screenshots (scratch folder `shots/`; findings cite them as `page-width-kind`) |
| --- | --- | --- |
| Home | Front page (maintenance-plugin template) | `20261121T1001Z-home-{360,390,600,768,1024,1440}-{fold,full}.png` |
| Expertise | Page | `20261121T1003Z-expertise-{360,390,768,1440}-{fold,full}.png` |
| Contact | Page with form and booking frame | `20261121T1004Z-contact-…`, `20261121T1010Z-contact-{320,390-textspacing,zoom200}.png` |
| Privacy Policy | Legal page | `20261121T1005Z-privacy-…` |
| Maintenance Page | Published placeholder | `20261121T1006Z-maintenance-…` |
| 404 | Theme error page | `20261121T1008Z-404-…` |

## 4. Findings

Index, ranked by effect on the site's job:

| ID | Title | Severity | Prior audit |
| --- | --- | --- | --- |
| D-01 | Language switch covers the phone menu button | High | F-01 |
| D-02 | No next step on the first screen | High | |
| D-03 | Contact form is too wide for phones | High | |
| D-04 | Closing booking button does nothing | High | F-03 |
| D-05 | Off-brand WordPress purple competes with the logo | Medium | |
| D-06 | Inner pages lose their margins | Medium | |
| D-07 | Zig-zag alignment breaks reading | Medium | |
| D-08 | Phone body text under 16 px on key pages | Medium | |
| D-09 | Heading sizes and weights do not form a scale | Medium | F-09 |
| D-10 | Contact form Submit is an unstyled default | Medium | |
| D-11 | Stock imagery where real work should be | Medium | F-05 |
| D-12 | Template cards and boxes that look clickable | Medium | F-06 |
| D-13 | One action, three names | Low | F-10 |
| D-14 | Fade-in on every Home section | Low | F-15 |
| D-15 | Non-breaking spaces cause odd line breaks | Low | |
| D-16 | Footer and language links are small targets | Low | F-15 |
| D-17 | 404 page offers only a search box | Low | |

### 3.2 Typography

#### [D-08] Phone body text under 16 px on key pages

- Severity: Medium
- Confidence: High
- Category: Typography
- Pages and viewports: Home, Expertise, Contact at 360 and 390 px
- Affects: a site manager reading on a phone outdoors
- Evidence: [FACT] Most paragraph text is 14.5 px at 390 (14.3 at 360) on Home (61% of paragraph characters), Expertise (98%) and Contact (89%), but 16.2 px on Privacy; 20 px at 1440 (Appendix A). [INFERENCE] The fluid scale drops below a 16 px floor; Privacy uses a different block style.
- Why it matters: the selling pages are hardest to read on the main device.
- Recommendation: Body text 16 px minimum on phones (fluid to 18 px), the same on every template.
- Effort: S
- Impact: Med
- Prior audit ID:

#### [D-09] Heading sizes and weights do not form a scale

- Severity: Medium
- Confidence: High
- Category: Typography
- Pages and viewports: all, all widths
- Affects: a visitor skimming headings to find the offer
- Evidence: [FACT] H1 and H2 are the same size at every width (32.7, 40.1, 48 px). [FACT] Home has no H1; its name is a logo image with empty alt text. [FACT] Some headings are wrapped in `strong` (900), others not (600); in "Find where your processes lose time." the bold stops before "time.". [FACT] H4 line height is 1.0.
- Why it matters: sections read as equal, so the offer does not stand out.
- Recommendation: One heading scale (about 1.25 steps), one weight, an H1 with the offer on Home, no `strong` wrappers, H4 line height 1.2.
- Effort: S
- Impact: Med
- Prior audit ID: F-09 (no H1)

#### [D-15] Non-breaking spaces cause odd line breaks

- Severity: Low
- Confidence: High
- Category: Typography
- Pages and viewports: Home, Expertise, Contact; phones most visibly
- Affects: phone readers
- Evidence: [FACT] 82 non-breaking spaces in the Home text, 63 on Expertise, 21 on Contact (probe, 10:13Z). [FACT] Expertise at 390 px breaks "built to be maintained — with / tests" and "or the / data can't leave" with half-empty lines (`20261121T1003Z-expertise-390-fold.png`).
- Why it matters: ragged, gappy lines look careless on a site selling precision.
- Recommendation: Replace the pasted non-breaking spaces with normal spaces, keeping them only between numbers and units.
- Effort: S
- Impact: Low
- Prior audit ID:

### 3.3 Color and contrast

Computed contrast: 0 failures in 26 readings. Manual checks: 8 text elements over images (the hero tagline over the marble texture; readable in screenshots), 14 whose background came from parent elements only (footer and form labels; screenshots show dark text on white or sand). Pairings for the recommended palette, computed: `#2c2c2c` on `#ebe6d8` 11.2:1; `#1c1c1c` on the logo yellow `#e8c048` 9.79:1; white on the yellow 1.74:1 (fails); the purple `#9b51e0` on sand 3.62:1 (passes only as large text).

#### [D-05] Off-brand WordPress purple competes with the logo

- Severity: Medium
- Confidence: High
- Category: Color
- Pages and viewports: Home, all widths
- Affects: a visitor forming a first impression of a careful, coherent firm
- Evidence: [FACT] `#9b51e0` colors 19 Home elements (Expertise boxes, both sector headings) and 37.5% of borders; five icons are purple images (`*_purp.png`). [INFERENCE] It is WordPress's built-in "vivid purple" preset, a default rather than a brand choice. [FACT] The logo accent is yellow `#e8c048`.
- Why it matters: two unrelated accents dilute the one distinctive asset the brand has.
- Recommendation: Drop the purple. Use near-black for icons, borders and sector headings, and the logo yellow sparingly as the action accent behind dark text.
- Effort: S
- Impact: Med
- Prior audit ID:

### 3.4 Spacing, grid and layout rhythm

#### [D-06] Inner pages lose their margins

- Severity: Medium
- Confidence: High
- Category: Spacing
- Pages and viewports: Expertise (all widths), Privacy (390, 1440 px)
- Affects: readers of the Expertise page, the site's strongest content
- Evidence: [FACT] Text margins: Expertise 0 px both sides at 390 and 1440; Privacy 0 at 390, 60 left and 0 right at 1440; Home 20 and 120; Contact 20 and 60 (probe, 10:13Z). [FACT] Expertise lines at 1440 px: median 138 characters, maximum 155; Privacy median 101 (Appendix B; `expertise-1440-fold`).
- Why it matters: edge-to-edge text and 150-character lines look broken and tire readers.
- Recommendation: One content container for every template: 20 px phone margins, text about 680 px wide at most, aligned with the logo.
- Effort: S
- Impact: High
- Prior audit ID:

#### [D-07] Zig-zag alignment breaks reading

- Severity: Medium
- Confidence: High
- Category: Spacing
- Pages and viewports: Home ("Why work with us", "Sectors", closing section), Expertise, Contact ("Book a call"), all widths
- Affects: a visitor scanning the reasons to trust the firm
- Evidence: [FACT] Expertise: 8 text blocks right-aligned, 10 left (probe). [FACT] Home's "Why work with us" alternates right and left alignment, including right-aligned multi-line paragraphs (`home-1440-full`). [FACT] Contact's "Book a call" is right-aligned (`contact-390-full`).
- Why it matters: the eye has to find a new starting edge for every block; right-aligned paragraphs longer than two lines are hard to read.
- Recommendation: Left-align all running text and headings; use one centered element at most (the closing call to action).
- Effort: S
- Impact: Med
- Prior audit ID:

### 3.5 Visual hierarchy and above the fold

#### [D-02] No next step on the first screen

- Severity: High
- Confidence: High
- Category: Hierarchy
- Pages and viewports: Home, every width (360-1440 px)
- Affects: a manager deciding in seconds whether to call
- Evidence: [FACT] No booking button among first-screen controls at 390 or 1440 px (Appendix A); on a 375 px phone it is 1,163 px down (prior run). [FACT] The hero repeats the logo at 547 px on stock marble with a slogan (`home-390-fold`, `home-1440-fold`). [FACT] Theia and Stellar show offer and button on the first phone screen.
- Why it matters: the site's one action appears only after a screen of logo.
- Recommendation: Replace the second logo with the offer as H1 and the booking button, inside the first phone screen.
- Effort: S
- Impact: High
- Prior audit ID:

### 3.6 Responsiveness

Passes: Home has no sideways scroll at 320 px and at the 200% zoom layout; no page overflows at 768, 1024 or 1440 px.

#### [D-01] Language switch covers the phone menu button

- Severity: High
- Confidence: High
- Category: Responsive
- Pages and viewports: all six pages at 360 and 390 px (Contact at 390)
- Affects: phone visitors looking for another page
- Evidence: [FACT] In 11 of 12 phone readings, the element at the centre of the 24 x 24 px "Open menu" button is the "EN" link (Appendix A). [FACT] The fixed layer over the header is the language switcher `gt_switcher_wrapper`. A real tap confirmed it in the prior audit.
- Why it matters: the menu is the only way to other pages on phones; the footer has only Privacy and Impressum.
- Recommendation: Move the language switcher into the menu on phones; add Contact and booking links to the footer.
- Effort: S
- Impact: High
- Prior audit ID: F-01

#### [D-03] Contact form is too wide for phones

- Severity: High
- Confidence: High
- Category: Responsive
- Pages and viewports: Contact at 320, 360 and 390 px
- Affects: a visitor writing an enquiry on a phone
- Evidence: [FACT] Layout width 390 px in a 320 px window, 392 px at 360 and 390 (Appendix A `layoutWidth`, C `reflow320`). [FACT] The overflowing elements are the form fields and labels; the Message box runs past its card and the screen (`contact-390-full`). [INFERENCE] The fields keep their `size="40"` width, so the phone shrinks or side-scrolls the page.
- Why it matters: the enquiry page looks broken on common phones and fails [WCAG 2.2 SC 1.4.10](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html) (not re-fetched).
- Recommendation: Set form fields to `width: 100%` with `box-sizing: border-box` inside the card.
- Effort: S
- Impact: High
- Prior audit ID:

### 3.7 Components and consistency

Keyboard focus (Appendix C, 1440 px): Home 38 of 40 steps show a visible change; Contact 24, plus 7 unknown steps inside the Cloudflare Turnstile widget (shadow DOM, check by hand) and the Microsoft Bookings frame. No focus ring under 3:1.

#### [D-04] Closing booking button does nothing

- Severity: High
- Confidence: High
- Category: Components
- Pages and viewports: Home, all widths
- Affects: a visitor convinced by the whole page
- Evidence: [FACT] "Book a 30-minute call" in the closing section is a link without a destination on all 6 Home widths (Appendix A `noHref`). [FACT] It never receives keyboard focus: the focus walk goes from "Write to us" to "Or just send us a message" (Appendix C, 10:09Z).
- Why it matters: the last and most decisive button fails silently, for mouse, touch and keyboard.
- Recommendation: Link it to the booking page, as the first button is.
- Effort: S
- Impact: High
- Prior audit ID: F-03

#### [D-10] Contact form Submit is an unstyled default

- Severity: Medium
- Confidence: High
- Category: Components
- Pages and viewports: Contact, all widths
- Affects: a visitor about to send an enquiry
- Evidence: [FACT] Submit renders in the browser default: background `#efefef`, 13.3 px text, square corners, while every other button is black `#1c1c1c` with white 16 px text and 5 px corners (Appendix B button table). [FACT] Visible in `20261121T1004Z-contact-390-full.png`.
- Why it matters: the final step of the main form looks unfinished, at the moment trust matters most.
- Recommendation: Style Submit as the primary button and name it "Send message".
- Effort: S
- Impact: Med
- Prior audit ID:

#### [D-12] Template cards and boxes that look clickable

- Severity: Medium
- Confidence: High
- Category: Components
- Pages and viewports: Home, all widths
- Affects: a visitor deciding whether the firm is specialist or generic
- Evidence: [FACT] "What we offer" is five identical white cards: 10 px radius, one soft shadow, centered text (`home-1440-full`). [FACT] The six Expertise boxes have button-like outlines but are not links; the Expertise page is not linked from Home (F-06).
- Why it matters: the services look like any template's, and boxes that look like buttons but do nothing frustrate.
- Recommendation: Turn the services into a left-aligned list with one line each and a link to a service page; make the Expertise boxes links to `/expertise/` sections, or plain text without outlines.
- Effort: M
- Impact: Med
- Prior audit ID: F-06

#### [D-17] 404 page offers only a search box

- Severity: Low
- Confidence: High
- Category: Components
- Pages and viewports: any missing URL, all widths
- Affects: a visitor following an old or mistyped link
- Evidence: [FACT] The 404 keeps the site's design but shows only "404 – Page Not Found", "Search below to find what you're looking for." and a search field, the theme's default text; the menu is covered on phones (D-01) (`20261121T1008Z-404-390-full.png`).
- Why it matters: a six-page site gains nothing from search; a dead end loses the visitor.
- Recommendation: Replace the search with links to Home and to booking a call.
- Effort: S
- Impact: Low
- Prior audit ID:

### 3.8 Imagery and iconography

#### [D-11] Stock imagery where real work should be

- Severity: Medium
- Confidence: High
- Category: Imagery
- Pages and viewports: Home, all widths
- Affects: a manager judging whether the firm has done this before
- Evidence: [FACT] The hero background is a stock marble texture (`pexels-diva-29035509`); the two sector photos are a stock factory image (`pexels-anntarazevich-5963134`) and a generic construction image; the five service icons are purple stock-style icons (Appendix A images). [FACT] No image shows the team, an office, a site visit or a delivered tool.
- Why it matters: for a firm whose pitch is "we come to the factory", generic pictures say the opposite.
- Recommendation: Use real photos from site visits and screenshots of delivered apps (with permission), and replace the marble with the offer (D-02).
- Effort: M
- Impact: Med
- Prior audit ID: F-05

### 3.9 Motion

#### [D-14] Fade-in on every Home section

- Severity: Low
- Confidence: High
- Category: Motion
- Pages and viewports: Home, all widths
- Affects: visitors who scroll quickly; nobody with reduced motion set
- Evidence: [FACT] 30-31 text elements are hidden until scrolled into view at every Home width; with `prefers-reduced-motion: reduce`, 0 are hidden and 0 animations run (Appendix A and C). [FACT] A `prefers-reduced-motion` rule exists.
- Why it matters: a uniform entrance animation on every section is a template default that draws attention to nothing; fast scrollers meet blank gaps.
- Recommendation: Remove the section animations, or keep one on the first screen only.
- Effort: S
- Impact: Low
- Prior audit ID: F-15

### 3.10 Template check

See Output §5.

### 3.11 Written content

#### [D-13] One action, three names

- Severity: Low
- Confidence: High
- Category: Content
- Pages and viewports: Home, Contact, booking page
- Affects: a visitor deciding which button leads where
- Evidence: [FACT] The booking action is "Book a free 30-minute call", "Book a 30-minute call" and "Book a call"; the message action is "Write to us", "Or just send us a message" and "Submit". [FACT] The booking page offers four services (F-10).
- Why it matters: consistent names are how visitors learn the way; "free" disappearing reads as a change of offer.
- Recommendation: One name per action everywhere: "Book a free 30-minute call" and "Send a message".
- Effort: S
- Impact: Low
- Prior audit ID: F-10

#### [D-16] Footer and language links are small targets

- Severity: Low
- Confidence: High
- Category: Responsive
- Pages and viewports: all pages, phones
- Affects: phone users tapping legal or language links
- Evidence: [FACT] 5 to 11 controls per page under 24 px high at 390 px, one of them a visually hidden skip link: "Privacy Policy" 84 x 15, "Impressum" 66 x 15, "EN" 20 x 17, "DE" 19 x 17, inline email links (Appendix A, 390 px).
- Why it matters: small targets cause mis-taps ([WCAG 2.2 SC 2.5.8](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html), not re-fetched in this run).
- Recommendation: Give footer and language links at least 24 px of tap height through padding.
- Effort: S
- Impact: Low
- Prior audit ID: F-15

### 3.12 Brand surfaces

Favicon and 180 px touch icon use the wordmark crop; no share image (F-09); the Google profile has no logo or photos (F-07, read 2026-11-20, not re-read). The booking page header shows "ketztek" as plain text. No social profiles exist to compare.

### Strengths to keep

- The wordmark with its yellow double "z": distinctive, legible at 120 px in the header.
- A quiet palette: sand `#ebe6d8`, white, near-black, brown headings; 0 contrast failures across 26 readings.
- Inter and Instrument Sans: a sound, unshowy pairing for a technical firm.
- Reduced motion respected; 200% zoom and 320 px reflow pass on Home.
- Keyboard focus visible on 38 of 40 Home steps.
- One consistent primary button style.
- Honest, specific copy ("Sometimes the honest answer is two weeks of work").

## 5. Template-default check

| Item | Result | Where |
| --- | --- | --- |
| Theme or template named for another trade | seen | Parent theme "Bakery and Pastry" (source only; F-16) |
| Placeholder or demo content | seen | Published "Maintenance Page": "Website is under Maintenance." (F-09, F-16) |
| Builder chrome in footer | not seen | |
| Default 404 page | seen | Theme default text and search (D-17) |
| Legal links to home or a builder's editor | seen | Privacy links into a Hostpoint editor (F-11) |
| Buttons with no destination | seen | Closing booking button (D-04) |
| Cream, high-contrast serif, terracotta | not seen | Sand background, but sans-serif type and a yellow accent |
| Near-black with acid accent | not seen | |
| Newspaper layout | not seen | |
| Card kit | seen | "What we offer" (D-12) |
| Template chrome (caps eyebrows, middle dots, arrows, `#111`-style blacks, monospace labels) | partly | Four near-blacks (`#0f0f0f`, `#1c1c1c`, `#2c2c2c`, `#3a3228`); none of the others (0 caps labels, 0 middle dots, 0 arrows) |
| Numbered markers on a non-sequence | not seen | Privacy's numbered headings are a real sequence |
| Big-number hero | not seen | |
| Theme default fonts and palette unchanged | seen | Calm Canvas ships Inter and Instrument Sans; WordPress "vivid purple" `#9b51e0` (D-05) |

**Business-specific replacements:** the logo yellow as the single action color; real photos from factory floors and building sites, including people by role in work gear; a screenshot of a delivered Power App or dashboard; a simple drawn process map (paper, Excel, app) for the hero or services; Winterthur's industrial setting; the trade's own words (defect lists, maintenance records, quality reports) in headings.

## 6. Page-by-page notes

| Page | 390 px first screen | 1440 px first screen | Findings |
| --- | --- | --- | --- |
| Home | Header logo, covered menu, EN/DE; hero logo again on marble; tagline; "Start with your processes." and the offer sentence at the bottom. No button. | Nav and EN/DE; large hero logo and tagline; offer heading and sentence. No button. | D-01, D-02, D-05, D-07, D-08, D-09, D-11, D-12, D-14 |
| Expertise | "Expertise" title and text from the screen edge; first section heading right-aligned. | Text flush to the window edge at 0 px; alternating hard-left and hard-right headings; 150-character lines. | D-01, D-06, D-07, D-08, D-15 |
| Contact | H1 "Let's talk about the process that annoys you most", intro; form below. Form wider than the screen. | H1, intro, form card; booking section right-aligned. | D-01, D-03, D-07, D-10, D-13 |
| Privacy | Title and text from the screen edge. | Title at 60 px, body at 120 px; lines to the right edge. | D-01, D-06 |
| Maintenance | "Maintenance Page", "Website is under Maintenance." | Same | F-16 |
| 404 | "404 – Page Not Found", search field. | Same | D-01, D-17 |

## 7. Design direction

**Fix in place.** The identity is sound; the faults are in layout, components and defaults. A new direction is not supported by the evidence.

Corrected token sheet:

| Token | Keep, merge or change | Value | Finding |
| --- | --- | --- | --- |
| Ink | Merge `#0f0f0f`, `#1c1c1c`, `#2c2c2c` | `#1c1c1c` for text and buttons | D-05 |
| Heading | Keep | `#3a3228` | |
| Sand, white | Keep | `#ebe6d8`, `#ffffff` | |
| Accent | Change: drop `#9b51e0` | Logo yellow `#e8c048`, only as a fill behind `#1c1c1c` text (9.79:1) or as a thin underline; never as text on sand (1.4:1) | D-05 |
| Body size | Change | 16 px phones to 18 px desktop, all templates | D-08 |
| Heading scale | Change | H4 18, H3 22, H2 28, H1 36 px on phones; H4 20, H3 28, H2 36, H1 48 px on desktop; one weight (600) | D-09 |
| Content width | Change | 20 px phone margins; text column max about 680 px; left edge aligned with the logo | D-06 |
| Spacing | Merge | 8, 16, 24, 40, 80 px; drop 5, 31, 61 and similar one-offs | D-06 |
| Alignment | Change | Left-aligned text everywhere; one centered closing block | D-07 |
| Buttons | Merge | One primary (ink, white text, 5 px radius, 16 px), one secondary outline; Submit uses the primary | D-10 |

Component fixes, in order: language switcher out of the menu button's way (D-01); closing button linked (D-04); form fields at full width (D-03); hero with H1 offer and booking button (D-02); services as a list with links, Expertise boxes as links (D-12); 404 with two links (D-17).

Keep: the wordmark, sand and ink, the font pairing, the copy's voice, the primary button style.

## 8. Prioritized changes

| When | Finding | Change | Owner | Effort | Impact |
| --- | --- | --- | --- | --- | --- |
| Quick fix (under a day) | D-01 | Move language switcher on phones | Site administrator | S | High |
| Quick fix | D-04 | Link closing booking button | Site administrator | S | High |
| Quick fix | D-03 | Full-width contact form fields | Site administrator | S | High |
| Quick fix | D-10 | Style Submit as primary | Site administrator | S | Med |
| Quick fix | D-13 | One name per action | Site administrator | S | Low |
| Short term (under two weeks) | D-02 | Offer and button in hero | Designer, site administrator | S | High |
| Short term | D-06 | One content container everywhere | Site administrator | S | High |
| Short term | D-07 | Left-align all text | Site administrator | S | Med |
| Short term | D-08 | 16 px minimum body text | Site administrator | S | Med |
| Short term | D-09 | One heading scale and weight | Designer | S | Med |
| Short term | D-05 | Replace purple with ink and yellow | Designer | S | Med |
| Short term | D-15 | Remove pasted non-breaking spaces | Site administrator | S | Low |
| Short term | D-16 | Larger footer tap targets | Site administrator | S | Low |
| Short term | D-17 | 404 links to Home and booking | Site administrator | S | Low |
| Short term | D-14 | Drop section fade-ins | Site administrator | S | Low |
| Medium term | D-11 | Real photos of work | The business | M | Med |
| Medium term | D-12 | Services list, linked expertise | Designer, site administrator | M | Med |

No Critical finding. All four High findings are Quick fixes or Short term.

## 9. Client-safe summary

Written separately: [`client/reports/ketztek-design-summary.md`](../../../client/reports/ketztek-design-summary.md).

## 10. Open questions

For the business:

1. Is the current look meant to stay (logo, sand, fonts), or is a change welcome?
2. Who edits the site, and is the WordPress theme customised in code or only in the editor?
3. Are there photos from site visits, workshops or delivered tools that may be shown, and who owns them?
4. Is the purple a deliberate brand color?
5. Which language should the design be set for first (German or English; F-04)?

For the freelancer:

1. Present this as fixes on the current WordPress site, or as input to a rebuild? The evidence supports fixes.
2. Add a native German reviewer if German pages are designed.
3. Settled 2026-11-21 10:34Z: the Microsoft Bookings frame on Contact renders in a full Chromium browser at 390 px (logo, "Select a service", four services). The blank area in this run's captures came from the headless shell build, not the site.

## 11. Appendix

### Pages, viewports and loads

| Page | URL | Widths | Status |
| --- | --- | --- | --- |
| Home | `https://ketztek.com/` | 360, 390, 600, 768, 1024, 1440; Appendix C 320, 390, 640, 1440 | 200 |
| Expertise | `https://ketztek.com/expertise/` | 360, 390, 768, 1440 | 200 |
| Contact | `https://ketztek.com/contact/` | 360, 390, 768, 1440; Appendix C 320, 390, 640, 1440 | 200 |
| Privacy | `https://ketztek.com/privacy-policy/` | 360, 390, 768, 1440 | 200 |
| Maintenance | `https://ketztek.com/maintenance-page/` | 360, 390, 768, 1440 | 200 |
| 404 | `https://ketztek.com/this-page-does-not-exist-404/` | 360, 390, 768, 1440 | 404 |

Load log (UTC): robots 10:00:46; extraction Home 10:01:07-10:03:02, Expertise 10:03:12-10:04:14, Contact 10:04:24-10:05:26, Privacy 10:05:36-10:06:42, Maintenance 10:06:52-10:07:51, 404 10:08:01-10:09:01; Appendix C Home 10:09:29-10:10:46, Contact 10:10:56-10:12:11; margin and markup probe 10:12:56-10:15:13; raw HTML 10:15:47; logo file 10:16:58. Competitors: evolyze 10:01:21, Theia 10:01:46 (re-run 10:03-10:04, see limitations), Stellar 10:02:15; robots read first.

### Competitor comparison (home pages)

| | ketztek | evolyze | Theia | Stellar |
| --- | --- | --- | --- | --- |
| First phone screen | Logo twice, tagline, no button | Offer headline, scroll arrow | Offer, two buttons | Offer, one button |
| Body text at 390 px | 14.5 px Inter | 16 px Manrope, 1.6 | 14 px Montserrat, 1.63 | 14 px Inter, 1.6 |
| H1 at 1440 px | none | 46 px | 64 px | 86 px |
| Contrast failures (groups) | 0 | 0 | 18-25 (greys at 4.3-4.5, link blue 4.16) | 1 |
| Consent banner | none | none | yes, 15-16% of first screen | yes |
| Language | English | German | German, English | German |

Lessons: evolyze and Stellar show that a calm or plain page still puts the offer and one action first. Theia uses several generic defaults (caps eyebrow, gradient-accented word, arrows on buttons), which ketztek's quieter identity can avoid.

### Commands and scripts

- Appendix A, B and C scripts copied verbatim from the prompt, configured per page (`URL`, `PAGE`, `VIEWPORTS`, `SHOT_DIR`), run with `node run-extract.mjs <script> <out.json> <chromium>`; merge with `python3 -I merge.py extract-*.json`.
- Probe for side margins, heading markup, purple use and non-breaking spaces: one page load per page at 390 and 1440 px.
- `curl` for `robots.txt`, raw Home HTML (font-face rules) and the logo PNG (yellow sampled by decoding the PNG in Node).
- Contrast for the proposed palette computed in Python with the WCAG formula.

### Limitations

- Headless Chromium (shell build 149) stands in for real phones; the menu-button finding was confirmed with a real tap in the prior audit only.
- The Microsoft Bookings frame rendered blank in every headless-shell capture. A later check in full Chromium (2026-11-21 10:34Z) showed it renders; its own layout was not judged here.
- The Cloudflare Turnstile widget sits in shadow DOM; its focus indicator and layout were not judged.
- Hover, active and disabled states were not checked by hand.
- The Google profile and booking page were not re-read; cited from the prior audit (2026-11-20).
- Competitor inner pages not read. Theia was re-run after a script fix (see the pilot notes kept with this run); its figures above are from the re-run.
- Copy judgements are for English text; no German pages exist.

### Machine-readable summary

```json
[
 {
  "id": "D-01",
  "title": "Language switch covers the phone menu button",
  "severity": "High",
  "confidence": "High",
  "category": "Responsive",
  "pages": "all six pages at 360 and 390 px (Contact at 390)",
  "effort": "S",
  "impact": "High",
  "prior_audit_id": "F-01"
 },
 {
  "id": "D-02",
  "title": "No next step on the first screen",
  "severity": "High",
  "confidence": "High",
  "category": "Hierarchy",
  "pages": "Home, every width (360-1440 px)",
  "effort": "S",
  "impact": "High",
  "prior_audit_id": ""
 },
 {
  "id": "D-03",
  "title": "Contact form is too wide for phones",
  "severity": "High",
  "confidence": "High",
  "category": "Responsive",
  "pages": "Contact at 320, 360 and 390 px",
  "effort": "S",
  "impact": "High",
  "prior_audit_id": ""
 },
 {
  "id": "D-04",
  "title": "Closing booking button does nothing",
  "severity": "High",
  "confidence": "High",
  "category": "Components",
  "pages": "Home, all widths",
  "effort": "S",
  "impact": "High",
  "prior_audit_id": "F-03"
 },
 {
  "id": "D-05",
  "title": "Off-brand WordPress purple competes with the logo",
  "severity": "Medium",
  "confidence": "High",
  "category": "Color",
  "pages": "Home, all widths",
  "effort": "S",
  "impact": "Med",
  "prior_audit_id": ""
 },
 {
  "id": "D-06",
  "title": "Inner pages lose their margins",
  "severity": "Medium",
  "confidence": "High",
  "category": "Spacing",
  "pages": "Expertise (all widths), Privacy (390, 1440 px)",
  "effort": "S",
  "impact": "High",
  "prior_audit_id": ""
 },
 {
  "id": "D-07",
  "title": "Zig-zag alignment breaks reading",
  "severity": "Medium",
  "confidence": "High",
  "category": "Spacing",
  "pages": "Home (\"Why work with us\", \"Sectors\", closing section), Expertise, Contact (\"Book a call\"), all widths",
  "effort": "S",
  "impact": "Med",
  "prior_audit_id": ""
 },
 {
  "id": "D-08",
  "title": "Phone body text under 16 px on key pages",
  "severity": "Medium",
  "confidence": "High",
  "category": "Typography",
  "pages": "Home, Expertise, Contact at 360 and 390 px",
  "effort": "S",
  "impact": "Med",
  "prior_audit_id": ""
 },
 {
  "id": "D-09",
  "title": "Heading sizes and weights do not form a scale",
  "severity": "Medium",
  "confidence": "High",
  "category": "Typography",
  "pages": "all, all widths",
  "effort": "S",
  "impact": "Med",
  "prior_audit_id": "F-09 (no H1)"
 },
 {
  "id": "D-10",
  "title": "Contact form Submit is an unstyled default",
  "severity": "Medium",
  "confidence": "High",
  "category": "Components",
  "pages": "Contact, all widths",
  "effort": "S",
  "impact": "Med",
  "prior_audit_id": ""
 },
 {
  "id": "D-11",
  "title": "Stock imagery where real work should be",
  "severity": "Medium",
  "confidence": "High",
  "category": "Imagery",
  "pages": "Home, all widths",
  "effort": "M",
  "impact": "Med",
  "prior_audit_id": "F-05"
 },
 {
  "id": "D-12",
  "title": "Template cards and boxes that look clickable",
  "severity": "Medium",
  "confidence": "High",
  "category": "Components",
  "pages": "Home, all widths",
  "effort": "M",
  "impact": "Med",
  "prior_audit_id": "F-06"
 },
 {
  "id": "D-13",
  "title": "One action, three names",
  "severity": "Low",
  "confidence": "High",
  "category": "Content",
  "pages": "Home, Contact, booking page",
  "effort": "S",
  "impact": "Low",
  "prior_audit_id": "F-10"
 },
 {
  "id": "D-14",
  "title": "Fade-in on every Home section",
  "severity": "Low",
  "confidence": "High",
  "category": "Motion",
  "pages": "Home, all widths",
  "effort": "S",
  "impact": "Low",
  "prior_audit_id": "F-15"
 },
 {
  "id": "D-15",
  "title": "Non-breaking spaces cause odd line breaks",
  "severity": "Low",
  "confidence": "High",
  "category": "Typography",
  "pages": "Home, Expertise, Contact; phones most visibly",
  "effort": "S",
  "impact": "Low",
  "prior_audit_id": ""
 },
 {
  "id": "D-16",
  "title": "Footer and language links are small targets",
  "severity": "Low",
  "confidence": "High",
  "category": "Responsive",
  "pages": "all pages, phones",
  "effort": "S",
  "impact": "Low",
  "prior_audit_id": "F-15"
 },
 {
  "id": "D-17",
  "title": "404 page offers only a search box",
  "severity": "Low",
  "confidence": "High",
  "category": "Components",
  "pages": "any missing URL, all widths",
  "effort": "S",
  "impact": "Low",
  "prior_audit_id": ""
 }
]
```
