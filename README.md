# NYC Motor Vehicle Collisions — Exploratory Analysis

**Python · Pandas · Matplotlib · Seaborn · Folium · Statsmodels**

Exploratory analysis of the [NYC OpenData Motor Vehicle Collisions](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95) dataset: about 2.16 million police-reported crashes. The goal is to understand what causes crashes, when they happen, and where they cluster, to inform road-safety priorities.

📓 **[View the notebook](tdspnima.ipynb)**

---

## Questions

1. What factors contribute most to crashes?
2. Which vehicle types are involved most often?
3. When do crashes happen — by hour of day and over the years?
4. How did COVID-19 affect crash volume?
5. Which boroughs and ZIP codes have the most crashes?
6. How many crashes, injuries, and deaths occurred in Jackson Heights (ZIP 11372)?

## Key Findings

1. **Human behavior drives most crashes.** Excluding "Unspecified," the top factors are driver inattention/distraction, failure to yield, and following too closely.
2. **Crashes peak around 4 PM**, during evening rush hour.
3. **COVID-19 caused a sharp drop** in monthly crashes starting in 2020, and volume has stayed lower since.
4. **Brooklyn has the most crashes of any borough**, while the heatmap shows the densest concentration in Midtown Manhattan.
5. **Jackson Heights (ZIP 11372)** recorded 8,817 crashes, 2,858 injuries, and 19 fatalities.

## Methods

- **Data quality:** measured missing values for every column; dropped records with missing or out-of-bounds coordinates before mapping.
- **Exploratory analysis:** top contributing factors, vehicle types, and injury/death counts by road-user type.
- **Time series:** crashes by hour of day, monthly trend, and seasonal decomposition (Statsmodels) of daily crash counts.
- **Geospatial:** crash heatmaps with Folium (all of NYC and Jackson Heights), a severity map on a 1,000-crash sample, and top 10 ZIP codes by crash count.

## Limitations

- The dataset has crash counts, not exposure (no traffic volume or registration data), so comparisons are totals, not rates.
- Many records are missing borough, ZIP code, or coordinates.
- Folium maps are saved as HTML files and don't render in GitHub's notebook preview.

## Next Steps

- Focus on pedestrian and cyclist injuries in Queens ZIP codes.
- Publish the findings as an interactive Tableau dashboard.
