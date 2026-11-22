# Prototype acceptance checks

Checks from section 13 of `ketztek-design-prompt.md` (this folder), run on 2026-11-21 against the "Rapport" prototype in the sibling `ketztek-demo` repo. The prototype was built from the design prompt alone, to test whether a coding agent can work from it.

## How the checks were run

- A Playwright script opened every page from the local files in full Chromium, with a phone user agent and touch at phone widths, and waited for the fonts to load.
- Pages checked: Home, German Home, the five service pages, About, Contact, Impressum, Privacy and 404 (12 in all).
- Widths: 390 and 1440 px for most checks; 320, 360, 768 and 1024 px as well for sideways scrolling; 360 px as well for the menu.
- The checks ran on the annotated view (draft and supply notes visible) unless a row says otherwise.
- Screenshots of the results are in `ketztek-demo/screenshots/`.

## Results

| # | Check | Result | How it was checked |
| --- | --- | --- | --- |
| 1 | H1 and booking button visible without scrolling | Pass | Home, Automation and Contact at 390 x 844 and 1440 x 900: both elements end inside the window. |
| 2 | Logo exactly once on each first screen | Pass | Visible logo images counted inside the first window, same pages and widths. |
| 3 | Phone menu opens from a tap at its centre, closes with its button and Escape | Pass | At 360 and 390 px: hit test at the button centre returns the menu button (83 x 44 px); tap opens it, focus moves inside, the close button and Escape both close it. |
| 4 | Every link and button works; booking buttons open Microsoft Bookings in a new tab | Pass | 327 links checked: local targets exist on disk, `#` anchors exist on the target page, booking links point to Microsoft Bookings with `target="_blank"` and `rel="noopener"`. Contact form at 390 px: an empty submit marks the three required fields and focuses Name; a bad email is flagged; a valid submit hides the form and focuses the confirmation; no network request. |
| 5 | Body text at least 17 px (390) and 18 px (1440) | Pass | Computed font size of every running-text paragraph in `main`. |
| 6 | No running-text line over 75 characters at 1440 px | Pass | Characters per rendered line for every paragraph and list item over 120 characters. The only hit is a 76-character supply note on the German page, which is an annotation, not running text. |
| 7 | Contrast as in section 5; Marker never a text colour | Pass | WCAG ratio for every text element against its painted background; no failures. No text uses `#ebc34d`. |
| 8 | No sideways scrolling at 320 to 1440 px | Pass | Document width compared with the window at 320, 360, 390, 768, 1024 and 1440 px on every page, Contact included. |
| 9 | All text left-aligned except the closing block | Pass | Computed `text-align` of every text element. The only centred text is inside button labels (booking buttons, Menu, Send message). |
| 10 | Visible focus outline in a logical order | Pass | 29 Tab presses each on Home and Contact; every stop had an outline. Order: skip link, logo, navigation, language, Book a call, then the page content. |
| 11 | Tap targets at least 44 x 44 px | Pass | Menu button, buttons, form fields and footer links on Home, Contact and Automation at 390 px. |
| 12 | Only the section 5 palette | Pass | Computed text, background and border colours of every visible element, compared with the eight palette values. |
| 13 | No stock photo, mock-up, gradient or shadowed card | Pass | No `box-shadow`, no gradient backgrounds, and no images other than the logo. |
| 14 | Work-report block once per page, one interactive element | Pass | At most one report block per page; each holds exactly one link or button. |
| 15 | German drafts do not break a heading or button | Pass | Nothing is clipped and nothing scrolls sideways at 390 or 1440 px. The German button label wraps to two lines (58 px tall). With the original German H1 (102 characters, seven lines) the button ended at 828 px of 844 in the clean view. With the shortened H1 (91 characters, six lines) it ends at 789 px. With the notes visible it ends at 859 px, because the "native review" note takes its own line; the prompt now says to judge first-screen checks with notes hidden. |
| 16 | Nothing animates under reduced motion | Pass | One animation (the Next-step bar) runs normally; with `prefers-reduced-motion: reduce` none run. |
| 17 | Every draft and supply marker visible or listed here | Pass | All 23 draft markers have a dashed note on their page. Three supply items have no place on a page and are listed below. |

## Supply items with no place on a page

- A price cue or typical project size, if the business wants to show one (prompt section 3).
- The logo as SVG or PDF, to replace the PNG (prompt section 6).
- Confirmation of the official yellow; the prototype uses `#ebc34d`, sampled from the logo files (prompt section 6).

## Bug found by the checks

The first form test failed: after correcting an email error, a click on Send message did nothing. On mousedown the field lost focus, its error message disappeared, the button moved up and the click landed on empty space. Errors now clear while the visitor types (`ketztek-demo/js/site.js`), and the test passes.

## Deviations from the prompt (since fixed in the prompt)

- **Primary button hover:** the prompt asks for Ink fill with Marker text. That breaks the prompt's own rule that Marker is never a text colour, and check 7. The prototype uses Ink fill with Paper text.
- **Next-step row:** the prompt asks for a Marker band behind the button area, but the button is Marker too, so it would be yellow on yellow. The prototype marks the row with a 4 px Marker bar on its left edge.
- **Booking link:** the prompt leaves the Microsoft Bookings link as a supply item. The prototype uses the current public booking page from the research file, so that no booking button is dead.
- **Column width:** the prompt says 680 px is about 70 characters. In Archivo at 18 px, 680 px measured 77 to 78 characters, which fails check 6, so the column is 620 px.
- **German first screen:** the prompt's German H1 draft was 102 characters, against 81 in English, and ran to seven lines at 36 px, leaving 16 px on the first phone screen. The prompt now has a 91-character draft ("…mit Ihren eigenen Werkzeugen."), which takes six lines; the prototype uses it.
