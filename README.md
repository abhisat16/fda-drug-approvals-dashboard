# FDA Drug Approvals Dashboard — September 2026

An interactive dashboard of every US FDA drug approval action in September 2026, grouped by therapeutic area and approval type, with advanced filters and a searchable register.

**Live dashboard:** https://abhisat16.github.io/fda-drug-approvals-dashboard/

## What it shows

- **356 unique approval actions** from FDA's monthly Drugs@FDA report (380 rows as FDA lists them; 24 are repeat rows for different strengths or product names of the same approval).
- Share of approvals by **therapeutic area** (oncology, cardiovascular, neurology and others) and by **approval type** (novel drugs, new indications, new generics, labeling and manufacturing updates).
- **Advanced filters**: therapeutic area, approval type, application type (NDA / BLA / ANDA), FDA submission class, status, date range and company, all multi-select.
- A switch between counting **unique approvals (356)** and **every FDA row (380)**.
- A searchable, sortable register where each row links to its **Drugs@FDA record** (approval letters, labels, reviews).

## Data

- Source: [Drugs@FDA — Approvals by month, September 2026](https://www.accessdata.fda.gov/scripts/cder/daf/index.cfm?event=reportsSearch.process&rptName=1&reportSelectMonth=9&reportSelectYear=2026&nav)
- Cleaned data: [`data/fda_approvals_sep_2026.csv`](data/fda_approvals_sep_2026.csv)
- Coverage: CDER approvals (NDAs, ANDAs and CDER-reviewed BLAs). Vaccines and cell and gene therapies reviewed by CBER are not included.
- Therapeutic area is assigned from each drug's primary use; FDA does not publish this field. Multi-use drugs (for example rituximab, everolimus) are placed in their main area.
- "Novel drugs" are FDA Type 1 new molecular entities plus first-time biologics.

## Run it locally

The dashboard is a single self-contained `index.html` with the data built in. Open it in any browser; no server or install is needed.

## Roadmap

- Automatic monthly fetch of the FDA report
- 10-year history (2016 onward) with trend charts
- Automated therapeutic-area tagging from drug classes (RxNav / ATC)

---

Built by Dr. Abhijeet Satapathy, AI & Data Science, IIHMR Bangalore.
