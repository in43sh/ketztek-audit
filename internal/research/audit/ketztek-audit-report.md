# ketztek GmbH (ketztek.com): Web Presence Audit and Plan

## About this run

| Item | Value |
| --- | --- |
| Business | ketztek GmbH, a process analysis, automation and custom software consultancy for industrial and construction companies. Name used everywhere in lower case ("ketztek"). |
| Address | Schulergasse 9, 8406 Winterthur, Switzerland (site footer, Impressum, UID register, Google Maps, local.ch). Service area: "working across Switzerland" (home page). |
| Website | `https://ketztek.com/` (WordPress). `ketztek.ch` apex redirects to it; `www.ketztek.ch` is broken (F-02). |
| Slug | `ketztek` |
| Audit date | Friday 2026-11-20, Europe/Zurich (CET, UTC+1). Measurements carry UTC stamps on 2026-11-20 between 11:26Z and 11:51Z. |
| Prior audit | None (first run) |
| Lens | Primary A.1 (lead-gen service): conversions are a booked initial consultation, a contact-form enquiry and an email. No secondary lens. |
| Scenario | Freelancer approaches the business as a **prospect**. Nobody at the business was contacted. What the operators want from their web presence is unknown. |
| Report audience | Internal (freelancer). A separate client report is at `client/reports/ketztek-client-report.md`. |
| Capabilities | Browser (Playwright, signed out, phone emulation), `curl`, `dig`, `whois`, `openssl`, Lighthouse 13.6.0 via `npx`, Wayback CDX API, Google autocomplete endpoint, harness web search (leads only). No Search Console, analytics, hosting or WordPress access. |
| Languages read directly | English and German. German copy judgements are mine, not a native Swiss German speaker's; marked Medium confidence where they matter. |

Inputs settled from public sources (Section 0 gave only the URL): business name and address from the site, the federal UID register and Google Maps. Assumptions carried into section 12:

1. **Business goal (assumed):** more booked initial consultations ("Book a free 30-minute call") and more contact-form or email enquiries from Swiss industrial and construction SMEs. To be confirmed.
2. **Audience language (assumed):** German first. Winterthur is in German-speaking Switzerland, the contact form runs in locale `de_CH`, the booking page is bilingual, and 23 of 45 German autocomplete seeds returned the exact query against 0 of 6 English ones (section 6). English is a second audience (international staff, English-speaking managers).
3. **Seasonality:** none evidenced. B2B budget cycles around year-end are an assumption only.
4. **Section 0.1 (decisions already made):** none supplied.
5. **Freelancer's platform:** the Section 0 default (modern framework plus headless CMS, no WordPress) is assumed. It matters less than usual here: the operators are themselves software engineers (F-05 context, section 10).

Labels: `[FACT]` read on a source, `[INFERENCE]` follows from facts with the step stated, `[UNVERIFIED]` not confirmed. "Needs a website: Yes" means the fix needs a change to the site's pages, theme or settings; "No" means a change to DNS, listings, a third-party service or operations.

## 1. Executive summary

**Operating status: `APPEARS ACTIVE`.** The UID register shows the GmbH active in the commercial register, last validated 17.09.2026. The site's Expertise page was published 2026-10-30 and the Impressum edited 2026-10-28 (WordPress REST dates); the `.com` registration was updated 2026-11-08 and the Microsoft Bookings page is live with four services. No reviews, posts or press exist, so this verdict rests on registry and first-party signs (see 0.2 notes in the appendix).

**Site mode: A, LIVE.** `ketztek.com` returns HTTP 200 over valid HTTPS and carries the company's own Impressum and UID.

**Verdict.** A young firm (domain created 2025-11-07) with well-written, specific English copy, a working booking calendar and a fast, current WordPress install. It loses enquiries through small, cheap faults: phone visitors cannot open the menu (F-01), the published `www.ketztek.ch` address errors (F-02), the closing "Book" button is dead (F-03). Bigger gaps: no German pages for a German-speaking market (F-04) and no proof of past work (F-05). No Critical finding; five High.

**Top 5 problems:** F-01 menu unusable on phones; F-02 `www.ketztek.ch` returns a server error; F-03 dead closing booking button; F-04 English-only site, machine-translated German; F-05 no references, team or reviews.

**Top 5 opportunities:** German-first pages with real URLs; two or three short case stories; a complete Google profile with phone and photos; one consistent offer name for the free call; basic search metadata (titles, descriptions, schema).

**Keep:** the copy's honest positioning, the free 30-minute call, Microsoft Bookings, Turnstile plus Akismet spam protection, the Impressum with UID, consistent address on every surface, current WordPress core.

**Dated windows:** Christmas Eve Thursday 2026-12-24 (34 days); first working Monday of 2027, 2027-01-04 (45 days). Fix F-01 to F-03 before the break; German pages for Q1 2027 (assumed budget season).

**Challenge to a default:** the Section 0 platform assumption does not fit. The site works and the operators can maintain it; no rebuild is supported by the evidence (section 10).

**Expected impact (qualitative):** fewer silent losses on phones and from the `.ch` address; better findability and trust with German-speaking buyers.

## 2. Scorecard

| Category | Score | Justification |
| --- | --- | --- |
| Content | 6 | Specific, honest copy and a strong Expertise page (positive findings). English only (F-04), no proof (F-05), privacy text pasted from an old builder (F-11). |
| UX / Conversion | 4 | Booking and form are two taps from any page, but the phone menu is blocked (F-01), the closing CTA is dead (F-03), nav anchors fail off the home page (F-06), no phone (F-08). |
| Visual identity | 6 | Distinctive logo and calm palette, consistent at 375 and 1440 px. Stock photos and anonymous imagery (F-05); header overlap (F-01). No client material supplied. |
| Performance | 7 | Lighthouse medians 86-98 across 24 runs; CLS 0. Home mobile LCP median 3.29 s over the 2.5 s threshold; contact page 5.8 MB (F-12). |
| Accessibility | 6 | Lighthouse 90-95. Target size, unnamed iframe, heading order, no home H1 (F-15); menu unreachable by touch (F-01). |
| Technical SEO | 4 | Sitemap and canonicals present. Title "ketztek", no meta descriptions on 6 of 6 pages, no schema, placeholder page in sitemap (F-09); German not indexable (F-04). |
| Local SEO | 3 | Google place exists with correct address and website, but no phone, hours, photos or reviews; local.ch unclaimed; no search.ch entry (F-07). |
| Trust / Reputation | 2 | Zero reviews found on any platform, no references, no people by role (F-05). Impressum and UID are the only trust signals. |
| Analytics | 1 | No analytics or conversion tracking loads on any page, although the privacy text names Google Analytics (F-11, F-13). |
| Maintenance and security hygiene | 6 | WordPress 7.1.5 is the current release; TLS valid; DMARC `p=quarantine`. No security headers, `readme.html` public (F-14); `www.ketztek.ch` broken (F-02). |

## 3. Presence inventory and site map

### Presence inventory

Read 2026-11-20 UTC, signed out. "Operators can edit" is `UNVERIFIED` for all.

| Surface | Class | Read result | Key facts |
| --- | --- | --- | --- |
| [ketztek.com](https://ketztek.com/) | Owned | Full | 6 published pages, English, WordPress 7.1.5 |
| [Microsoft Bookings page](https://bookings.cloud.microsoft/book/ketztek1@ketztek.ch/?ismsaljsauthenabled) | Owned (third-party tool) | Full | 4 services, bilingual descriptions (F-10) |
| [Google Maps place](https://www.google.com/maps/search/ketztek+GmbH+Schulergasse+9+Winterthur?hl=en) | Owned (likely) | Limited view | "ketztek GmbH", Software company, Schulergasse 9, website ketztek.com. Prompts "Add place's phone number", "Add hours", "Add a photo". No rating. |
| [local.ch listing](https://www.local.ch/en/d/winterthur/8406/ketztek-gmbh-7bWDg4UHzh9k-DIdRxubPg) | Unclaimed aggregator | Full | Address only, "Unclaimed business", "Source: Swiss Official Gazette of Commerce" |
| [UID register](https://www.uid.admin.ch/Detail.aspx?uid_id=CHE295462558) | Registry | Full | ketztek GmbH, UID active, RC active, LLC, c/o a named individual (not recorded), last validation 17.09.2026, VAT fields empty |
| [search.ch directory](https://search.ch/tel/?was=ketztek) | Directory | Full | 0 entries |
| LinkedIn company page | n/a | Inconclusive | Guessed slug `/company/ketztek` returned 404 and a language chooser signed out. Existence `UNVERIFIED`. |
| Zefix (commercial register) | Registry | Not read | `robots.txt` disallows all. Founding date `UNVERIFIED`. |
| Moneyhouse | Aggregator | Not read | `robots.txt` disallows all |
| Instagram, Facebook, YouTube, Xing | n/a | Not found | No link from the site; not found by search. Absence `UNVERIFIED`. |
| Apple Maps, Bing Places | n/a | Not opened | Listed as a gap |

### NAP matrix

| Field | Site | Google | local.ch | UID register | Bookings |
| --- | --- | --- | --- | --- | --- |
| Name | "ketztek GmbH" (footer, Impressum); title "ketztek" | "ketztek GmbH" | "ketztek GmbH" | "ketztek GmbH" | "ketztek" |
| Address | Schulergasse 9, 8406 Winterthur, Schweiz | Schulergasse 9, 8406 Winterthur | Schulergasse 9, 8406 Winterthur | Schulergasse 9, 8406 Winterthur (c/o a person) | none |
| Phone | none | none | none | n/a | none |
| Email | `info@ketztek.ch` | none | none | n/a | n/a |
| Hours | none | none | none | n/a | slot calendar |
| Website | ketztek.com; privacy text says `www.ketztek.ch` | ketztek.com | none | n/a | n/a |

No mismatch in name or address. The gaps are the missing phone and hours everywhere (F-07, F-08) and the `www.ketztek.ch` reference (F-02).

### Site tree (English only; language-parity table not applicable)

```text
/                     Home (template wpmm-page-template.php), no H1, 689 words
  #homepage-expertise anchor (nav "Expertise")
  #services           anchor (nav "Services")
/expertise/           Expertise, 472 words; not linked from nav or home (orphan, F-06)
/contact/             Contact form + Bookings iframe, 92 words
/impressum/           10 words, UID shown
/privacy-policy/      620 words, "Last updated: 12. November 2025" (F-11)
/maintenance-page/    "Website is under Maintenance.", in sitemap (F-09)
/services/            404 (no such page)
```

Words are visible text outside header, nav, footer and form, counted in code from raw HTML. The sitemap (`wp-sitemap.xml`) lists the six pages; there are 0 posts.

### Link labels against targets

| Label | Where | Target | Result |
| --- | --- | --- | --- |
| Expertise | Nav, all pages | `#homepage-expertise` | Works on home only; does nothing on the five other pages (F-06) |
| Services | Nav, all pages | `#services` | Same |
| Book a free 30-minute call | Home, section 2 | Microsoft Bookings | Works |
| Book a 30-minute call | Home, closing section | none (`<a>` without `href`) | Dead (F-03) |
| <www.ketztek.ch> (2 links) | Privacy page | `http://www.ketztek.ch/` | HTTP 500 (F-02) |
| <info@ketztek.ch>, <www.ketztek.ch/privacy> | Privacy page | Hostpoint site-builder editor preview | 303 to a Hostpoint login (F-11) |

### Dated history

| Date | Event | Source |
| --- | --- | --- |
| 2025-11-07 | `ketztek.com` registered (Ascio, nameservers Hostpoint) | `whois` |
| 2025-11-12 | Privacy text "Last updated" date, written for `www.ketztek.ch` | Privacy page |
| 2026-07-03 to 07-06 | WordPress pages created (maintenance page, contact, Impressum, privacy, home) | WordPress REST API |
| 2026-08-13 | Contact page last modified | REST API |
| 2026-09-17 | UID register last validation | UID register |
| 2026-10-28, 10-30 | Impressum edited; Expertise page published | REST API, sitemap |
| 2026-11-08 | `.com` registration updated | `whois` |
| 2026-11-16 | Current Let's Encrypt certificates issued for `ketztek.com` and `www` | `openssl` |

The Wayback Machine holds no capture of either domain (CDX and availability API, both empty). `[INFERENCE]` The privacy page's links into a Hostpoint site-builder editor show an earlier site on Hostpoint's builder, probably at `www.ketztek.ch`; no capture exists to confirm what it held. No sign of an earlier owner of either domain.

## 4. Detailed findings

Findings are ranked by effect on the assumed conversions (booked call, form, email). Index:

| ID | Title | Severity |
| --- | --- | --- |
| F-01 | Phone menu cannot be opened | High |
| F-02 | `www.ketztek.ch` returns a server error | High |
| F-03 | Closing "Book a 30-minute call" button is dead | High |
| F-04 | English-only site for a German-speaking market | High |
| F-05 | No proof of past work, people or reviews | High |
| F-06 | Nav anchors fail off home; Expertise page orphaned | Medium |
| F-07 | Google profile and directories nearly empty | Medium |
| F-08 | No phone number anywhere | Medium |
| F-09 | Search basics missing on every page | Medium |
| F-10 | Booking page offer is confusing | Medium |
| F-11 | Privacy page pasted from the old builder site | Medium |
| F-12 | Heavy font and uncached assets slow mobile | Medium |
| F-13 | No analytics or conversion measurement | Medium |
| F-14 | No security headers; version files public | Medium |
| F-15 | Minor accessibility failures | Low |
| F-16 | Theme and plugin leftovers | Low |
| F-17 | Two domains on two mail systems | Low |

### 4.2 Content and messaging

**What a buyer learns without phoning:** what the firm does (five services), for whom (industry and construction), the tools (Microsoft 365, Power Platform, Azure, custom code, AI, AR/VR), where (Winterthur, on site across Switzerland) and how to start (free 30-minute call). Missing on every surface: who the people are, any past project or client, prices or price cues, typical project size or duration beyond "two weeks of work", credentials, phone, office hours, response time.

**Value proposition as perceived:** "Winterthur consultants who fix slow processes with Microsoft tools or custom software, sized honestly." It should add proof and German (direction only: "Wir digitalisieren Abläufe in Industrie- und Baubetrieben und zeigen vorher, ob es sich lohnt.").

**Aged or unverifiable statements:** "a network we've worked with for years" and "Most clients simply choose not to [replace us]" are unverifiable for a firm whose domain is about a year old; both need a fact behind them (F-05). The privacy text's "Last updated: 12. November 2025" predates the site (F-11).

#### [F-04] English-only site for a German-speaking market

- Severity: High
- Confidence: Medium
- Category: Content, SEO
- Conversion touched: Consultation booking, Contact
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] All six pages: `lang="en-US"`, English copy, no `hreflang`. [FACT] The DE switch (GTranslate, `href="#"`) machine-translates in the browser on the same URL; it worked in 1 of 3 attempts (2026-11-20). [FACT] German autocomplete matched 23 of 45 seeds, English 0 of 6 (section 6). [FACT] 8 of 9 competitors are German-first. [INFERENCE] Only the English text is indexed, so German queries cannot reach the site.
- Why it matters: the target buyers search and decide in German.
- Recommendation: Publish German pages written by the operators (they already write German on the booking page) at their own URLs with `hreflang`; keep English second. Remove the live machine translation once real pages exist.
- Effort: M
- Impact: High

#### [F-05] No proof of past work, people or reviews

- Severity: High
- Confidence: High
- Category: Content, Trust
- Conversion touched: Trust, Consultation booking
- Cause: Content/operations
- Needs a website: Yes
- Evidence: [FACT] No page names a client, project, result, certification or team role; photos are two Pexels stock images and one generic construction image. [FACT] 0 reviews on Google; none found elsewhere. [FACT] 8 of 9 competitors show references or case stories (section 5). [UNVERIFIED] Whether shareable projects or certifications exist.
- Why it matters: a buyer handing a core process to a young firm needs evidence it has done this before; competitors one click away show it.
- Recommendation: Add two or three short anonymised project stories (problem, tool, result in hours saved), a team section by role with real photos, any certifications held, and ask first clients for Google reviews.
- Effort: M
- Impact: High

#### [F-11] Privacy page pasted from the old builder site

- Severity: Medium
- Confidence: High
- Category: Content, Trust
- Conversion touched: Trust
- Cause: Content/operations
- Needs a website: Yes
- Evidence: [FACT] Two links, labelled `info@ketztek.ch` and `www.ketztek.ch/privacy`, point to a Hostpoint site-builder editor preview URL that answers 303 to a Hostpoint login (2026-11-20). [FACT] The text says it covers `www.ketztek.ch` (HTTP 500, F-02) and names Google Analytics, which loads on no page. [FACT] It names none of the third parties that do load: Cloudflare Turnstile, GTranslate and Google Translate, Microsoft Bookings, Akismet. [FACT] A named individual appears as contact (not copied here).
- Why it matters: a login page behind an email link looks careless to a careful buyer. No legal conclusion is drawn.
- Recommendation: Operators rewrite it for `ketztek.com` and the services that load, with plain `mailto:` links.
- Effort: S
- Impact: Med

### 4.3 UX and conversion

**Journeys (as the surfaces stand on 2026-11-20):**

| Journey | Entry | Steps to convert | Friction |
| --- | --- | --- | --- |
| Plant manager on a phone wants a call | Google, home page | Scroll to section 2, tap "Book a free 30-minute call", pick a service, pick a slot: 3 taps plus form | Menu blocked (F-01); booking page lists 4 services (F-10) |
| Same reader finishes the home page | Home, end | Taps "Book a 30-minute call": nothing happens | Dead button (F-03) |
| Buyer who prefers to write | Contact page | Nav "Contact", fill 3 required fields, submit: 2 clicks plus form | None on desktop; on phones nav blocked, footer has no Contact link |
| Buyer who wants to phone | Any | Not possible | No number (F-08) |
| Buyer who saw `www.ketztek.ch` on an email or card | Browser | Server error page | F-02 |

**CTA inventory (home):** "Book a free 30-minute call" (filled button, y=1163 px at 375 px, below the fold), "Write to us" (y=1234), "Book a 30-minute call" (dead, y=6590), "Or just send us a message" (y=6661). No CTA is above the fold at 375 or 1440 px: the hero holds the logo image and "Making your business run smoother." The home page is 6,934 px tall at 375 px.

**Contact form (inspected, nothing submitted):** fields name, email, subject (all required) and message (optional); Contact Form 7 6.2.5 with Cloudflare Turnstile and the Akismet honeypot; form locale `de_CH` while labels are English. Submitting with an empty message but a subject is allowed, the reverse is not.

**Above-the-fold teardown.** 1440 px: nav (Home, Expertise, Services, Contact, EN/DE), large logo on a marble texture, one tagline; the offer, region and call are all below the fold. 375 px: logo, overlapping menu and language links, the same hero, then "Start with your processes." Screenshots `2026-11-20T1137Z-home-375.png` and `2026-11-20T1142Z-home-1440.png` were kept in the session scratchpad only (temporary, not committed).

**Heuristic review (Nielsen, 0-4, 4 = no problem):** status 3 (form spinner); real-world match 2 (F-04); user control 2 (F-06); consistency 2 (F-10); error prevention 3; recognition 3; flexibility 2 (F-08); minimal design 3 (long scroll, blank gaps until animations fire); error recovery 3; help 1 (no FAQ, prices or process steps).

#### [F-01] Phone menu cannot be opened

- Severity: High
- Confidence: High
- Category: UX
- Conversion touched: Contact, Consultation booking
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] At 360, 375, 390 and 414 px (phone user agent, touch), the GTranslate "EN" link covers the centre of the "Open menu" button. [FACT] 34 of 144 sampled points (24%) of the button are hittable; a centre tap leaves the menu closed (`/contact/`, 390 px, 2026-11-20). [FACT] From 600 px the nav works. [FACT] The footer links only to Privacy Policy and Impressum.
- Why it matters: phone visitors on the Expertise, Contact or legal pages have no working way to the other pages.
- Recommendation: Move the language switch out of the header's right edge on small screens (or into the menu), and add Contact and Book links to the footer.
- Effort: S
- Impact: High

#### [F-03] Closing "Book a 30-minute call" button is dead

- Severity: High
- Confidence: High
- Category: UX
- Conversion touched: Consultation booking
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] Raw HTML of `https://ketztek.com/` (2026-11-20 11:26Z): `<a class="wp-block-button__link wp-element-button">Book&nbsp;a 30-minute call</a>`, with no `href`. [FACT] The rendered DOM agrees (`href: null`, 375 px). The section-2 button links to Microsoft Bookings correctly.
- Why it matters: this is the button a reader taps after being convinced by the whole page; it fails silently.
- Recommendation: Link it to the same Bookings URL as the first button, and test every button after each edit.
- Effort: S
- Impact: High

#### [F-06] Nav anchors fail off home; Expertise page orphaned

- Severity: Medium
- Confidence: High
- Category: UX, Information architecture
- Conversion touched: Trust, Contact
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] Nav "Expertise" is `#homepage-expertise` and "Services" is `#services` on all six pages; those IDs exist only on the home page. [FACT] `/expertise/` (472 words, published 2026-10-30) is linked only from itself and the sitemap. [FACT] `/services/` returns 404.
- Why it matters: the strongest supporting page is unreachable from navigation, and two of four nav items do nothing on five of six pages.
- Recommendation: Point "Expertise" to `/expertise/` and "Services" to `/#services` (or a real services page, section 7).
- Effort: S
- Impact: Med

#### [F-08] No phone number anywhere

- Severity: Medium
- Confidence: High
- Category: UX, Local SEO
- Conversion touched: Call
- Cause: Content/operations
- Needs a website: No
- Evidence: [FACT] 0 `tel:` links and no phone text on the six pages; the Google place shows "Add place's phone number"; local.ch and the Impressum show none. [FACT] 7 of 9 competitors publish `tel:` links on their home page.
- Why it matters: some buyers, especially in construction, phone before they book; a missing number also weakens the Impressum and Google profile.
- Recommendation: If the operators want calls, publish one business number in the footer, Impressum, Google and local.ch.
- Effort: S
- Impact: Med

#### [F-10] Booking page offer is confusing

- Severity: Medium
- Confidence: High
- Category: UX, Content
- Conversion touched: Consultation booking
- Cause: Third party
- Needs a website: No
- Evidence: [FACT] The Bookings page (2026-11-20) lists four services: "Demo Software" (30 minutes, no description), "Coffee Chat / Kennenlerngespräch [30 min]", "Free Initial Consultation / Kostenloses Erstgespräch [30 min]" and "Demo M365 & Power Platform [1h]". [FACT] Descriptions show literal `**EN**` and `**DE**` markers. [FACT] The site promises one "free 30-minute call".
- Why it matters: a buyer who clicked "free 30-minute call" must choose between three similar options and a test-looking one.
- Recommendation: Hide "Demo Software"; make the free initial consultation the first or only option linked from the site; remove the asterisks.
- Effort: S
- Impact: Med

### 4.4 Visual identity and brand

Logo (lower-case wordmark with a yellow double "z") in header, hero and favicon; sand, near-black and yellow palette with Instrument Sans and Inter, consistent at 375 and 1440 px. It suits a calm, practical consultancy. Weak points are covered elsewhere: stock photos (F-05), header overlap (F-01), no share image (F-09). Reuse the logo, palette and tone. No client material supplied. No separate finding.

### 4.5 Technical foundations

Readings (host, domains, TLS, mail, platform versions, endpoint status) and the 24 Lighthouse runs are in the appendix under "Technical readings" and "Lighthouse results". Summary: WordPress 7.1.5 is current; cold first byte 0.50-0.57 s; Lighthouse performance medians 86-98; home mobile LCP 3.29 s; contact page about 5.8 MB.

#### [F-02] `www.ketztek.ch` returns a server error

- Severity: High
- Confidence: High
- Category: Technical, Hosting
- Conversion touched: Contact, Trust
- Cause: Hosting/DNS
- Needs a website: No
- Evidence: [FACT] `http://www.ketztek.ch/` returned HTTP 500 three times (11:29Z, 11:44Z, 11:45Z), body "Seite nicht verfügbar" by Hostpoint. [FACT] `https://www.ketztek.ch/` presents the `*.web.hostpoint.ch` certificate, so browsers show a certificate warning first. [FACT] The privacy page links to `http://www.ketztek.ch/` twice. [FACT] The public email is `@ketztek.ch`. [INFERENCE] The `www` host was left on Hostpoint's default vhost when the site moved to `ketztek.com`.
- Why it matters: anyone who types the address implied by the company email, or follows the privacy link, lands on an error; it looks like the firm is gone.
- Recommendation: In the Hostpoint account, attach `www.ketztek.ch` to the site (or a redirect) and its certificate, then confirm a 301 to `https://ketztek.com/`.
- Effort: S
- Impact: High

#### [F-12] Heavy font and uncached assets slow mobile

- Severity: Medium
- Confidence: High
- Category: Performance
- Conversion touched: Consultation booking
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] Home mobile LCP median 3.29 s (3 runs), above 2.5 s. [FACT] Largest asset on every page: `Inter-VariableFont_opsz,wght.ttf`, 874,708 bytes, `font/ttf`, no `Cache-Control`; Lighthouse estimates 1,372 KiB cache savings and flags font display. [FACT] Contact page 5.8-6.0 MB and about 200 requests, mostly the Bookings iframe (2,752 KB from Microsoft) and Turnstile (2,015 KB).
- Why it matters: phone users on site networks wait; repeat visitors download the font again.
- Recommendation: Serve WOFF2 subsets, set long cache headers for `/wp-content/`, and load the Bookings iframe on demand (button that reveals it).
- Effort: S
- Impact: Med

#### [F-14] No security headers; version files public

- Severity: Medium
- Confidence: High
- Category: Security
- Conversion touched: None
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] Home response headers (2026-11-20 11:48Z): no `Strict-Transport-Security`, `Content-Security-Policy`, `X-Content-Type-Options`, `X-Frame-Options` or `Referrer-Policy`. [FACT] `readme.html` 200; generator tag shows 7.1.5; public users endpoint lists 1 account (name not recorded); `security.txt` 404. Core and two of three visible plugins are current.
- Why it matters: low risk today, but a security-minded buyer (or their IT) may check, and this firm sells software quality.
- Recommendation: Add the headers in Hostpoint's `.htaccess` or a security plugin, hide `readme.html`, restrict the users endpoint, add `security.txt`.
- Effort: S
- Impact: Low

#### [F-16] Theme and plugin leftovers

- Severity: Low
- Confidence: High
- Category: Maintenance
- Conversion touched: None
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] Active theme Calm Canvas with parent "Bakery and Pastry"; home uses the maintenance plugin's template `templates/wpmm-page-template.php`; `/maintenance-page/` is published. [FACT] Superb Blocks 4.2.5 installed, 4.2.7 released 2026-11-20.
- Why it matters: a later theme update can change layout unexpectedly; a stray maintenance mode switch could hide the site.
- Recommendation: Keep auto-updates on, move the home page to a normal template, unpublish the maintenance page.
- Effort: S
- Impact: Low

#### [F-17] Two domains on two mail systems

- Severity: Low
- Confidence: Medium
- Category: Domain and email
- Conversion touched: Contact
- Cause: Hosting/DNS
- Needs a website: No
- Evidence: [FACT] `ketztek.ch` mail goes to Microsoft 365; `ketztek.com` MX points to Hostpoint mail. [FACT] Both DMARC records lack a reporting address; no DKIM found at common selectors. [UNVERIFIED] Whether any `@ketztek.com` mailbox is read.
- Why it matters: a buyer who guesses `info@ketztek.com` from the website address may write to an unread mailbox.
- Recommendation: Forward or alias `@ketztek.com` to Microsoft 365, enable DKIM in Microsoft 365, add a DMARC `rua` address. Any DNS change must leave the existing MX and SPF working.
- Effort: S
- Impact: Low

### 4.6 Accessibility

Automated checks only (Lighthouse axe rules); manual keyboard and zoom checks were not run. Contrast passed on all pages.

#### [F-15] Minor accessibility failures

- Severity: Low
- Confidence: Medium
- Category: Accessibility
- Conversion touched: Contact
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] Lighthouse (mobile, 2026-11-20): `target-size` fails on all four pages (footer links, language links, menu button); Contact iframe has no `title` (WCAG 4.1.2); `heading-order` fails on Contact, Expertise and Privacy (H3 without H2, 1.3.1); no `main` landmark on inner pages; home has no H1. [FACT] 21 text elements stay at opacity 0 until scrolled into view (scroll animations).
- Why it matters: screen-reader and older users get a weaker page structure and small tap targets.
- Recommendation: Add an H1 on home, a `title` on the iframe, correct heading levels, a `main` element, 24 px tap targets, and respect `prefers-reduced-motion`.
- Effort: S
- Impact: Low

### 4.7 SEO

**What ranks today:** not measured. Google web search returned a 429 challenge (11:34Z) and Bing, Brave and Startpage disallow their search paths in `robots.txt`. Whether any page is indexed is `UNVERIFIED`. Search Console verification records exist on both domains, so the operators can see it themselves.

**Local presence:** one Google place with correct name, address, category "Software company" and website. No roundups or guides list the firm (none found by search).

#### [F-07] Google profile and directories nearly empty

- Severity: Medium
- Confidence: High
- Category: Local SEO
- Conversion touched: Contact, Trust
- Cause: Listing/profile
- Needs a website: No
- Evidence: [FACT] Google place (11:34Z, signed out): no phone, hours, photos, description or reviews; prompts "Add place's phone number", "Add hours", "Add a photo". Ownership `UNVERIFIED`. [FACT] local.ch: "Unclaimed business", address only. [FACT] search.ch: 0 entries. [FACT] Competitors' places show phone, hours and 2-39 photos (section 5).
- Why it matters: "IT Beratung Winterthur" and "Softwarefirma Winterthur" are real autocomplete queries; an empty profile loses to filled ones.
- Recommendation: Claim and complete the Google profile (category, description in German, phone, hours or "by appointment", office and team photos, services); claim local.ch and add search.ch.
- Effort: S
- Impact: Med

#### [F-09] Search basics missing on every page

- Severity: Medium
- Confidence: High
- Category: Technical SEO
- Conversion touched: Consultation booking
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] Home `<title>` is "ketztek"; other titles "Page – ketztek". [FACT] 0 of 6 pages have a meta description; Lighthouse SEO 92 on all four tested pages for that reason. [FACT] No JSON-LD and no Open Graph tags on any page. [FACT] Home has no H1. [FACT] `/maintenance-page/` ("Website is under Maintenance.") is in the sitemap and indexable.
- Why it matters: search results and link previews show no offer, no place and no description; a placeholder page can appear in results.
- Recommendation: Write a German and English title and description per page, add `ProfessionalService` schema with address, add a share image, add an H1, remove the maintenance page from the sitemap.
- Effort: S
- Impact: Med

**Schema and metadata plan (for the fixed or rebuilt site):**

| Page | Title direction | Schema |
| --- | --- | --- |
| Home (de) | "Prozessoptimierung und Automatisierung für Industrie und Bau, Winterthur" | `ProfessionalService` (name, address, `areaServed` Switzerland, `url`, `email`, `telephone` once published, `knowsAbout`) |
| Service pages | Service name plus "für KMU" | `Service` with `provider` |
| Case stories | Problem and result | `Article` or `CreativeWork` |
| Contact | "Kontakt und kostenloses Erstgespräch" | `ContactPage` |

Use `hreflang` `de-CH`, `en` and `x-default` once German pages exist. No opening-hours markup unless the operators publish hours.

**Backlinks and mentions:** none found by search beyond the registry-fed directories. No paid backlink data used.

**AI answer check:** the harness search tool's summary said a directory lists ketztek GmbH as founded in 2025 (lead only; Zefix not readable). Consistent with the 2025-11-07 domain date, still `UNVERIFIED`.

### 4.8 Competitive benchmark

See section 5.

### 4.9 Reputation and off-site presence

No rating exists on Google, and no review profile was found elsewhere. No press, awards or partner listings found by search. Social profiles: none linked from the site, none found by search; LinkedIn `UNVERIFIED` (F-05, F-07). Nothing to reconcile.

### 4.10 Analytics, tracking and compliance

#### [F-13] No analytics or conversion measurement

- Severity: Medium
- Confidence: High
- Category: Analytics
- Conversion touched: Consultation booking, Contact
- Cause: Site or platform
- Needs a website: Yes
- Evidence: [FACT] No GA4, GTM, pixel or other analytics script in the raw HTML or the Lighthouse request lists of four pages; no consent banner. [FACT] Third parties that load: Cloudflare Turnstile (all pages), GTranslate and Google Translate (on DE click), Microsoft Bookings (Contact). [FACT] The privacy text names Google Analytics (F-11).
- Why it matters: the operators cannot tell whether the site produces bookings or which page or listing led to them.
- Recommendation: Add a privacy-friendly analytics tool, count booking-button and form events, tag Google-profile links with UTM, and use Bookings' own counts and Search Console as baselines.
- Effort: S
- Impact: Med

**What the operators can measure today without changes:** Google profile insights (views, website clicks), Search Console (verified on both domains), Microsoft Bookings appointment counts, contact-form emails, and "how did you hear about us" in the first call.

### Positive findings to keep

- **Clear, honest copy** ("Sometimes the honest answer is two weeks of work"; "one critical Excel file and the person who understands it"). Keep the voice in German.
- **A low-risk first step:** a free 30-minute call with a live Microsoft Bookings calendar, plus a contact form protected by Turnstile and Akismet.
- **Consistent identity data:** the same name and address on the site, Google, local.ch and the UID register; Impressum shows the UID.
- **Current platform:** WordPress 7.1.5 and current Contact Form 7 and GTranslate; HTTPS with clean redirects on `ketztek.com`; cold server response about 0.5 s; CLS 0.
- **The Expertise page:** six technologies, each tied to a business use.
- **Mail security basics:** DMARC `p=quarantine` on both domains.

## 5. Competitor matrix and gap analysis

**Selection.** (a) Small Power Platform and process-digitisation firms selling to Swiss SMEs around Zurich, plus a Winterthur software firm; (b) larger providers buyers also compare; (c) one presentation benchmark. Leads came from search results; every home page was opened in a browser (11:38Z, Appendix B script) and six Google places one by one. `thepoweraddicts.ch` redirects to `kmupower.com` (counted once). All `robots.txt` files allowed reading. Home pages only.

| Competitor | Group | Location (Google) | Lang | `tel:` | CTA labels | Proof on home | Schema | Google |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [PowerAlps](https://www.poweralps.ch/) | a | Samstagern | de-CH | 3 | Kontakt aufnehmen | Mentions customers; no references | Organization | No rating; phone, hours, 2 photos |
| [Theia Solutions](https://theiasolutions.ch/) | a | Zürich | de, en (`hreflang`) | 2 | Termin buchen, Anfrage senden | Referenzen, Microsoft partner | ProfessionalService | 5.0 (1), newest visible 6 months ago; 3 photos |
| [KMUpower](https://kmupower.com/) | a | Not shown | de-CH (`hreflang` CH, DE, AT) | 1 | Termin buchen | Fallstudien, Microsoft MVP | ProfessionalService, LocalBusiness | No rating, no phone or hours |
| [Stellar Automation](https://www.stellar-automation.ch/) | a | Dübendorf | de-CH | 0 | Kostenlosen Prozess-Check machen | Projekte | ProfessionalService, FAQPage | 5.0 (4); phone, hours, owner post |
| [evolyze](https://www.evolyze.ch/) | a | Winterthur | de | 2 | Kontakt | Erfolgsstories | none | No rating; phone, hours, 4 photos |
| [Kallysoft](https://kallysoft.ch/) | b | Basel (site) | de, en, fr, it | 2 | Termin vereinbaren, online Termin buchen | Referenzen | Organization | Not checked |
| [IOZ](https://www.ioz.ch/) | b | Sursee (site) | de | 8 | Kontakt | Erfolgsgeschichten | Organization, LocalBusiness | Not checked |
| [Noser Engineering](https://www.noser.com/) | b | Winterthur | de | 7 | Kontakt | Kundenprojekte | Organization | 4.7 (20); 39 photos |
| [Zühlke](https://www.zuehlke.com/) | c | Schlieren (site) | en, de | 0 | Contact us, Request for proposal | "Trusted by" client list | none | Not checked |
| ketztek | | Winterthur | en (machine DE) | 0 | Book a free 30-minute call | none | none | No rating, no phone, no photos |

Counts recomputed in code: 8 of 9 German-first, 7 of 9 with `tel:` links, 8 of 9 with references or case stories, 9 of 9 with a meta description, 7 of 9 with JSON-LD.

**Gap analysis.** What the closest competitors do that ketztek does not: German-first copy (all five in group a), named proof (case studies, an MVP title, partner status), a phone number, a complete Google place, schema. Where ketztek can differentiate: sector focus on industry and construction (only Theia mentions both, IOZ and others are sector-neutral), on-site work, AR/VR and custom code alongside low-code, and the "we size it honestly" stance. Patterns to copy: Theia's real `hreflang` versions and booking CTA; Stellar's "free process check" offer name; evolyze's success stories. Patterns to avoid: KMUpower's consent banner as first text, Stellar's 17-item nav.

## 6. Keyword map

Google autocomplete, `gl=ch`, 2026-11-20 11:4xZ, 51 seeds (45 German, 6 English). "Exact" means the seed itself appeared as a suggestion. No volume source: difficulty is `inferred`. Target fields assume the German-first structure in section 7.

| Query | Lang | Intent | Autocomplete | Target | Priority |
| --- | --- | --- | --- | --- | --- |
| ketztek | de/en | Brand | No suggestions | Home title, Google name | High |
| ketztek winterthur | de | Brand | No suggestions | Home, Google | Med |
| ketztek gmbh | de | Brand | No suggestions | Impressum, Google | Low |
| prozessoptimierung kmu | de | Service | Exact | Service: Prozessanalyse | High |
| prozessoptimierung winterthur | de | Near | None | Home, Google description | Med |
| prozessanalyse kmu | de | Service | None | Service: Prozessanalyse | Med |
| prozessautomatisierung kmu | de | Service | Exact | Service: Automatisierung | High |
| prozessautomatisierung schweiz | de | Service | Exact | Service: Automatisierung | High |
| digitalisierung kmu schweiz | de | Service | Exact | Home | High |
| digitalisierung kmu winterthur | de | Near | None | Home, Google | Med |
| power platform beratung | de | Service | Exact | Expertise: Power Platform | High |
| power platform beratung schweiz | de | Service | None | Expertise: Power Platform | Med |
| power apps entwicklung | de | Service | Exact | Service: Automatisierung | Med |
| power apps agentur | de | Service | None | Service: Automatisierung | Low |
| power automate beratung | de | Service | None | Service: Automatisierung | Med |
| power bi beratung | de | Service | Exact | Expertise: Power Platform | Med |
| microsoft 365 beratung kmu | de | Service | None | Expertise: Microsoft 365 | Med |
| sharepoint beratung | de | Service | Exact | Expertise: Microsoft 365 | Med |
| sharepoint einführung kmu | de | Service | None | Expertise: Microsoft 365 | Low |
| individualsoftware entwicklung | de | Service | Exact | Service: Software | High |
| individualsoftware schweiz | de | Service | None | Service: Software | Med |
| softwareentwicklung winterthur | de | Near | None | Service: Software, Google | Med |
| softwareentwicklung zürich kmu | de | Near | None | Service: Software | Low |
| schnittstellen programmieren | de | Service | Exact | Service: Software | Med |
| systemintegration kmu | de | Service | None | Service: Software | Low |
| ki für kmu | de | Service | Exact | Expertise: KI | High |
| ki beratung kmu schweiz | de | Service | Exact | Expertise: KI | High |
| ki dokumentenerkennung rechnungen | de | Service | None | Case story | Low |
| azure migration kmu | de | Service | None | Expertise: Cloud | Low |
| digitalisierung baustelle | de | Sector | Reordered only | Sector: Bau | High |
| baustellendokumentation app | de | Sector | Exact | Sector: Bau | High |
| mängelmanagement app | de | Sector | Exact | Sector: Bau | Med |
| digitalisierung bauunternehmen | de | Sector | Exact | Sector: Bau | High |
| digitalisierung produktion kmu | de | Sector | None | Sector: Industrie | Med |
| instandhaltung software kmu | de | Sector | None | Sector: Industrie | Med |
| maschinendaten auswerten | de | Sector | Exact | Sector: Industrie | Med |
| qualitätsbericht automatisieren | de | Sector | None | Sector: Industrie | Low |
| augmented reality wartung | de | Sector | Exact | Expertise: AR/VR | Low |
| power apps schulung | de | Training | Exact | Service: Schulungen | Med |
| microsoft 365 schulung | de | Training | Exact | Service: Schulungen | Med |
| excel ablösen | de | Problem | Exact | Home, case story | High |
| excel durch datenbank ersetzen | de | Problem | None | Case story | Med |
| it beratung winterthur | de | Near | Exact | Google category and description | High |
| softwarefirma winterthur | de | Near | Exact | Google, Home | High |
| informatik winterthur | de | Near | Exact (schools and jobs dominate) | None | Low |
| power platform consultant switzerland | en | Service | None | EN Expertise | Low |
| process automation switzerland | en | Service | None (other suggestions) | EN Home | Low |
| custom software development switzerland | en | Service | None | EN Software | Low |
| microsoft 365 consultant zurich | en | Service | None | EN Expertise | Low |
| construction site documentation app | en | Sector | None | EN Bau | Low |

## 7. Proposed information architecture

The listings carry the facts (address, phone if any, hours or "by appointment", category, photos, reviews); the site carries the offer, proof and booking. Whether German comes first is operator question 6; this tree assumes German first with English mirrors.

```text
/                         Home (DE)            CTA: Kostenloses Erstgespräch buchen      F-03, F-04, F-09
/leistungen/              Services overview    one block per service, link to each       F-06
  /prozessanalyse/        Process analysis     CTA: Erstgespräch     prozessoptimierung kmu
  /automatisierung/       M365 + Power Platform CTA: Erstgespräch    prozessautomatisierung kmu, power platform beratung
  /software/              Custom software      CTA: Erstgespräch     individualsoftware entwicklung
  /prototypen/            Prototyping, AR/VR   CTA: Erstgespräch
  /schulungen/            Workshops, training  CTA: Anfrage          power apps schulung
/branchen/industrie/      Industry             case story + CTA      maschinendaten auswerten
/branchen/bau/            Construction         case story + CTA      baustellendokumentation app
/expertise/               Technologies         (exists, English)     F-06
/projekte/                Case stories         2-3 to start          F-05
/ueber-uns/               Team by role, how we work, network          F-05
/kontakt/                 Form, Bookings on demand, address, phone   F-08, F-12
/impressum/  /datenschutz/                                            F-11
/en/...                   English mirror of the above, hreflang      F-04
```

## 8. Home page and key-page wireframe descriptions

**Home (German, 375 px first):**

1. Header: logo left, menu button right with nothing over it; language switch inside the menu or footer (F-01).
2. Hero (above the fold): German H1 `[operators write]`, one line on Winterthur and on-site work, button "Kostenloses Erstgespräch (30 Min.)" to the free-consultation booking type, secondary "Nachricht schreiben" (F-03, F-04, F-09).
3. Three pain points (existing copy, translated by the operators).
4. Services: five cards linking to service pages (F-06).
5. Sectors: Industrie, Bau, each with one case story teaser `[operators supply]` (F-05).
6. Proof strip: `[client or project outcome]`, `[certification if held]`, `[Google rating once reviews exist]`. Leave empty rather than invent (F-05).
7. "Why us" (existing six points, shortened).
8. Closing CTA repeating the hero button, working link (F-03), plus `[phone if published]` (F-08).
9. Footer: address, email, `[phone]`, Kontakt, Erstgespräch, Impressum, Datenschutz, language switch (F-01).

**Contact:** H1 "Kontakt" plus the existing friendly line; form with name, email, message (subject optional); response promise `[operators decide, e.g. "Antwort innert 1 Arbeitstag"]`; button "Termin wählen" that loads the Bookings iframe (with `title`) on demand (F-12, F-15).

**Case story template:** client type and region (anonymised if needed), starting problem, tools used, result `[measured figure from the operators]`, time to deliver, quote by role.

**Google profile fields and photo plan (F-07):** primary category matching the offer (operators choose, e.g. "Software company" or "Business management consultant"), German description of about 700 characters using "Prozessoptimierung", "Power Platform", "Industrie", "Bau", "Winterthur"; phone `[if published]`; hours or "by appointment" `[operators]`; services list mirroring section 7; photos: office or building exterior, team at work by role, a site or factory visit `[with permission]`, logo, a screenshot of a delivered app `[if shareable]`. Ask first clients for reviews.

## 9. Prioritized roadmap

Owner names the role that must act; no access was granted.

| When | Finding | Action (five words or fewer) | Owner | Effort | Impact | Needs website or platform change |
| --- | --- | --- | --- | --- | --- | --- |
| Quick win, before 2026-12-24 | F-02 | Fix `www.ketztek.ch` host | Hostpoint account holder | S | High | No (hosting) |
| Quick win | F-01 | Unblock phone menu button | Site admin | S | High | Yes, small edit |
| Quick win | F-03 | Link closing booking button | Site admin | S | High | Yes, small edit |
| Quick win | F-06 | Fix nav targets | Site admin | S | Med | Yes, small edit |
| Quick win | F-10 | Tidy Bookings services | Microsoft 365 admin | S | Med | No |
| Quick win | F-07 | Complete Google profile | Operators | S | Med | No |
| Quick win | F-08 | Publish a phone number | Operators | S | Med | No |
| Short term, January 2027 | F-09 | Add titles, descriptions, schema | Site admin or freelancer | S | Med | Yes |
| Short term | F-11 | Rewrite privacy page | Operators | S | Med | Yes, content |
| Short term | F-13 | Add analytics and events | Site admin or freelancer | S | Med | Yes |
| Short term | F-12 | Font, caching, lazy Bookings | Site admin or freelancer | S | Med | Yes |
| Short term | F-14 | Add security headers | Site admin | S | Low | Yes |
| Medium term, Q1 2027 | F-04 | German pages with `hreflang` | Operators write; freelancer builds | M | High | Yes |
| Medium term | F-05 | Case stories, team, reviews | Operators supply; freelancer builds | M | High | Yes |
| Medium term | F-15 | Accessibility fixes | Site admin or freelancer | S | Low | Yes |
| Long term | F-16 | Clean theme leftovers | Site admin | S | Low | Yes |
| Long term | F-17 | Unify mail, DKIM, DMARC reports | Microsoft 365 and DNS admin | S | Low | No |

No Critical finding exists; all five High findings sit in Quick wins or Medium term, and the three that block conversions today (F-01, F-02, F-03) are Quick wins.

## 10. Platform recommendation

The operating-status verdict is `APPEARS ACTIVE`, so this is not worded conditionally.

| Option | Fit | Notes |
| --- | --- | --- |
| 1. Fix without a new site (listings, DNS, Bookings) | Strong | F-02, F-07, F-08, F-10, F-17 need no site work at all |
| 2. Keep WordPress and fix it | **Recommended** | Current core, fast server, working form; F-01, F-03, F-06, F-09, F-12 are small edits; German pages via a multilingual plugin (Polylang or WPML) instead of GTranslate |
| 3. Hosted builder | Weak | The firm left Hostpoint's builder already (F-11 traces); no gain over option 2 |
| 4. Custom build, framework plus headless CMS | Conditional | Only if the operators want a larger German-first site and prefer to hand it over; no ranking history to protect |
| 5. Booking platform only | Already in place | Microsoft Bookings works; keep it |

**Recommendation with reasoning.** Fix listings and DNS first (option 1), then fix the site in place (option 2). Every High finding except F-04 and F-05 is platform-independent or a small edit, and F-04 and F-05 are mostly content the operators must write. A rebuild would not fix any of them by itself.

**Freelancer fit.** If the freelancer will not work on WordPress, say so plainly: the realistic offer is the listings work, a content plan (German structure, case-story template, Google profile), and an optional rebuild later. The operators build software for a living and may prefer to do the WordPress edits themselves.

**Change the recommendation if** the operators want a German-first site with several service and case pages and no time to maintain WordPress; then option 4 with a headless CMS and real language routes is reasonable.

**Who looks after the current site and DNS until then:** the operators, who hold the Hostpoint account (site and DNS for both domains) and Microsoft 365.

**Launch or migration checklist (any path):** leave MX and SPF on both domains untouched; keep `ketztek.com` as the primary host with 301s from `ketztek.ch`, `www.ketztek.ch` and `www.ketztek.com`; keep the Bookings link and Turnstile; publish German and English with `hreflang`; resubmit the sitemap in Search Console; test the menu and every button at 375 px with a phone user agent.

## 11. Measurement plan

| KPI | Baseline | Tool |
| --- | --- | --- |
| Booked free consultations per month | Unknown (operators can read Bookings history) | Microsoft Bookings |
| Contact-form and email enquiries per month | Unknown | Mailbox, Contact Form 7 |
| Clicks on booking buttons | Not measured (F-13) | Analytics event |
| Google profile views, website clicks, calls | Unknown (needs profile access) | Google Business Profile insights |
| Search impressions for German service queries | Unknown | Search Console (verified on both domains) |
| Google reviews | 0 (2026-11-20) | Google profile |
| Home mobile LCP | 3.29 s median (2026-11-20) | Lighthouse, three runs |
| Source of each enquiry | Not recorded | Ask in the first call |

Targets only after one month of measured baseline.

## 12. Open questions

### For the operators

1. What would you like this site (or your online presence) to do for the business today?
2. Who runs the business day to day, and who holds each login: domains and hosting (Hostpoint), WordPress, Microsoft 365 and Bookings, the Google profile, any LinkedIn page?
3. What is current now: which of the five services do you sell most, and which booking types on the Bookings page are real?
4. Which phone number, email and hours (or "by appointment") should be public, and is `info@ketztek.com` meant to receive mail?
5. Which past projects or clients may be described, even anonymously, and do you hold Microsoft certifications or partner status? What are typical project size, duration and price range, and which regions do you travel to?
6. Which language should come first, German or English, and should the site also serve French-speaking Switzerland?
7. How should a first meeting work: online only, at your office, or on the client's site?
8. Who owns the logo, the photos and any project screenshots, and which files exist?
9. Is "ketztek GmbH" the only name to show (we give no legal advice)?
10. How are enquiries and bookings tracked today?
11. What budget and timeline do you have in mind, if any?

### For the freelancer

1. Does the platform assumption hold here, given that the operators are software engineers on a working WordPress site, and is a non-rebuild offer (listings, content plan, fixes) acceptable?
2. Prospect or existing relationship, and is a Swiss B2B firm in scope for a Chicago-area practice (language, time zone, Swiss privacy expectations)?
3. Should the client report be sent in English, or translated into German by a native speaker first? (This run produced English only.)
4. Willingness to maintain anything afterwards, and engagement terms.
5. Whether to tell the operators about F-01, F-02 and F-03 now, unconditionally, since each is a quick fix that loses enquiries today.
6. Manual checks automation could not do: a Zefix lookup for the founding date, a signed-in LinkedIn search, Google results for the brand and "softwarefirma winterthur".
7. Whether and when to send the client report.

## 13. Appendix

### Hypotheses

No leads were supplied. My first readings became the hypotheses.

| # | Item | Reading | Source | Status | Finding |
| --- | --- | --- | --- | --- | --- |
| H1 | The site at the given URL belongs to the business | Impressum with UID on `ketztek.com` | `curl`, 11:28Z | CONFIRMED | Mode A |
| H2 | The firm is a Winterthur GmbH | Registry entry active | UID register, 11:35Z | CONFIRMED | Section 3 |
| H3 | `ketztek.ch` is an alias of the same site | Apex 301 to `.com`; `www` 500 | `curl`, `openssl` | CHANGED (apex yes, `www` broken) | F-02 |
| H4 | The DE switch provides a German version | Client-side machine translation, same URL, 1 of 3 attempts | Browser | REFUTED as a real version | F-04 |
| H5 | The business has reviews or a social presence | None found | Google place, search | REFUTED (LinkedIn `UNVERIFIED`) | F-05, F-07 |
| H6 | Google Analytics runs, as the privacy text says | No analytics loads | Raw HTML, Lighthouse requests | REFUTED | F-11, F-13 |
| H7 | Founded in 2025 | Directory snippet via search summary; domain created 2025-11-07 | Search tool lead, `whois` | UNVERIFIED | Section 4.7 |
| H8 | An earlier site existed on Hostpoint's builder | Editor-preview links in privacy text | Raw HTML | UNVERIFIED (no Wayback capture) | F-11 |

### Platform access

| Platform | Result |
| --- | --- |
| ketztek.com | Full (robots: `Crawl-delay: 10`, respected; one request per URL, 10 s apart) |
| Google Maps | Limited view, loaded (7 places) |
| Google web search | 429 challenge at 11:34Z; not retried |
| Bing, Brave, Startpage search pages | Not used: `robots.txt` disallows search paths |
| Zefix, Moneyhouse | Not read: `robots.txt` disallows all |
| UID register | Full |
| local.ch, search.ch | Full |
| LinkedIn | Inconclusive (404 signed out at a guessed slug) |
| `whois.nic.ch` | Refuses command-line queries |
| Microsoft Bookings | Full (read only, nothing booked) |

### Operating-status notes

`APPEARS ACTIVE` was chosen on: (1) the UID register, independent, showing commercial-register status active and a validation on 17.09.2026; (2) first-party content dated 2026-10-28 and 2026-10-30 and a registrar update on 2026-11-08; (3) a live booking calendar. There are no reviews, posts or press, the usual independent signs. If the freelancer reads the rule strictly (two independent dated signs, aggregators excluded), the registry is the only independent one and the verdict would be `UNCLEAR`; nothing in the evidence suggests the firm has stopped trading.

### Technical readings

| Item | Reading (2026-11-20) |
| --- | --- |
| Host | Hostpoint (Apache), A `217.26.55.115`, AAAA present; nameservers `ns*.hostpoint.ch` for both domains |
| `ketztek.com` | Registrar Ascio, created 2025-11-07, expires 2027-11-07, DNSSEC unsigned |
| `ketztek.ch` | Registrar data not read (`whois.nic.ch` refuses command-line queries) |
| Redirects | `http://ketztek.com` 301 to `https://ketztek.com/`; `https://www.ketztek.com` 301 to apex; `http://ketztek.ch` 301 to `https://ketztek.ch/` 301 to `https://ketztek.com/`; `www.ketztek.ch` HTTP 500 (F-02) |
| TLS | Let's Encrypt for `ketztek.com` and `www.ketztek.com` (2026-11-16 to 2027-02-14); Sectigo for `ketztek.ch` with SAN `www.ketztek.ch`, but `www.ketztek.ch` serves Hostpoint's `*.web.hostpoint.ch` certificate |
| Mail | `ketztek.ch`: MX Microsoft 365, SPF Hostpoint plus Outlook `~all`, DMARC `p=quarantine`. `ketztek.com`: MX Hostpoint, SPF redirect to Hostpoint, DMARC `p=quarantine`. No DKIM found at the common selectors on either. Search Console verification TXT on both. |
| Server timing | Cold first byte 0.50-0.57 s on all six pages (`curl`, first requests of the session) |
| Compression | HTML gzip; fonts and images served without `Cache-Control` or `Expires` |
| Platform | WordPress 7.1.5 (current per `api.wordpress.org`), theme Calm Canvas 1.4 (child of "Bakery and Pastry"), Contact Form 7 6.2.5 (current), GTranslate 5.0.2 (current), Superb Blocks 4.2.5 (4.2.7 released 2026-11-20), Akismet, a maintenance-mode page template on home |
| Endpoints (status only) | `wp-login.php` 200, `readme.html` 200, `xmlrpc.php` 403, `/wp-json/` 200, users endpoint 200 with 1 item, `security.txt` 404 |

### Lighthouse results

Lighthouse 13.6.0, three runs per page and strategy, median (range), 2026-11-20 11:34Z-11:46Z. All runs followed a cold `curl` pass, so they are warm.

| Page | Strategy | Perf | A11y | BP | SEO | LCP s | CLS | KB | Requests |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Home | Mobile | 91 (87-91) | 95 | 100 | 92 | 3.29 (3.24-3.62) | 0 | 1,420 | 33 |
| Home | Desktop | 86 (79-86) | 95 | 100 | 92 | 1.89 (1.81-1.96) | 0 | 1,806 | 33 |
| Contact | Mobile | 94 (94-94) | 90 | 77 | 92 | 2.56 (2.55-2.58) | 0 | 5,969 | 205 |
| Contact | Desktop | 92 (88-95) | 90 | 77 | 92 | 1.24 (1.16-1.43) | 0.012 | 5,780 | 199 |
| Expertise | Mobile | 98 (97-100) | 91 | 100 | 92 | 2.28 (1.47-2.35) | 0.009 | 1,147 | 21 |
| Expertise | Desktop | 98 (98-99) | 91 | 100 | 92 | 0.99 (0.90-1.01) | 0.014 | 1,147 | 21 |
| Privacy | Mobile | 97 (83-98) | 93 | 100 | 92 | 2.37 (2.33-2.42) | 0 | 1,150 | 23 |
| Privacy | Desktop | 98 (97-98) | 93 | 100 | 92 | 1.06 (1.00-1.09) | 0.001 | 1,150 | 23 |

Thresholds: LCP 2.5 s or less, INP 200 ms or less, CLS 0.1 or less ([web.dev, Core Web Vitals](https://web.dev/articles/vitals), not re-fetched in this run). CrUX field data: not available (no API key; site traffic likely too low).

### Commands used (summary)

- Headers and pages: `curl -sS -m 40 -w '%{http_code} %{time_starttransfer}'`, one URL per 10 s; `curl -sSI` for redirects.
- DNS: `dig +short <TYPE> <name>` for A, AAAA, CNAME, NS, MX, TXT, SOA, CAA, `_dmarc`, DKIM selectors `google`, `selector1`, `selector2`, `default`, `k1`, `s1`, `mail`.
- `whois ketztek.com`; `openssl s_client -servername <host>` piped to `openssl x509 -noout -text`.
- WordPress: `/wp-json/wp/v2/pages`, `/wp-json/wp/v2/posts`, `wp-sitemap.xml`; `api.wordpress.org` core, plugin and theme info.
- Wayback: `web.archive.org/cdx/search/cdx?url=<domain>*` and `archive.org/wayback/available`.
- Lighthouse: `npx -y lighthouse <url> --only-categories=performance,accessibility,seo,best-practices --chrome-flags="--headless=new --no-sandbox" --output=json` (plus `--preset=desktop`), 4 pages x 2 strategies x 3 runs, 10 s apart.
- Autocomplete: `suggestqueries.google.com/complete/search?client=firefox&gl=ch&hl=<de|en>&q=<seed>`, 1.5 s apart.
- Browser: Playwright, signed out; phone emulation 360-414 px with an iPhone user agent and touch; desktop 1440 px; Appendix B fingerprint script with German CTA terms.

### URLs opened

Site: `https://ketztek.com/` and `/expertise/`, `/contact/`, `/impressum/`, `/privacy-policy/`, `/maintenance-page/`, `/services/`, `/robots.txt`, `/wp-sitemap.xml`, `/wp-sitemap-posts-page-1.xml`, `/feed/`, `/wp-json/`, `/readme.html`, `/wp-login.php`, `/xmlrpc.php`, `/.well-known/security.txt`; `http://ketztek.ch/`, `https://ketztek.ch/`, `http://www.ketztek.ch/`, `https://www.ketztek.ch/`, `https://www.ketztek.com/`.

External: [UID register entry](https://www.uid.admin.ch/Detail.aspx?uid_id=CHE295462558), [local.ch listing](https://www.local.ch/en/d/winterthur/8406/ketztek-gmbh-7bWDg4UHzh9k-DIdRxubPg), [search.ch query](https://search.ch/tel/?was=ketztek), [Google Maps place](https://www.google.com/maps/search/ketztek+GmbH+Schulergasse+9+Winterthur?hl=en), [Bookings page](https://bookings.cloud.microsoft/book/ketztek1@ketztek.ch/?ismsaljsauthenabled), [WordPress version API](https://api.wordpress.org/core/version-check/1.7/), competitor home pages in section 5 and their Google places (evolyze, PowerAlps, Theia Solutions, KMUpower, Noser Engineering, Stellar Automation).

### Limitations

- No search-engine result pages: Google returned a 429 challenge; other engines disallow their search paths. Rankings and indexing are `UNVERIFIED`.
- Zefix and Moneyhouse not read (`robots.txt`); founding date and register publications `UNVERIFIED`.
- `ketztek.ch` registration details not read (`whois.nic.ch` refuses command-line queries).
- LinkedIn, Xing, Apple Maps and Bing Places not checked or inconclusive.
- German copy judgements are not by a native Swiss German speaker.
- Accessibility: automated checks only; no keyboard, zoom or screen-reader pass.
- Lighthouse runs are warm (they followed a cold `curl` pass); CrUX field data not available.
- Three competitors' Google places (Kallysoft, IOZ, Zühlke) not opened; competitor inner pages not read.
- The browser tool could only write captures inside this repository (`.playwright-mcp/`, git-ignored); they were moved to the session scratchpad at the end of the run and the folder was deleted. Screenshots are therefore temporary; quoted text and measured values in this report stand on their own.

### Machine-readable summary

```json
[
 {
  "id": "F-01",
  "title": "Phone menu cannot be opened",
  "severity": "High",
  "confidence": "High",
  "category": "UX",
  "conversion": "Contact, Consultation booking",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "High"
 },
 {
  "id": "F-02",
  "title": "www.ketztek.ch returns a server error",
  "severity": "High",
  "confidence": "High",
  "category": "Technical, Hosting",
  "conversion": "Contact, Trust",
  "cause": "Hosting/DNS",
  "needs_website": false,
  "effort": "S",
  "impact": "High"
 },
 {
  "id": "F-03",
  "title": "Closing \"Book a 30-minute call\" button is dead",
  "severity": "High",
  "confidence": "High",
  "category": "UX",
  "conversion": "Consultation booking",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "High"
 },
 {
  "id": "F-04",
  "title": "English-only site for a German-speaking market",
  "severity": "High",
  "confidence": "Medium",
  "category": "Content, SEO",
  "conversion": "Consultation booking, Contact",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "M",
  "impact": "High"
 },
 {
  "id": "F-05",
  "title": "No proof of past work, people or reviews",
  "severity": "High",
  "confidence": "High",
  "category": "Content, Trust",
  "conversion": "Trust, Consultation booking",
  "cause": "Content/operations",
  "needs_website": true,
  "effort": "M",
  "impact": "High"
 },
 {
  "id": "F-06",
  "title": "Nav anchors fail off home; Expertise page orphaned",
  "severity": "Medium",
  "confidence": "High",
  "category": "UX, Information architecture",
  "conversion": "Trust, Contact",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "Med"
 },
 {
  "id": "F-07",
  "title": "Google profile and directories nearly empty",
  "severity": "Medium",
  "confidence": "High",
  "category": "Local SEO",
  "conversion": "Contact, Trust",
  "cause": "Listing/profile",
  "needs_website": false,
  "effort": "S",
  "impact": "Med"
 },
 {
  "id": "F-08",
  "title": "No phone number anywhere",
  "severity": "Medium",
  "confidence": "High",
  "category": "UX, Local SEO",
  "conversion": "Call",
  "cause": "Content/operations",
  "needs_website": false,
  "effort": "S",
  "impact": "Med"
 },
 {
  "id": "F-09",
  "title": "Search basics missing on every page",
  "severity": "Medium",
  "confidence": "High",
  "category": "Technical SEO",
  "conversion": "Consultation booking",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "Med"
 },
 {
  "id": "F-10",
  "title": "Booking page offer is confusing",
  "severity": "Medium",
  "confidence": "High",
  "category": "UX, Content",
  "conversion": "Consultation booking",
  "cause": "Third party",
  "needs_website": false,
  "effort": "S",
  "impact": "Med"
 },
 {
  "id": "F-11",
  "title": "Privacy page pasted from the old builder site",
  "severity": "Medium",
  "confidence": "High",
  "category": "Content, Trust",
  "conversion": "Trust",
  "cause": "Content/operations",
  "needs_website": true,
  "effort": "S",
  "impact": "Med"
 },
 {
  "id": "F-12",
  "title": "Heavy font and uncached assets slow mobile",
  "severity": "Medium",
  "confidence": "High",
  "category": "Performance",
  "conversion": "Consultation booking",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "Med"
 },
 {
  "id": "F-13",
  "title": "No analytics or conversion measurement",
  "severity": "Medium",
  "confidence": "High",
  "category": "Analytics",
  "conversion": "Consultation booking, Contact",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "Med"
 },
 {
  "id": "F-14",
  "title": "No security headers; version files public",
  "severity": "Medium",
  "confidence": "High",
  "category": "Security",
  "conversion": "None",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "Low"
 },
 {
  "id": "F-15",
  "title": "Minor accessibility failures",
  "severity": "Low",
  "confidence": "Medium",
  "category": "Accessibility",
  "conversion": "Contact",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "Low"
 },
 {
  "id": "F-16",
  "title": "Theme and plugin leftovers",
  "severity": "Low",
  "confidence": "High",
  "category": "Maintenance",
  "conversion": "None",
  "cause": "Site or platform",
  "needs_website": true,
  "effort": "S",
  "impact": "Low"
 },
 {
  "id": "F-17",
  "title": "Two domains on two mail systems",
  "severity": "Low",
  "confidence": "Medium",
  "category": "Domain and email",
  "conversion": "Contact",
  "cause": "Hosting/DNS",
  "needs_website": false,
  "effort": "S",
  "impact": "Low"
 }
]
```
