# Dashboard design — Zurich Airbnb Analysis

## Page 1: Overview

| Visual | Type | Fields |
| --- | --- | --- |
| Average price per night | KPI card | `Average Price` measure |
| Total listings | KPI card | `Total Listings` measure |
| Average review score | KPI card | `Average Review Score` measure |
| Average availability (days/year) | KPI card | `Average Availability` measure |
| Listings map | Filled / bubble map | Neighbourhood, `Average Price` |
| Average price by room type | Bar chart | Room type, `Average Price` |
| Listings by room type | Donut chart | Room type, `Total Listings` |

## Page 2: Neighbourhoods & pricing

| Visual | Type | Fields |
| --- | --- | --- |
| Average price by neighbourhood | Bar chart (sorted descending) | Neighbourhood, `Average Price` |
| Price distribution | Histogram / column chart | Price (binned) |
| Listing details | Table | Name, neighbourhood, room type, price, minimum nights, reviews, availability, `Estimated Monthly Cost` |

## Slicers (both pages)

- Neighbourhood (multi-select)
- Room type (Entire home/apt, Private room, Shared room, Hotel room)
- Price range (slider)
- Minimum nights

## Design notes

- One consistent colour palette across pages; price is the accent measure.
- KPI cards at the top of Page 1 so the headline numbers are visible first.
- The map and the neighbourhood bar chart are cross-filtered: selecting a neighbourhood on one updates the other.
- Estimated costs use the DAX measures in `dax/measures.dax` — they are not hard-coded in the visuals.
