# ketztek visual research for design v2 (Option E)

Run on 2026-11-21 (Saturday). Internal file for the design lead. Input: [design v2 prompt](ketztek-design-v2-prompt.md). Earlier inputs: [research](../design-brief/ketztek-design-research.md) and [design prompt](../design-brief/ketztek-design-prompt.md).

## Method and limits

- Passive only. `robots.txt` was read first for every host. Two rules matter: [evolyze.ch](https://www.evolyze.ch/robots.txt) disallows `/` only for `Googlebot-Image` (general agents may read pages but not `.png`, `.jpg`, `.svg` and similar, so no images were fetched), and [ioz.ch](https://www.ioz.ch/robots.txt) sets a 10 s crawl delay for general bots and blocks `MonSpark` completely. [ketztek.com](https://ketztek.com/robots.txt) asks for 10 s. No form was submitted, nothing was booked, and no contact was made.
- Pages were read as rendered text through a web-fetch agent on 2026-11-21. CSS was stripped, so typefaces and accent colours cannot be confirmed from that run. Where a font or accent is named below, it comes from the 2026-11-21 fingerprint in the [earlier research](../design-brief/ketztek-design-research.md) section 6, not from this run.
- No competitor or reference screenshot was taken in this run. Raw captures stay outside the repositories and none were kept.
- Best of Swiss Web: the gold list gives only one B2B project that fits (see 5.1.2). The brief asks for five. The gap is recorded, not filled.

## 5.1 Local visual culture

### 5.1.1 Swiss design heritage, applied today

Swiss Style (grid, asymmetric layout, flush-left type, strong hierarchy, restrained colour) is still the reference point for Swiss corporate and B2B sites. Sources read: [Smashing Magazine, "Lessons From Swiss Style Graphic Design", 2009](https://www.smashingmagazine.com/2009/07/17/lessons-from-swiss-style-graphic-design/) and the [Wikipedia entry for Swiss Style](https://en.wikipedia.org/wiki/Swiss_Style_(design)). Read as search summaries only, not in full: [AIGA Eye on Design essay on minimalism](https://eyeondesign.aiga.org/graphic-designers-have-always-loved-minimalism-but-at-what-cost/) and a [Swiss modernism essay](https://blazetype.eu/blog/swiss-modernism).

Where it has become a cliché:

- As a default. A grid, a sans-serif and a thin rule are now read as "professional" before the content is read. Any consultancy can use the same set.
- As a logo system. Corporate marks copy the ornament-free look without adding anything of their own.
- As proof of seriousness. Heavy grid use reads as a fashion of the moment, not as evidence of precision.

Principle to keep: the grid and the flush-left text column make the page's order obvious. Drop the look, keep the order.

### 5.1.2 Award winners

[Netzwoche, "Das sind die Gold-Gewinner auf einen Blick", 2025-04-03, read 2026-11-21](https://www.netzwoche.ch/news/2025-04-03/das-sind-die-gold-gewinner-auf-einen-blick) lists the 11 gold awards of Best of Swiss Web 2025 (8 projects, 85 shortlisted from 328). The page names projects but no clients, agencies, descriptions or project URLs. The only project that fits B2B, technology or industry is:

| Project | Categories | Source | Principle to borrow |
| --- | --- | --- | --- |
| Bucher Connect Serviceplattform (Master of Swiss Web 2025) | Marketing, Productivity, Technology; Master title | [Netzwoche, 2025-04-03](https://www.netzwoche.ch/news/2025-04-03/gold-fuer-bucher-connect-serviceplattform) (headline only read in search) | A B2B platform is judged on its working tool. Show the operational purpose first, as a product for daily use. |

Not used, and why: Nemo, Chopard, WOZ, Marktplatz Zermatt, the Lehrstellen campaign and Bilder der Schweiz Online are consumer, media, tourism or campaign work. Accessibility of live events (Innovation, Public Value) is a technology project, but the page does not show it is B2B.

Gap: five B2B, technology or industry winners could not be read. The next step is to read the individual winner pages on Netzwoche (not in this run) or the Best of Swiss Web site itself.

### 5.1.3 Swiss industrial and construction brands

Read as rendered text on 2026-11-21 (web-fetch agent; CSS not visible, so no typefaces or hex values confirmed):

| Brand | URL | What the first screen is made of | Signal of precision or trust |
| --- | --- | --- | --- |
| Sulzer | [sulzer.com](https://www.sulzer.com/) | Text: "A top industrial company that truly creates value for stakeholders" | Live share-price widget with time stamp |
| Rieter | [rieter.com](https://www.rieter.com/) | Text, three news teasers with thumbnails | "Facts and Figures" counter block (years, sites, countries, employees) |
| Bühler | [buhlergroup.com](https://www.buhlergroup.com/) | Header image, image carousel | Tile grid "Solutions for your industries"; breadth, not depth |
| Stadler | [stadlerrail.com](https://www.stadlerrail.com/) | Photo of a train; model cards from product renders | Facts strip: order intake, backlog, revenue, margin, vehicles sold |
| Burckhardt Compression | [burckhardtcompression.com](https://www.burckhardtcompression.com/) | Photo of engineers beside a compressor | Dated, labelled news cards with tags such as "Ad hoc" and "Success Stories" |
| Hilti | [hilti.com](https://www.hilti.com/) (US site, English) | Product promo over a headline | Selector charts and an engineering entry point: functional decision tools |
| Implenia | [implenia.com](https://www.implenia.com/) (German) | 20-year video teaser | KPI block with prior-year comparison (backlog, EBIT, free cash flow, equity ratio) |

Reading for ketztek: these firms signal precision with figures, comparison and decision tools, not with decoration. Figures with a comparison column are the most credible trust signal available to a young firm that has no case studies yet, but ketztek has no figures to show. Do not invent any (see the brief's rule on figures).

Visitors note: none of the seven shows its own work as technical drawing or diagram on the first screen. That is the gap a drawn system can own.

### 5.1.4 Local conventions

These are general Swiss conventions, not sourced in this run. Check them before the Impressum and privacy pages are built:

- Swiss Standard German does not use "ß" ("ss" everywhere).
- Quotes in German text use «guillemets».
- Phone numbers `+41 52 ...` (Winterthur area code 052). None is published yet.
- Dates `21.11.2026`.
- Impressum and privacy page in the footer. The privacy text must follow the Swiss revised data protection act (nDSG); no legal advice here.
- German first or English first: the brief's [design research](../design-brief/ketztek-design-research.md) found all seven competitors in German and German search terms as the working vocabulary. Keep German first.
- Language switch as "DE | EN" linking to real pages, not machine translation.

### 5.1.5 Type

Foundries and licence costs (read on 2026-11-21):

- **Grilli Type**: the web licence is sold as a set number of licences for servers under the buyer's control, sized to monthly visitors. The EULA is governed by Swiss law. Two EULA versions name different legal entities, so check the current one before buying ([Grilli Type Web EULA](https://grillitype.com/api/v1/download/eula_web/Grilli-Type-Web-EULA-1_7.pdf)). Price not found.
- **Dinamo**: priced by company size, excluding VAT; quote tool on the site ([Dinamo pricing](https://abcdinamo.com/news/about-our-pricing), [Discounts and pricing](https://abcdinamo.com/discounts-and-pricing)). Price not found without the quote.
- **Swiss Typefaces**: the site says fonts are full versions and no extra licence is needed per media type ([Swiss Typefaces advantages](https://swisstypefaces.com/advantages)). Optimo web price not found.

Recommendation: no commercial face for launch. Its licence cost and the visitor-based count would land on a company that has not yet bought a single font, and the brief allows a commercial face only as a recommendation with a free fallback actually used. Keep Archivo (SIL OFL, already self-hosted in the prototype). Its width axis gives the headlines the precision the directions need without a second family.

Avoid list, checked: the competitors use Manrope, Montserrat, Inter, Satoshi, Clash Display, Maven Pro and Trade Gothic (fingerprint, 2026-11-21). The current site uses Inter and Instrument Sans. Archivo is none of these.

## 5.2 Competitors, re-read

First screens were read as text on 2026-11-21. Fonts and accent colours come from the [2026-11-21 fingerprint](../design-brief/ketztek-design-research.md) (section 6), because the text-only read could not see CSS.

| Site | H1 (read 2026-11-21) | Primary call to action (text read) | Font and accent (fingerprint) | First screen | What makes it look professional or not |
| --- | --- | --- | --- | --- | --- |
| [evolyze](https://www.evolyze.ch/) | "Wir helfen Organisationen, mit Daten und Software erfolgreich zu sein" | "Kontakt" in header | Manrope; navy `#162b3e` | Text, three value statements | Calm and clear, but no offer or next step on the first screen |
| [Theia Solutions](https://theiasolutions.ch/) | "Von Daten zu Entscheidungen" | "Services entdecken", secondary "Jetzt Kontakt aufnehmen" | Montserrat; blue-teal gradient | Text plus a workflow dashboard mock-up | Dashboard mock-ups and a consent dialog on the phone |
| [PowerAlps](https://www.poweralps.ch/) | "Power Platform Spezialisten für Prozessdigitalisierung" | "Kontakt aufnehmen" | Clash Display; green `#0ce696` on dark | Text and three bullets | Clearest Power Platform offer, but the accent is green |
| [Stellar Automation](https://www.stellar-automation.ch/) | "Prozessautomatisierung für Schweizer Unternehmen" | "Kostenlosen Prozess-Check machen" | Inter, Satoshi; blue `#007ee5` | Headline, tagline, one button | A named free offer, the best CTA wording in the set |
| [KMUpower](https://kmupower.com/) | "Power Platform für KMU: wiederkehrende Arbeit automatisieren." | "Erstgespräch buchen" | System sans; teal `#0b6e6d` | Text plus a Power Automate flow screenshot | A real artefact on the first screen; the strongest of the seven |
| [IOZ](https://www.ioz.ch/) | "IOZ - spezialisiert auf Intranets, Prozesslösungen und Managementsysteme" | "Supportfall melden" (top bar) | Maven Pro; orange `#ea6212` | Banner with a GIF, then case-study teasers with logos | The H1 sits below the fold; the logo row carries the proof |
| [Noser Engineering](https://www.noser.com/) | "Hard- & Software Engineering - we know how" | "Jetzt entdecken" (AI card) | Trade Gothic; warm photo | Text and three image cards | Photo-led; cookie window on the phone (63%) |

Ambit Group (Winterthur, Power Platform practice) was found through job advertisements, not a company site: no official URL was found in search. Recorded as a local competitor to verify. HSO and Reply Cluster were found in search but show no Swiss base in the results, so they are not local.

Category defaults, counted from the seven: 5 of 7 use a cool accent; 4 of 7 open on a photo or video; 7 of 7 sans-serif only; 3 of 7 show a call to action on the first phone screen. In the 2026-11-21 text reads, none uses a drawn or diagrammed visual of its own work, except KMUpower's real flow screenshot.

Gap ketztek can own: a warm, non-blue accent (the logo's yellow and black); a visual language of the visitors' own documents and drawings; the honest-sizing line; and a first-screen next step that is the offer, not a dashboard.

## 5.3 Reference board

Eight references read or identified. Two shown here are verified only at text level; no reference is verified for its diagram quality.

| # | Reference | URL | Principle to borrow | What not to copy |
| --- | --- | --- | --- | --- |
| 1 | Sulzer | [sulzer.com](https://www.sulzer.com/) | A figure tied to a time stamp is a credible trust signal | Share-price widget: irrelevant to a 30-minute consulting call |
| 2 | Rieter | [rieter.com](https://www.rieter.com/) | A compact facts block with production sites and employees makes size honest without claiming it | Animated counters that read zero in a text capture |
| 3 | Bühler | [buhlergroup.com](https://www.buhlergroup.com/) | Organise by the reader's industry, not the company's structure | Tile grid of 16:9 images: breadth without precision |
| 4 | Stadler | [stadlerrail.com](https://www.stadlerrail.com/) | One strip of facts above the fold | Product renders as the only visual |
| 5 | Burckhardt Compression | [burckhardtcompression.com](https://www.burckhardtcompression.com/) | Dated, tagged news cards show activity | Engineers beside machines as a stock-like hero: ketztek has no such photos |
| 6 | Hilti | [hilti.com](https://www.hilti.com/) | Decision tools (selectors, charts) answer a practical question at once | Product promo in the hero |
| 7 | Implenia | [implenia.com](https://www.implenia.com/) | A KPI block with the prior-year comparison | Video teaser as the first screen |
| 8 | KMUpower (competitor, kept as reference) | [kmupower.com](https://kmupower.com/) | A real flow screenshot beside the text, one button | Its teal accent |

Diagram-led references (the brief asks for at least two): not verified. Candidates for the next pass, to read and screenshot before checkpoint 2: a Swiss automation supplier with published process diagrams, and a machine-maker's service page with a drawn assembly or maintenance view. Until they are read, the drawn-system direction rests on the local document vocabulary in the [design research](../design-brief/ketztek-design-research.md) (section 7), not on a reference.

## 5.4 Synthesis

For a plant manager or a construction operations lead in Switzerland, "professional and modern" means concrete things, not a style. The page has to show, on the first screen, what ketztek does, for whom and what the next step costs, with figures or documents rather than decoration. It should use a calm base with one warm accent, the logo's yellow, and black type with a consistent drawn language: rules, forms, process lines and dimension marks taken from the visitors' own paper and Excel documents. It should look finished without a single photograph, because none exists yet. Trust comes from precision: flush-left text, a grid that is visible in the drawings, honest units such as half an hour and two weeks, and no claim that cannot be backed. The same signals the Swiss industrial firms use (comparison figures, dated facts, decision tools) work for a young company when they are honest and few.
