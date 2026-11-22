# ketztek design v2 (Option E): direction, scoring and spec

Date: 2026-11-21. Inputs: [visual research](ketztek-visual-research.md), [design v2 prompt](ketztek-design-v2-prompt.md), the [earlier design prompt](../design-brief/ketztek-design-prompt.md) (copy bank, pages, supply list). Logo: option B "Balanced" from `client/logo-options/`, marked as a proposal on the page.

## 1. Three directions

Each direction differs from the others in layout and visual system, not only in colour. Hex values are the palette; ratios are WCAG 2.2 contrast, computed on 2026-11-21.

### 1.1 Direction 1: "Drawing sheet" (chosen)

- **Idea:** every page is a numbered drawing sheet of the visitor's own process, with a title block, as in an engineering drawing set. Nothing is a stock picture; everything is a figure drawn from the visitors' documents.
- **Palette:** Ink `#000000` (all text, rules that matter, logo black); Paper `#ffffff` (sheets); Drawing paper `#f4f4f1` (page); Concrete `#d6d7d2` (decorative rules and figure fills); Note `#4a4b47` (secondary text); Marker `#ebc34d` (logo yellow: primary button fill and the "after" mark in figures); Rust `#9e3d1b` (the problem marks in figures and one small label style); Error `#b42318` (form errors).
- **Contrast:** Ink on Paper 21.00:1; Ink on Drawing paper 19.06:1; Note on Paper 8.79:1; Note on Drawing paper 7.98:1; Ink on Marker 12.45:1; Rust text on Paper 6.69:1; Rust text on Drawing paper 6.07:1; Error on Paper 6.57:1; Field line `#6b6b66` on Paper 5.36:1 (interface). Marker on Drawing paper 1.53:1, so a yellow button always gets an Ink outline. Concrete on Paper 1.45:1: decoration only.
- **Type:** Archivo, self-hosted WOFF2 (variable `wdth`, `wght`). Headlines `wdth` 100, `wght` 700, line height 1.1, slight negative tracking. Body `wdth` 100, `wght` 400, line height 1.55. Labels, figure captions and form labels `wdth` 75, `wght` 500, sentence case. Fallback `system-ui, -apple-system, "Segoe UI", Roboto, Arial, sans-serif`.
- **Layout:** 12-column grid on desktop (1200 px frame, 40 px gutters on desktop, 20 px on phones). Drawing number and label in the left 3 columns, text and figures in the right 9. One column on phones.
- **Signature:** the title block: a bordered box in the bottom-right of the first screen with four cells, Process, Status, Next step, and a drawing number "Sheet 1 of 1". The Next step cell holds the real primary button. Used once per page.
- **Visual system:** line figures on the grid: 1.5 px Ink strokes, square corners, labels in label style, a caption "Fig. n". Before state drawn in Note with dashed lines and Rust problem marks; after state drawn in Ink with a Marker fill on the one element that changed.
- **Motion:** one. The "after" line of the first figure draws once on load (600 ms, ease-out). Off under `prefers-reduced-motion`.
- **Buildable:** static HTML and CSS, inline SVG figures, no framework.

Wireframe, Home first screen:

```text
390 px                                   1440 px
+------------------------------------+   +----------------------------------------------------------------+
| [logo B]                    [Menu] |   | [logo B]        Services  Sectors  About  Contact  DE|EN  [Book a call] |
|                                    |   |----------------------------------------------------------------|
| 01  Find the process that costs    |   | 01 Find the process that costs     +----------------------------+|
|     you time, and fix it with the  |   |    you time, and fix it with the   | Process   Excel file +email  ||
|     tools you already have.        |   |    tools you already have.         | Today     assembled by hand   ||
|                                    |   |    Analysis, automation and        | Next step [Book a free     ||
|  Analysis, automation and custom   |   |    custom software ...             |           30-minute call] ||
|  software ... Winterthur.          |   |    Send a message                  | Sheet 1 of 1               ||
|  Send a message                    |   +----------------------------------------------------------------+
|                                    |
| +--------------------------------+ |
| | Process   Quality reports      | |
| | Today     assembled by hand    | |
| | Next step [Book a free 30-min] | |
| | Sheet 1 of 1                   | |
| +--------------------------------+ |
+------------------------------------+
```

### 1.2 Direction 2: "Product fragments"

- **Idea:** the site shows the tools ketztek builds as flat, labelled interface fragments: an inspection checklist, an approval step, a maintenance log. The visitor sees the outcome before the price.
- **Palette:** Ink `#000000`; Paper `#ffffff`; Mineral `#ecebe6` (page); Graphite `#2b2c2a` (fragment chrome); Marker `#ebc34d` (state only: "done", the primary button); Rust `#9e3d1b` (open issue).
- **Type:** Archivo; headlines `wdth` 100 `wght` 600; fragment labels `wdth` 75.
- **Layout:** text left, one fragment right; fragments on the grid with 1 px borders and no shadows, never floating.
- **Signature:** a checklist whose last row is "Book a free 30-minute call".
- **Motion:** check marks tick once on load.
- **Why not chosen:** the nearest of the three to a SaaS dashboard, which the brief rules out. Interface fragments also need real product screens to be honest, and ketztek has none to show. Scored below Direction 1 for finished-without-photos and buildable.

Wireframe, Home first screen:

```text
390 px                                   1440 px
+------------------------------------+   +----------------------------------------------------------------+
| [logo B]                    [Menu] |   | [logo B]     Services  Sectors  About  Contact  DE|EN  [Book a call] |
| H1: Find the process that costs    |   | H1: Find the process          +-----------------------------+  |
|     you time ...                  |   |     that costs you time ...   | Inspection checklist  [x]   |  |
| Analysis, automation ...           |   | Analysis, automation ...      | [x] Guard fitted            |  |
| +--------------------------------+ |   |                               | [ ] Log entry  OPEN (rust)  |  |
| | Inspection checklist           | |   |                               | [Book a free 30-min call]   |  |
| | [x] Guard fitted               | |   |                               +-----------------------------+  |
| | [ ] Log entry  OPEN            | |   +----------------------------------------------------------------+
| | [Book a free 30-minute call]   | |
| +--------------------------------+ |
+------------------------------------+
```

### 1.3 Direction 3: "Measured"

- **Idea:** the honest-sizing promise is drawn as a dimension line. "Half an hour" and "two weeks" are the only measured units on the site, shown on lines with ticks and labels.
- **Palette:** Ink `#000000`; Paper `#ffffff`; Stone `#e7e5df` (bands); Graphite `#2b2c2a`; Marker `#ebc34d` (the dimension line's end cap and the primary button).
- **Type:** Archivo `wdth` 125 for headlines (expanded), `wdth` 100 body. The expanded headline is the most distinctive type choice of the three.
- **Layout:** full-width measured bands, one dimension line per page.
- **Signature:** the dimension line under the H1, labelled with the honest time.
- **Motion:** the dimension line extends once on load.
- **Why not chosen:** the signature is a generic blueprint idea; it reads as an engineering template and repeats on every page, against the brief's "one signature, spent in one place". Its primary button and phone layout score the same as Direction 1, but it has no drawn set to carry the rest of the site, and the expanded width is harder to hold at 320 px.

Wireframe, Home first screen:

```text
390 px                                   1440 px
+------------------------------------+   +----------------------------------------------------------------+
| [logo B]                    [Menu] |   | [logo B]     Services  Sectors  About  Contact  DE|EN  [Book a call] |
| H1: Find the process that costs    |   |                                                                |
|     you time, and fix it ...      |   | H1: Find the process that costs you time, and fix it ...      |
| |<------ half an hour ------>|     |   | |<--------------- half an hour --------------->|                |
| Analysis, automation ...           |   | Analysis, automation ...                                       |
| [Book a free 30-minute call]       |   | [Book a free 30-minute call]   Send a message                  |
+------------------------------------+   +----------------------------------------------------------------+
```

## 2. Scoring

Scores 1 to 5 on the eight criteria in the brief. A, B, C and D are scored from the screenshots and from the assessment in the brief (D was re-viewed at 1440 and 390 px on 2026-11-21). The three new directions are scored before the build, so they are predictions. The chosen direction is re-checked at checkpoint 2 and the final checks.

| Option | Professional and trustworthy | Modern | Stands out | Fits Swiss market | Offer and booking clear on phone | Finished without photos | Accessible | Buildable as static site | Total |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A, calm | 4 | 2 | 1 | 3 | 5 | 2 | 4 | 5 | 26 |
| B, structured | 4 | 2 | 3 | 3 | 3 | 3 | 4 | 4 | 26 |
| C, bold | 2 | 3 | 4 | 2 | 4 | 3 | 3 | 5 | 26 |
| D, balanced | 4 | 3 | 2 | 3 | 5 | 3 | 4 | 5 | 29 |
| 1, Drawing sheet | 5 | 4 | 4 | 4 | 5 | 4 | 5 | 5 | 36 |
| 2, Product fragments | 4 | 4 | 4 | 3 | 4 | 3 | 4 | 4 | 30 |
| 3, Measured | 4 | 5 | 4 | 4 | 5 | 4 | 4 | 4 | 34 |

Direction 1 against D, criterion by criterion: professional (5 against 4, win); modern (4 against 3, win); stands out (4 against 2, win); fits Swiss market (4 against 3, win); phone (5 against 5, tie); finished without photos (4 against 3, win); accessible (5 against 4, win); buildable (5 against 5, tie). Six wins, so it passes the rule.

Two points are predictions and need checking: accessible 5 depends on the build meeting the contrast table above and visible focus everywhere; finished 4 depends on the figures reading well at 390 px. If checkpoint 2 shows either is wrong, the rule is re-run before the build continues.

Direction 3 would also have passed the phone and buildable ties but wins only four criteria against D, so it fails the rule.

## 3. Chosen direction: specification

### 3.1 Tokens

All values are CSS custom properties on `:root` in `css/style.css`.

| Token | Value | Use |
| --- | --- | --- |
| `--ink` | `#000000` | Text, primary rules, logo |
| `--paper` | `#ffffff` | Sheets, form fields |
| `--drawing` | `#f4f4f1` | Page background |
| `--concrete` | `#d6d7d2` | Decorative rules, figure fills (not text) |
| `--note` | `#4a4b47` | Secondary text |
| `--field-line` | `#6b6b66` | Form field borders |
| `--marker` | `#ebc34d` | Primary button fill, "after" marks in figures |
| `--rust` | `#9e3d1b` | Problem marks, the problem label |
| `--error` | `#b42318` | Form error text and borders |
| `--font-sans` | Archivo, fallback stack from section 1.1 | All text |
| `--wdth-head` | 100 | Headlines |
| `--wght-head` | 700 | Headlines |
| `--wdth-label` | 75 | Labels, captions, form labels |
| `--wght-label` | 500 | Labels, captions, form labels |
| `--size-h1` | 36 px phone / 52 px desktop | H1 |
| `--size-h2` | 28 px / 36 px | H2 |
| `--size-h3` | 22 px / 26 px | H3 |
| `--size-body` | 17 px / 18 px | Body |
| `--size-label` | 15 px | Labels and captions (never below 15 px) |
| `--lh-head` | 1.1 | Headlines |
| `--lh-body` | 1.55 | Body |
| `--space-1` to `--space-8` | 4, 8, 12, 16, 24, 32, 48, 80 px | Space scale |
| `--radius` | 0 | Sheets, figures, fields, buttons: square corners |
| `--radius-button` | 4 px | Buttons only (the brief's button radius) |
| `--measure` | 620 px | Text column maximum width |
| `--stroke` | 1.5 px | Figure strokes |
| `--rule` | 1 px | Ruled lists and sheets |
| `--focus` | 2 px Ink outline, 2 px offset | Focus on every control |
| `--target` | 44 px | Minimum tap target |

Rules: no shadows; no gradients; no photographs; yellow never carries text; Rust is never used for a button or a link.

### 3.2 Components and states

| Component | States | Notes |
| --- | --- | --- |
| Logo | Light (on Paper and Drawing paper), dark (on Ink), icon (favicon and touch icon) | Option B SVGs, copied unchanged. The original PNG is the fallback on light backgrounds |
| Header, desktop | Default, current page (Ink underline 2 px), hover (underline 2 px), focus | Links: Services, Sectors, About, Contact; language switch; "Book a call" button |
| Menu button, phone | Default, focus, open (aria-expanded true) | 44 by 44 px, nothing on top of it |
| Phone menu | Closed, open | Full-screen Paper sheet; Escape closes; focus moves in; current page bold with a 4 px Marker bar |
| Primary button | Default (Marker fill, Ink text, Archivo 600 17 px, 48 px tall, 2 px Ink border), hover (Ink fill, Paper text, 21.00:1), focus, disabled (Drawing fill, Note text) | Yellow button edge is Ink, so it does not depend on Marker against the page |
| Secondary action | Default (Ink text, 1 px underline), hover (2 px underline), focus | Text link, never a second filled button |
| Title block | Default only | Four cells; the Next step cell holds the primary button; used once per page |
| Figure | Default; animated once (drawn) under motion; static under reduced motion | Captions "Fig. n" in label style |
| Ruled list | Default, focus on links | 1 px Concrete rules (decorative), 16 px row padding |
| Form field | Default (48 px, 1 px field line), focus (2 px Ink), error (2 px Error, message under field starting with what to do), filled | Labels above; sentence case |
| Footer | Default | Paper background, 1 px rule above, every link 44 px tall |

### 3.3 Figure rules

- Stroke 1.5 px Ink (before state: Note, dashed 4 4). Square corners, no fills except Marker on one changed element per figure.
- Labels in label style, Ink, 15 px minimum at 1x.
- Every figure has an `aria-label` describing the process in one sentence and a `<figcaption>` ("Fig. n").
- Figures scale with width (`viewBox`), never fixed px at phone widths.
- One figure per page on Home, at most two on any page.

### 3.4 Page-by-page section plans

Home: header; first screen (H1, supporting line, title block with Process "Quality reports" and Today "assembled by hand", as in the copy bank); Fig. 1 before and after; the four steps as a numbered ruled list; services as ruled rows; sectors as two ruled columns (no cards); the closing block (the only centred element); footer. [[draft]] and [[supply: ...]] notes as in the brief.

Automation & Digital Workflows: first screen (H1 "Automation with the licences you already pay for", title block with Process "Approvals and inspections"); where it fits; Microsoft 365 backbone; how a project runs; proof (hidden until supplied); closing.

Contact: first screen (H1, two ruled sheets with the booking sheet first on phones); form with error state and confirmation; address sheet; footer.

Phone menu, 404 page, Impressum, Privacy: as in the brief.

### 3.5 What must not drift

- The title block appears once per page and holds one interactive element: the primary button.
- Yellow is the primary button fill and the "after" mark only.
- No shadows, gradients, photographs or device mock-ups.
- No card boxes: sectors and services are ruled lists.
- Every heading is flush left. The closing block is the only centred element.
- Figures are drawn from the visitors' documents, not from ketztek software; no screenshot of a product is shown unless it is real.

## 4. Checkpoint 1 scope

Built on branch `design/option-e` in `ketztek-demo`: the token sheet (section 3.1), the header with the proposed logo, the Home first screen (section 1.1 wireframe) and its title block, the primary button and secondary action states. The draft marker for the logo is shown once and disappears under `?clean`. Screenshots at 390 by 844 and 1440 by 900 are in the session scratchpad, not in the repositories.

## 5. Status (2026-11-22)

Built and pushed:

- Drawing sheet: branch `design/option-e` in `ketztek-demo`, last commit `ecb0e01`. Home, Automation, Contact (form and error state), phone menu and 404 checked at 390 and 1440 px in the clean view.
- Measured: branch `design/option-e-measured`, last commit `0c896a9`. Chosen after the drawing sheet was judged too close to Rapport. Home only.
- Demo `main`: one site with three options. The root is a chooser, Rapport is in `rapport/`, and the other two are in `drawing-sheet/` and `measured/` (commit `d908199`). Live at <https://ketztek-demo.vercel.app>. The README has the details.
- Audit `main`: the research, this spec and the Stitch prompt are merged (commit `cd0ac84`). The current Stitch prompt is `ketztek-stitch-prompt.md` in this folder.

Not done:

- The section 8 checks have not run on any option: contrast on every pair, tap targets, focus order, reduced motion, and the sideways-scroll sweep.
- No diagram-led reference was verified for the reference board (section 5.3 of the research file).
- Best of Swiss Web gave one B2B winner; the brief asks for five.
- The drawing sheet's accessibility (5) and finished-without-photos (4) scores are predictions, not measurements.
- Only Home was reviewed for the measured option. The service pages, About, Impressum, Privacy and German Home were not reviewed for any option.
- The German copy is a draft, and only the headline and button have German text.
- Nothing has been shared with ketztek.

Deployment:

- Vercel SSO protection has been off for the `ketztek-demo` project since 2026-11-22, so previews and production are public. Git fork protection is still on.
- Preview deployments of `design/option-e` were made before later changes and are out of date. Redeploy from a branch to refresh one.
