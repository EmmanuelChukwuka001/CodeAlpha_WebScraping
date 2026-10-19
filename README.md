# CodeAlpha Web Scraping — Nigerian Equipment Marketplace

This repository contains **Task 1** of my CodeAlpha Data Analytics internship. The project explores how to collect publicly available equipment-listing data from the Nigerian equipment marketplace website and prepare a structured dataset for analysis.

## Project objective

- Inspect the public website and its listing structure.
- Explore the site's public listings API and pagination.
- Retrieve approved listings in pages using Python.
- Keep only fields needed for analysis and omit seller contact/owner fields for privacy.
- Save the collected records for the downstream EDA and visualization tasks.

## Tools and libraries

- Python
- `requests` for HTTP requests
- `json` for structured data storage
- `pandas` for tabular data inspection and preparation
- Jupyter Notebook

## Workflow

1. Inspect the marketplace website and understand how listing data is exposed.
2. Test the public listings endpoint and inspect the response structure.
3. Test pagination with a small page of results.
4. Iterate through pages with request timeouts and response-status checks.
5. Retain the fields relevant to equipment inventory analysis.
6. Save the resulting dataset for Tasks 2 and 3.

## Running the notebook

1. Install Python 3.10+ and Jupyter.
2. Install the dependencies:

   ```bash
   pip install requests pandas jupyter
   ```

3. Open the web-scraping notebook in Jupyter Notebook or JupyterLab.
4. Run cells in order. The source website/API must be reachable for live collection.

## Output and next steps

The intended output is a JSON dataset of public listing fields that can be used by the Exploratory Data Analysis and Data Visualization notebooks. The downstream notebooks expect the collected file to be available locally.

## Responsible data collection

This project is for learning and analysis. Use only publicly available information, follow the website's terms and applicable laws, avoid collecting personal/contact fields, and make requests at a considerate rate. Live API responses may change over time.

## Internship

Completed as part of the **CodeAlpha Data Analytics Internship** — Task 1: Web Scraping.
