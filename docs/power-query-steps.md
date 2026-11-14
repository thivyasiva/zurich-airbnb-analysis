# Power Query transformation steps — Zurich Airbnb Analysis

Applied in Power Query Editor, in order, to the listings CSV.

1. **Get Data → Text/CSV** — load the listings file.
2. **Change types** — `price` to Currency / Decimal Number, `minimum_nights`, `number_of_reviews` and `availability_365` to Whole Number, `review_score` to Decimal Number.
3. **Remove blank / invalid rows** — filter out rows where `price` is null or `price <= 0`, and rows with a blank `neighbourhood` or `room_type`.
4. **Trim and clean text** — trim whitespace on `name` and `neighbourhood`; standardise `room_type` values (e.g. "Entire home/apt", "Private room", "Shared room", "Hotel room").
5. **Add price band column** — conditional column `Price Band`:
   - Under $100
   - $100–$199
   - $200–$299
   - $300+
6. **Add estimated cost column** — custom column `Estimated Monthly Cost` = `price * 30` (documented as an estimate, not a quoted rate).
7. **Remove duplicates** — remove duplicate rows by listing `id`.
8. **Load** — load the cleaned table as `Listings` into the Power BI model.
