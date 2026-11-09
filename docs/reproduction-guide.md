# Reproduction Guide

## Explore the Report
1. Open the PBIX in Microsoft Power BI Desktop.
2. Use the Year slicer to explore 2010–2023; 2023 is the benchmark shown in the screenshots.
3. Review **The Human Crisis** for out-of-school counts, rates, geography, and gender exclusion.
4. Review **Beyond Access** for enrollment/completion and spending/governance comparisons.
5. Use Region and Income Level slicers; Page 1 also includes Country Name.

## Model
The report uses `Fact_Indicator`, `Dim_Countries`, `Dim_Year`, and `_Measures`. The dimensions filter the fact table. Confirm exact keys and relationship properties in Model view.

## Refresh/Rebuild
This guide supports opening and exploring the existing PBIX. Full refresh/rebuild steps are not yet reproducible because source file paths, exact extracts, Power Query M scripts, and data-source settings have not been documented.
