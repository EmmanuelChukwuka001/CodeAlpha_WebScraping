# CodeAlpha Task 1: Web Scraping
## Nigerian Equipment Marketplace

This repository contains **Task 1 — Web Scraping** for the CodeAlpha Data Analytics Internship. The notebook collects publicly available equipment listings from [Equipment Marketplace Nigeria](https://equipmentmarket.ng/) and saves structured records for the EDA and visualization stages.

## Objective

Explore how listing data is delivered by the website, identify the public listings endpoint, test pagination, and collect a reproducible snapshot of approved listings while minimizing personal data collection.

## Repository contents

| File | Purpose |
|---|---|
| [`Task 1_Web scraping.ipynb`](Task%201_Web%20scraping.ipynb) | Step-by-step investigation of the website, API and pagination, followed by data collection |
| [`equipment_listings_raw.json`](equipment_listings_raw.json) | Collected raw listing records; input for Task 2 |
| [`requirements.txt`](requirements.txt) | Python dependencies |
| [`README.md`](README.md) | Project overview and run instructions |

## Workflow

1. Inspect the website HTML and confirm that listing cards are loaded dynamically.
2. Review `robots.txt` and inspect the site's JavaScript bundles to locate the public listings API.
3. Test the endpoint and confirm that pagination returns different pages.
4. Retrieve approved listings page by page, checking HTTP responses and pausing between requests.
5. Retain analysis-relevant fields and omit seller contact and owner details.
6. Save the results to `equipment_listings_raw.json`.

## Data snapshot

The notebook records **245 approved listings across 25 pages** in the collection run. The downstream EDA filters this dataset to **158 equipment listings** after excluding service listings. Live website content may change, so a new run may produce different results.

## Run locally

Python 3.10 or newer is recommended.

```bash
python -m pip install -r requirements.txt
jupyter notebook
```

Open `Task 1_Web scraping.ipynb` and run the cells in order. The source website and API must be reachable for live collection. The existing JSON file is included so the downstream analysis can use the saved snapshot without immediately re-scraping the site.

## Project sequence

- **Task 1 — Web Scraping:** this repository
- **Task 2 — Exploratory Data Analysis:** [CodeAlpha_ExploratoryDataAnalysis](https://github.com/EmmanuelChukwuka001/CodeAlpha_ExploratoryDataAnalysis)
- **Task 3 — Data Visualization:** [CodeAlpha_DataVisualization](https://github.com/EmmanuelChukwuka001/CodeAlpha_DataVisualization)

## Responsible collection and limitations

This is an educational snapshot of public listings, not a census of Nigeria's equipment market. Follow the website's terms and applicable rules, avoid collecting personal/contact fields, use a considerate request rate, and do not treat advertised details as independently verified facts.

*CodeAlpha Data Analytics Internship · Task 1: Web Scraping*
