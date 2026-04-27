# Scraping SEC (Nigeria)

A Python web scraper that extracts capital-market operator (CMO) data from the [Nigerian Securities and Exchange Commission](https://sec.gov.ng/cmos/) registry and exports it to an Excel spreadsheet for downstream analysis.

## What it does

- Iterates through every page of the SEC CMO registry using Selenium.
- For each operator, extracts the main row data plus the "Headquarters", "Sponsored Individuals", and "Directors" tabs hidden behind the row's expand control.
- Writes the consolidated dataset to an Excel file via `openpyxl`.

![Excel output preview](Data%20on%20Excel.png)

## Stack

- Python 3
- Selenium (Chrome WebDriver)
- openpyxl
- Pipenv

## Run

```bash
pipenv install
pipenv run python get_info.py
```

A matching `chromedriver` must be available on `PATH` or supplied to the `Browser` class.
