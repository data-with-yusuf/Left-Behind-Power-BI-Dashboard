# Technical Documentation

## Report Overview
**Left Behind: A Global Analysis of Primary Education Access and Equity** is a two-page Power BI report covering 2010–2023, with 2023 as the benchmark/default year.

- **The Human Crisis:** out-of-school counts and rates, geographic distribution, country ranking, and gender exclusion.
- **Beyond Access:** enrollment and completion comparisons, completion gender gaps, and contextual comparisons involving education spending and government effectiveness.

## Data Model
The model contains:
- `Fact_Indicator` — indicator observations, including Country Code, Series Code, Year, Indicator, Category, Series, and Sub_Category.
- `Dim_Countries` — country attributes including Country Code, Name, Region, Income Level, iso2Code, Latitude, and Longitude.
- `Dim_Year` — Year and Decade.
- `_Measures` — measure organization.

The model diagram shows one-to-many relationships from `Dim_Countries` and `Dim_Year` to `Fact_Indicator`, filtering toward the fact table. The expected fact grain is country, year, and indicator series; confirm exact keys in Model view before rebuilding.

## Report Controls
- Page 1 slicers: Year, Country Name, Region, Income Level.
- Page 2 slicers: Year, Region, Income Level.
- The report supports 2010–2023; 2023 is the benchmark shown in supplied screenshots.
- Missing selected-year observations remain blank rather than being treated as zero or silently replaced with a latest year.

## Visual Inventory
### The Human Crisis
- Map: country iso2Code; Out of School Rate %; tooltips include Out of School Children, Out of School Rate %, Data Availability.
- KPI cards: Out of School Children, Out of School Rate %, GPI, Countries with Data.
- Country ranking: Country Name by Out of School Children; tooltip includes Out of School Rate %, GPI, Enrollment Gender Gap.
- Gender exclusion table: Country Name, Out of School Children, Out of School Girls Rate %, Out of School Boys Rate %, OOS Gender Gap.
- Insight card: Country Snapshot, Gender Status, Data Availability.

### Beyond Access
- Completion gender-gap bar chart: Completion Gender Gap; tooltip includes Completion Gender Gap Magnitude, Female Completion Rate, Male Completion Rate.
- Spending vs completion scatter: Edu Spend % GDP (x), Completion Rate (y), country category.
- Governance vs completion scatter: Gov Effectiveness (x), Completion Rate (y), country category.
- Enrollment vs completion scatter: Enrollment Rate (x), Completion Rate (y), country category.

## Verification Status
Report page structure, visible slicers, model tables, and visual field assignments were reviewed from the PBIX definition and screenshots. DAX formulas, exact numerator/denominator logic, slicer sync, edit interactions, visual filters, sort order, and Top N settings remain pending direct model verification.
