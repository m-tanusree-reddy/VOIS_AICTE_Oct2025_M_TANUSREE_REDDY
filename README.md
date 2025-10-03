# Airbnb-Hotel-Booking-Analysis
# Airbnb Data Analysis

## About the Author

- **Name:** Nihal DR
- **College:** CMR Institute of Technology
- **Branch:** Artificial Intelligence & Data Science (AI&DS)

## Project Title

Airbnb Listings Analysis — Insights into property types, pricing, hosts, and availability

## Problem Statement

This project analyses an Airbnb listings dataset to answer specific business questions:

1. What are the different property types in the dataset?
2. Which neighbourhood group has the highest number of listings?
3. Which neighbourhood groups have the highest average prices for Airbnb listings?
4. Is there a relationship between the construction year (or year built) of a property and price?
5. Who are the top 10 hosts by calculated host listing count?
6. Are hosts with verified identities more likely to receive positive reviews?
7. Is there a correlation between the price of a listing and its service fee?
8. What is the average review rating for listings, and does it vary by neighbourhood group and room type?
9. Are hosts with a higher calculated host listings count more likely to maintain higher availability throughout the year?

---

## Dataset

* Source: *Replace with your CSV/Parquet file path or link (e.g., `data/listings.csv`)*
* Key columns expected (common Airbnb schemas):

  * `id`, `name`, `host_id`, `host_name`, `host_listings_count_calculated` (or `host_listings_count`), `neighbourhood_group`, `neighbourhood`, `latitude`, `longitude`, `room_type`, `price`, `service_fee`, `year_built` (or `construction_year`), `reviews_per_month`, `review_scores_rating`, `number_of_reviews`, `availability_365`, `host_identity_verified` (or similar)

> **Note:** if your dataset uses different column names, adapt the code below accordingly.

---

## Environment & Reproducibility

Install required packages (Python 3.8+ recommended):

```bash
pip install pandas numpy matplotlib seaborn scipy jupyterlab
```

Run analysis in a notebook or script. Example:

```bash
jupyter lab
# open notebooks/airbnb_analysis.ipynb
```

---


## Visualizations (suggested)

* Bar chart: counts of property types
* Choropleth or scatter map: listings by neighbourhood
* Boxplots: price distribution per neighbourhood group
* Scatter + regression: price vs construction year
* Heatmap: average review score by neighbourhood and room type


## Example interpretation template (fill with your computed results)

* **Property types:** *e.g.,* Apartment (45%), House (30%), Townhouse (10%), etc.
* **Top neighbourhood group by listings:** *e.g.,* `Manhattan` with 4,500 listings.
* **Highest average price groups:** *e.g.,* `Manhattan` (avg $200) > `Brooklyn` ($120) > ...
* **Construction year vs price:** *e.g.,* Pearson r = -0.12 (weak negative correlation) — interpret whether older/newer properties command higher prices.
* **Top 10 hosts:** list of host IDs/names with counts.
* **Identity verification & reviews:** *e.g.,* Verified hosts mean rating 4.8 vs non-verified 4.6; t-test p = 0.02 → statistically significant at α=0.05.
* **Price vs service fee correlation:** *e.g.,* r = 0.65 (moderate positive correlation), likely because service fee is a function of price.
* **Average review rating by group/room type:** include pivot table and call out notable differences.
* **Host listings vs availability:** *e.g.,* correlation = -0.03 (no relationship) or positive — discuss business meaning.

---

## Conclusions & Business Recommendations

* Highlight the highest-value neighbourhoods for investment.
* Consider targeting property types with high occupancy and above-average review scores.
* If verified hosts consistently receive better reviews, encourage identity verification via onboarding improvements.
* Price–service fee relationship: consider dynamic pricing and transparent fee structures.

---

## Reproducibility & Files in Repository

* `data/` — raw dataset (or a pointer to download link)
* `notebooks/airbnb_analysis.ipynb` — exploratory notebook with charts and narrative
* `scripts/` — helper scripts to clean data and generate figures
* `figs/` — images produced by visualizations
* `README.md` — this file

