# IQAir-historical-data-scraper

**How to use:** download the notebook (`IQAir_scraper.ipynb`) and follow the inline instructions.

This vibe-coded project scrapes high‑quality historical PM2.5 air quality data from IQAir without using the paid internal API.
It collects all PM2.5 columns for a chosen continent, together with:

Rank
City
Country
Time periods, following the current layout on the website, for example:
| 2024 | Sty | Lut | Mar | Kwi | Maj | Cze | Lip | Sie | Wrz | Paź | Lis | Gru | 2023 | 2022 | 2021 | 2020 | 2019 | 2018 | 2017 |
These time‑period columns are stored generically as AQI_1, AQI_2, … in the raw output, where:

AQI_1 corresponds to the current full year (e.g. 2024)
AQI_2–AQI_13 correspond to months from January to December of the current year
AQI_14+ correspond to previous full years (e.g. 2023, 2022, …)
A separate cleaning step converts these technical names into readable labels like AQI_2024, Jan_2024, …, adjusting automatically when the website’s current year changes.
