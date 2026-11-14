# Zurich Airbnb Analysis

Solo project by Thivya Siva — Toronto Metropolitan University, Bachelor of Commerce, Business Technology Management (minor in Computer Science), expected April 2027.

An interactive **Power BI** dashboard examining Zurich Airbnb accommodation prices, neighbourhoods, room types and estimated costs.

## What the dashboard contains

- **KPI cards:** average price per night, total listings, average review score, average availability
- **Map:** listings by neighbourhood, sized/coloured by average price
- **Filters / slicers:** neighbourhood, room type, price range, minimum nights
- **Charts:** average price by room type, average price by neighbourhood, listings by room type, price distribution
- **Table:** listing details — name, neighbourhood, room type, price, minimum nights, reviews, availability

## Skills

Power BI, Power Query, DAX, data cleaning and transformation, dashboard design.

## Data

The dashboard was built from a Zurich Airbnb listings dataset with, per listing: id, name, neighbourhood, room type, price (per night), minimum nights, number of reviews, review score, availability (days per year) and estimated cost.

The original dataset is not included in this repository. A small synthetic sample in the same format is included at `data/sample_listings.csv` so the structure, Power Query steps and DAX measures can be inspected.

> **Note on the .pbix file:** no `.pbix` binary is included in this repository. The dashboard design, Power Query transformation steps and DAX measures are documented here so the report can be rebuilt in Power BI Desktop from the sample (or original) data.

## How to rebuild the dashboard in Power BI Desktop

1. Open Power BI Desktop → **Get Data → Text/CSV** → select `data/sample_listings.csv` (or the original listings file).
2. Apply the Power Query steps in `docs/power-query-steps.md`.
3. Create the measures in `dax/measures.dax` (Modelling → New measure, one per measure).
4. Build the report pages following `docs/dashboard-design.md`.

## Files

| File | Description |
| --- | --- |
| `docs/dashboard-design.md` | Page layout, visuals, KPIs and filters |
| `docs/power-query-steps.md` | Power Query transformation steps |
| `dax/measures.dax` | DAX measure definitions |
| `data/sample_listings.csv` | Synthetic sample listings (not the original dataset) |
