# Methods: Spray Foam Insulation Cost Register (US, 2026)

## Collection
- **Starting list:** the outbound sources cited on sprayfoamguide.com's live cost pages (/cost/spray-foam-insulation-cost/, /cost/spray-foam-insulation-cost-per-board-foot/, /cost/spray-foam-insulation-cost-per-square-foot/, /cost/open-cell-vs-closed-cell-spray-foam-cost/), plus contractor price pages found by web search on 2026-10-21.
- **How:** each page was fetched live on 2026-10-21 (America/Chicago); the raw HTML and a text extraction were kept locally (raw/, not redistributed). Figures were recorded by hand into `src/build.py` with a short verbatim quote. The build normalizes whitespace and dashes and **fails** unless (a) the quote appears in that page's text and (b) every number in the row appears inside the quote.
- No figures came from calls, quote requests, forms, logins or paywalled content.
- **Coverage:** 44 rows from 12 source URLs and 11 independent businesses; 2 primary-tier rows and 42 secondary-tier rows; local rows cover GA, MN, TX.

## Tiers and grouping
- **Primary:** a business publishing its own price, price list, or quoted/completed project.
- **Secondary:** aggregator cost guides (Angi, HomeAdvisor, HomeGuide, etc.), publishers, manufacturers, calculator sites, news reports, and contractor pages that describe general market ranges rather than their own prices.
- Angi and HomeAdvisor share `independent_business` = "Angi Inc." Multiple pages from one company share one value and are not independent corroboration.

## Rules applied
1. No averaging, blending, midpoints or estimates. Any average is the source's own stated figure.
2. Open-ended figures ("$X+", "starting at") are recorded as stated and flagged in `notes`.
3. Scope and unit are recorded with every row; compare rows only when scope, unit and geography match.
4. Undated sources are `Not stated`; dates from page metadata are labeled as such.
5. Only individual figures and short quotes are reproduced; no page text is mirrored.

## Exclusions and gaps
- Not used: angi.com spray foam page returned HTTP 403 (HomeAdvisor, same company, carries matching figures); michigansprayfoaminsulation.com returned an empty page; envirofoamofamerica.com timed out.
- Not used: armorthane.com publishes a computed median of other guides (derivative), not prices.
- HomeGuide inconsistency: its DIY page lists professional open-cell at "$1.50 to $5.00 per board foot", matching its per-square-foot figure; this looks like a unit error and was not recorded.
- Gap: only one business publishing its own price (Toursque LLC, MN; location from phone area code). txfoampros.com and gasprayfoaminsulation.com do not name an operator and are treated as secondary.

## Limitations
- Published prices, not transactions; businesses choose what to publish.
- Not representative; few markets and few businesses per market.
- Aggregator ranges are national with undisclosed or partially disclosed methods.
- Point in time; re-check `source_url` before relying on a figure.
