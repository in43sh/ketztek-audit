# UX Design Audit Report: ketztek.com

**Scope:** usability of the public website, evaluated fresh against 15 usability principles, independently of the earlier presence and design audits in this repository.

**Source (fetched 2026-11-21, 10:32Z-10:40Z UTC):**

- [ketztek.com](https://ketztek.com/) (home)
- [ketztek.com/expertise/](https://ketztek.com/expertise/)
- [ketztek.com/contact/](https://ketztek.com/contact/)
- [ketztek.com/privacy-policy/](https://ketztek.com/privacy-policy/)
- `https://ketztek.com/this-page-does-not-exist-ux/` (the 404 page)
- The Microsoft Bookings page the booking buttons lead to, and `http://www.ketztek.ch/`, linked from the privacy page

**Interface type:** marketing site for a B2B consultancy (process analysis, automation, custom software). Primary flows: understand the offer, book a free 30-minute call, or send a message.

**How it was checked:** raw HTML for structure; a real Chromium browser at 390 px (iPhone user agent, touch) and 1440 px for rendered layout, computed styles, taps, hover, keyboard focus, the mobile menu dialog, the language switch and the embedded booking calendar. Requests spaced 10 s apart, as the site's `robots.txt` asks.

**Limitations:**

- The contact form was not submitted, so its validation messages, success message and spam check after submission were not observed.
- The spam-check widget (Cloudflare Turnstile) and the Google translation service may behave differently in an automated browser than for a visitor.
- Screen readers were not used; accessibility findings come from markup and computed styles.

## How to Read This Report

Findings are rated on a 0-4 severity scale (4 = users can't complete tasks, 1 = cosmetic only). Each finding references an established usability principle. Start from the top: the most impactful issues are listed first.

## Summary

| Severity | Count |
| --- | --- |
| 4 - Catastrophe | 1 |
| 3 - Major | 6 |
| 2 - Minor | 12 |
| 1 - Cosmetic | 5 |
| **Total findings** | **24** |

## Quick Wins

1. Phone menu cannot be opened (Severity 4): move the EN/DE switcher out from on top of the menu button.
2. "Expertise" and "Services" menu links do nothing off the home page (Severity 3): point them to `/expertise/` and `/#services`.
3. Closing "Book a 30-minute call" button does nothing (Severity 3): give it the booking link.
4. Contact form wider than phones (Severity 3): make the fields `width: 100%`.
5. Secondary buttons look like the primary one (Severity 2): give "Write to us" an outline style.

## Findings

### [Severity 4] The phone menu cannot be opened

- **Principle:** Affordances and Signifiers; Structure; Accessibility
- **Location:** header on every page at phone widths (390 px tested); the "Open menu" button and the fixed language switcher `div.gt_switcher_wrapper`
- **Issue:** The EN/DE language links sit on top of the 24 x 24 px menu button. A tap at the button's centre lands on "EN"; the menu stays closed (tested on Contact). The footer has only Privacy Policy and Impressum, so on any page but Home there is no other way to reach the rest of the site.
- **User impact:** A phone visitor on Contact, Privacy, the 404 page or Expertise taps the menu, nothing happens, and they cannot get to the offer or contact page without editing the address. Most will leave.
- **Fix:** On phones, move the language switcher into the menu dialog or to the left of the menu button with at least 8 px between them. Make the menu button 44 x 44 px. Add Contact and "Book a call" to the footer as a second path.

### [Severity 3] "Expertise" and "Services" in the menu go nowhere except on Home

- **Principle:** Consistency and Standards; Structure; Visibility of System Status
- **Location:** main navigation on every page; links `#homepage-expertise` and `#services`
- **Issue:** Both links are same-page anchors that only exist on the home page. On Expertise, Contact, Privacy and the 404 page, clicking them does nothing at all. The dedicated `/expertise/` page is linked from nowhere except itself.
- **User impact:** A visitor on the contact page who wants to check what the firm does clicks "Expertise" or "Services", nothing happens, and they conclude the site is broken. The best content page is effectively hidden.
- **Fix:** Link "Expertise" to `https://ketztek.com/expertise/` and "Services" to `https://ketztek.com/#services` (full URL, so it works from every page).

### [Severity 3] The closing "Book a 30-minute call" button does nothing

- **Principle:** Visibility of System Status; Affordances and Signifiers; Accessibility
- **Location:** Home, final section "Not sure where to start?"
- **Issue:** The button is an `<a>` without an `href`. It looks exactly like the working booking button above it but has no destination, and it is skipped entirely by keyboard Tab.
- **User impact:** The visitor who read the whole page and is ready to book taps the most important button and nothing happens, with no feedback. They must scroll back up to find a working one, or give up.
- **Fix:** Add the booking URL (the same one as "Book a free 30-minute call") and keep the label identical to it.

### [Severity 3] No booking button on the first screen

- **Principle:** Aesthetic and Minimalist Design; Perceptibility
- **Location:** Home, first screen at 390 and 1440 px
- **Issue:** The first screen shows the logo in the header, the same logo again at 547 px wide over a marble texture, and the slogan "Making your business run smoother." The first booking button appears only after scrolling a full screen; the only controls on the first screen are the menu, EN and DE.
- **User impact:** A busy manager landing from a search or a referral learns neither what the firm does nor what to do next without scrolling. The repeated logo spends the most valuable space on nothing new.
- **Fix:** Replace the second logo with a short headline that says what ketztek does for whom (as an `h1`), one supporting line, and the "Book a free 30-minute call" button, all inside the first phone screen.

### [Severity 3] The contact form is wider than a phone

- **Principle:** Structure; Accessibility; Error Prevention
- **Location:** Contact, "Write to us" form at 320 to 390 px
- **Issue:** The form fields keep a fixed width (`size="40"`), so the page lays out at 392 px on a 390 px phone and 390 px in a 320 px window. The Message box runs past its white card and off the right edge of the screen.
- **User impact:** On the page where enquiries start, the layout wobbles sideways and part of the message box is cut off, so people can't see the end of the lines they type. It looks broken and invites the visitor to leave.
- **Fix:** Give form fields `width: 100%; box-sizing: border-box;` inside the card.

### [Severity 3] Choosing German shows "DE" as active but the page stays in English

- **Principle:** Visibility of System Status; Perceptibility; Match Between System and Real World
- **Location:** EN/DE switch in the header (GTranslate), tested on Home at 1440 px
- **Issue:** After a click on "DE", the switch immediately marks DE as current (bold), but the page text stayed English for the 15 seconds observed, with no loading indicator. The links are `href="#"` and the address does not change, so there is no German page to bookmark or share. The switch relies on a third-party machine translation, which may work in other browsers but gives no feedback either way.
- **User impact:** A German-speaking visitor, most of the firm's likely audience, asks for German, is told they have it, and keeps reading English. They can't tell whether to wait, retry or give up.
- **Fix:** Short term: show progress while translating, and only mark DE as current once the text has changed. Better: publish real German pages at their own addresses and link the switch to them.

### [Severity 3] Inner pages have no side margins and very long lines

- **Principle:** Aesthetic and Minimalist Design; Structure
- **Location:** Expertise (all widths), Privacy (390 px, and the right edge at 1440 px)
- **Issue:** Text starts at 0 px from the screen edge on Expertise at 390 and 1440 px and on Privacy at 390 px. On desktop, Expertise lines run to a median of 138 and a maximum of 155 characters; Privacy to a median of 101. Home uses 20 px and 108 px margins and Contact 20 px and 60 px, so every template has a different left edge.
- **User impact:** On phones, text touching the glass is hard to read and looks broken. On desktop, readers lose their place moving from the end of a 150-character line to the start of the next, so the page that explains the firm's skills is the most tiring one to read.
- **Fix:** Give every template the same content container: 20 px side margins on phones, a text column of about 65-75 characters (around 680 px at 18 px), and a left edge aligned with the header logo.

### [Severity 2] Secondary buttons look exactly like the primary one

- **Principle:** Affordances and Signifiers; Aesthetic and Minimalist Design
- **Location:** Home, "Find where your processes lose time." ("Book a free 30-minute call" with "Write to us") and the closing section ("Book a 30-minute call" with "Or just send us a message")
- **Issue:** Both buttons in each pair are solid near-black with white 16 px text and 5 px corners.
- **User impact:** Visitors get two equal choices instead of one clear next step, which slows the decision and splits attention away from booking.
- **Fix:** Keep booking as the solid primary button; make "Write to us" an outline or text link.

### [Severity 2] The booking step is confusing once you get there

- **Principle:** Match Between System and Real World; Consistency and Standards; User Control and Freedom
- **Location:** booking buttons on Home, and the embedded calendar on Contact (Microsoft Bookings)
- **Issue:**
  - The site promises "a free 30-minute call", but the booking page asks the visitor to "Select a service" from four cards. The first is "Demo Software" with no description; the free consultation is third.
  - Service names are cut off with "…".
  - The buttons send the visitor to Microsoft's site in the same tab, with no hint that they are leaving.
  - On Contact, the calendar is a 710 px framed area that scrolls inside the page on phones.
- **User impact:** Someone who clicked "free call" meets a different set of options, may pick the wrong one or hesitate, and on a phone has to scroll a box within the page.
- **Fix:**
  - In Bookings, hide "Demo Software" and put the free consultation first, with a short name.
  - Link the site's buttons straight to that service if Bookings allows it.
  - On Contact, show a button that opens the calendar instead of the embedded frame.

### [Severity 2] The contact form asks for the wrong things and hides which are required

- **Principle:** Error Prevention; Match Between System and Real World; Consistency and Standards
- **Location:** Contact form
- **Issue:**
  - Name, E-Mail and Subject are required (`aria-required="true"`), but Message is optional, and nothing on screen marks required fields.
  - The submit button reads "Submit" and is an unstyled browser-default button (grey, 13.3 px, square corners), unlike every other button on the site.
  - The message is capped at 2,000 characters with no counter.
- **User impact:** People find out what is required only after an error. A "Subject" is unusual friction for a first message, while an empty message is accepted. The plain grey button looks unfinished at the moment trust matters most.
- **Fix:**
  - Require Message and make Subject optional (or drop it).
  - Mark required fields.
  - Rename the button "Send message" and style it as the primary button.
  - Add a character counter near the limit.

### [Severity 2] Phone body text is small on the main pages

- **Principle:** Aesthetic and Minimalist Design; Accessibility
- **Location:** Home, Expertise, Contact and 404 at 390 px
- **Issue:** Paragraph text is 14.5 px on these pages (14.2 px on the 404 page), while Privacy uses 16.2 px. Line height is 1.4.
- **User impact:** The pages that explain and sell are harder to read than the legal page, especially outdoors or for older readers, who are likely among plant and site managers.
- **Fix:** Set body text to a 16 px minimum on phones, growing to 18 px on desktop, the same on every template.

### [Severity 2] Text alignment keeps switching sides

- **Principle:** Structure; Aesthetic and Minimalist Design
- **Location:** Home ("Why work with us", "Sectors", the closing section), Expertise headings, Contact ("Book a call"), footer
- **Issue:** On Home, 17 text blocks are left-aligned, 10 centred and 8 right-aligned. "Why work with us" alternates right-aligned headings with right-aligned or centred paragraphs. Expertise alternates hard-left and hard-right headings.
- **User impact:** Each block starts at a different edge, so the eye has to hunt for the next line. Right-aligned paragraphs of four or more lines are noticeably harder to read, and the trust section is the one that suffers.
- **Fix:** Left-align all headings and running text; keep centring for at most one short closing call to action.

### [Severity 2] The menu gives no feedback on hover and no sign of the current page

- **Principle:** Visibility of System Status; Perceptibility; Affordances and Signifiers
- **Location:** main navigation (desktop) and the phone menu dialog; primary buttons
- **Issue:**
  - Menu links do not change at all on hover: same color, weight and underline.
  - The current page carries `aria-current="page"` but looks identical to the other links, on desktop and in the phone menu.
  - The primary button's hover darkens it from `#1c1c1c` to `#121212`, a difference too small to see.
- **User impact:** Visitors get no confirmation that a link is live or where they are, which adds to the uncertainty caused by the dead menu items above.
- **Fix:** Underline or color-shift menu links on hover. Give the current page a visible marker, for example an underline or bold. Make the button hover clearly different, for example by lightening it or adding a yellow underline.

### [Severity 2] Expertise boxes look like buttons but do nothing

- **Principle:** Affordances and Signifiers
- **Location:** Home, "Expertise" section (six boxes with a 4 px purple border)
- **Issue:** The boxes ("Software Engineering", "Cloud" and four more) have heavy button-like outlines but are plain paragraphs: no link, default cursor. Meanwhile the real Expertise page is not linked anywhere.
- **User impact:** Visitors tap or click them expecting details, nothing happens, and the details they wanted stay out of reach.
- **Fix:** Make each box a link to the matching section of `/expertise/`, or, if they stay static, remove the borders so they read as a list.

### [Severity 2] The privacy page links to a website that returns an error

- **Principle:** Error Recovery; Consistency and Standards
- **Location:** Privacy Policy, introduction and section 1 (`http://www.ketztek.ch/`, twice)
- **Issue:** Both links lead to a server error page (HTTP 500 at 10:38Z).
- **User impact:** A visitor checking who runs the site follows the link and lands on an error, which undermines trust on exactly the page meant to build it.
- **Fix:** Point the links to `https://ketztek.com/`, and fix or redirect `www.ketztek.ch`.

### [Severity 2] Headings do not describe the page structure

- **Principle:** Accessibility; Perceptibility
- **Location:** all pages
- **Issue:**
  - Home has no `h1`; its sections start at `h3`, styled as large as the one `h2`.
  - On every page, `h1` and `h2` render at the same size (33.3 px phone, 48 px desktop).
  - Inner pages jump from `h1` to `h3`.
  - Expertise, Contact and Privacy have no `<main>` landmark.
  - The menu is labelled "Menü" (German) on English pages.
- **User impact:** Screen-reader users can't jump to the main content or navigate by heading levels. Sighted users skimming headings see every section shout equally, so nothing guides the eye to the offer.
- **Fix:**
  - One `h1` per page (on Home, the offer headline), `h2` for sections, `h3` below; a visible size step between levels.
  - Wrap the page content in `<main>`.
  - Label the menu "Menu".

### [Severity 2] The 404 page offers only a search box

- **Principle:** Error Recovery; Help and Documentation
- **Location:** any missing URL
- **Issue:** The page says "404 – Page Not Found / Search below to find what you're looking for." with a search field, the theme's default text. There are no links to Home, the services or Contact, and on phones the menu cannot be opened (see Severity 4).
- **User impact:** Someone following an old or mistyped link on a phone is stuck with a search box on a six-page site.
- **Fix:** Replace the search with two links: "Go to the home page" and "Book a free 30-minute call".

### [Severity 2] Small tap targets on phones

- **Principle:** Affordances and Signifiers; Accessibility
- **Location:** phone menu dialog (links 22 px tall), footer ("Privacy Policy" 84 x 15 px, "Impressum" 66 x 15 px), EN and DE (20 x 17 px), the menu button (24 x 24 px)
- **Issue:** These targets are well under the 44 x 44 px touch guideline, and EN and DE sit directly next to the menu button.
- **User impact:** Mis-taps, especially on the language links next to the menu button, where a mis-tap is exactly what breaks the menu.
- **Fix:** Pad menu, footer and language links to at least 44 px of tap height, with 8 px between neighbours.

### [Severity 2] Nothing tells the visitor what happens after they reach out

- **Principle:** Help and Documentation; Visibility of System Status
- **Location:** Contact page, booking buttons
- **Issue:** The site promises "a real answer, not a brochure" but gives no response time, no outline of what the free call covers or what follows it, and no phone number or hours.
- **User impact:** Cautious buyers hesitate to book or write because they don't know what they are committing to or when they'll hear back.
- **Fix:** Add one line under each path, for example "We reply within one working day" and "In 30 minutes we look at one process and tell you honestly whether it's worth fixing", using the operators' real terms.

### [Severity 1] Two unrelated accent colors

- **Principle:** Consistency and Standards; Aesthetic and Minimalist Design
- **Location:** Home ("Expertise" boxes, "Industry & Manufacturing" and "Construction" headings, the five service icons)
- **Issue:** The logo's accent is yellow, but a purple (`#9b51e0`, WordPress's built-in "vivid purple") colors the Expertise box borders and text, two sector headings and the icons. Body text also uses four slightly different near-blacks (`#0f0f0f`, `#1c1c1c`, `#2c2c2c`, `#3a3228`).
- **User impact:** The page feels assembled from parts rather than designed. Purple on non-clickable boxes also strengthens the false "button" impression.
- **Fix:** Use one accent (the logo yellow, behind dark text) and one text black; turn icons and sector headings to the text color.

### [Severity 1] Services and expertise make the phone page very long

- **Principle:** Aesthetic and Minimalist Design; Structure
- **Location:** Home at 390 px, "What we offer" and "Expertise"
- **Issue:** The phone home page is about 6,870 px tall. Five identical centred cards take about 1,000 px, and six full-width boxes follow; card text is centred over several lines.
- **User impact:** Visitors scroll a long way past repeated card frames before reaching the reasons to trust the firm and the closing call to action; centred multi-line text is slower to read.
- **Fix:** Show services as a left-aligned list (icon, name, one line) and expertise as a compact two-column list on phones.

### [Severity 1] The home page's title says only "ketztek"

- **Principle:** Match Between System and Real World; Recognition Over Recall
- **Location:** `<title>` on Home; no meta description and no share image on any page
- **Issue:** The browser tab, bookmark and search result for the home page read "ketztek"; links shared in email or chat show no preview.
- **User impact:** People comparing several tabs or search results can't tell what ketztek does without opening it.
- **Fix:** Title along the lines of "ketztek – process automation and software for industry and construction, Winterthur"; add a description and a share image.

### [Severity 1] Odd line breaks from pasted non-breaking spaces

- **Principle:** Aesthetic and Minimalist Design
- **Location:** Home (82 non-breaking spaces in the markup), Expertise (63), Contact (21)
- **Issue:** Words glued together with non-breaking spaces force early line breaks, leaving half-empty lines on phones (for example "built to be maintained — with / tests" on Expertise).
- **User impact:** Ragged text looks careless on a site selling precision.
- **Fix:** Replace them with normal spaces, except between numbers and units.

### [Severity 1] Every home section fades in on scroll

- **Principle:** Aesthetic and Minimalist Design
- **Location:** Home, all sections (31 text elements hidden until scrolled into view)
- **Issue:** A uniform entrance animation runs on every section. The site does include a `prefers-reduced-motion` rule.
- **User impact:** Fast scrollers briefly see empty space; the motion draws attention to nothing in particular.
- **Fix:** Remove the section animations, or keep a single one on the first screen.

## Strengths

- **Labelled, sensible form fields.** Every field has a visible label wrapped around it, Name and E-Mail have `autocomplete` hints and the e-mail field uses `type="email"`, so phones offer the right keyboard and autofill (Error Prevention, Accessibility).
- **A well-built menu dialog once open.** It is a proper `role="dialog"` with `aria-modal`, moves focus to the first link, has a labelled close button and closes with Escape (User Control and Freedom, Accessibility).
- **Readable color contrast.** No text failed WCAG contrast on any of the five pages at either width (Accessibility, Perceptibility).
- **Visible keyboard focus.** Every control reached by Tab shows a focus outline, and a "Skip to content" link comes first (Accessibility, Flexibility and Efficiency).
- **Respect for user settings.** Page language is declared, zoom isn't blocked, and the animations have a reduced-motion rule (Accessibility, Flexibility).
- **Clear, human copy.** Headings and text speak the visitor's language ("Let's talk about the process that annoys you most") instead of jargon, and the form's markup includes a sending spinner (Match Between System and Real World, Visibility of System Status; not observed, since the form was not submitted).
- **A working, calm visual base.** The wordmark, sand and white backgrounds and the Inter and Instrument Sans pairing are worth keeping; most fixes above work within them.

## Evidence log

| Time (UTC) | Check |
| --- | --- |
| 10:32:13-10:32:57 | Raw HTML of the five pages (200, 200, 200, 200, 404) |
| 10:33:59-10:34:45 | Phone menu tap, menu dialog, Escape, booking frame, Turnstile (Contact 390 px); hover, current page, focus, booking link (Home 1440 px) |
| 10:35:27-10:38:39 | Computed styles, taps, margins and screenshots of the five pages at 390 and 1440 px |
| 10:38:55 | `http://www.ketztek.ch/` returned 500 |
| 10:40:24 | DE language switch timed on Home (no change in 15 s) |
