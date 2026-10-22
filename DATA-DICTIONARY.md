# Data dictionary

| column | meaning |
|---|---|
| id | Stable row id (prefix = topic) |
| service_component | What is priced |
| scope | Scope/type summary as stated by the source (our wording) |
| low_usd / high_usd | Published range ends, USD as stated. Blank if a single figure |
| point_or_stated_average_usd | A single published price, a starting price, or the source's own stated average (see notes) |
| unit | Unit of the figure (e.g., USD per linear ft, installed) |
| geography | Market the figure applies to, as stated or as shown by the publisher's location |
| state | US state code(s); blank for national |
| source_publisher | Who published the page |
| independent_business | Grouping key for affiliated publishers (Angi + HomeAdvisor = Angi Inc.) |
| source_url | Page the figure was taken from |
| source_date | Page date as stated, or from page metadata (labeled), or `Not stated` |
| retrieved_date | Date fetched (YYYY-MM-DD, America/Chicago) |
| source_type | Kind of page |
| source_tier | primary / secondary (see METHODS) |
| record_type | `price` |
| quoted_text | Short verbatim excerpt containing the figure (whitespace normalized); used by the build to verify the row |
| notes | Caveats: open-ended ranges, single projects, inconsistencies |
