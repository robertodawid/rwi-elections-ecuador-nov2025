# Analysis of Wealth (RWI) and Voting Patterns in Ecuador

This project analyses the relationship between the **Relative Wealth Index (RWI)** and voting behaviour in the most recent Ecuadorian referendum. Using high-resolution spatial data from Meta and official electoral results, we investigate whether socioeconomic status influenced support for four key ballot questions.

![rwi-Ecuador](/outputs/fig/rwi_map_ecuador.pngouputs/rwi_map_ecuador.png)

## 📌 Project Overview

The exercise explores a central question in political economy: **Do wealthier households vote differently on institutional and security reforms?** 

I utilise **H3 Hexagonal Hierarchical Geospatial Indexing** to bridge the gap between point-level wealth data and area-level voting results, allowing for a granular analysis of the "wealth-vote" gradient across Ecuador.

## 📊 Data Sources

- **Relative Wealth Index (RWI):** Provided by Meta (Data for Good), offering micro-estimates of wealth at a 2.4km resolution based on connectivity and satellite imagery.
- **Electoral Results:** Official parroquia-level (parish) data from the Consejo Nacional Electoral (CNE) of Ecuador.
- **Geospatial Boundaries:** Parroquia-level shapefiles for spatial joining and administrative mapping.

## 🛠 Methodology

1.  **Spatial Aggregation:** RWI point data is aggregated into H3 hexagons (Resolution 8, ~0.7km²).
2.  **Voting Mapping:** Parroquia-level voting results are distributed across H3 hexagons using spatial intersections.
3.  **Statistical Modeling:** 
    - **Weighted Least Squares (WLS):** To analyse the linear relationship between mean RWI and Yes/No percentages.
    - **Binomial Logistic Regression:** To model the probability of a "Yes" vote as a function of wealth.
4.  **Visualisation:** Choropleth maps of wealth and voting support, alongside scatterplots with trendlines.

## 🚀 Key Findings

*   **Wealth Neutrality:** Initial regression results show that wealth (RWI) is not a statistically significant predictor of the "Yes" vote for the analysed questions (p-values > 0.05).
*   **Low Explanatory Power:** R-squared values suggest that wealth explains less than 7% of the variation in voting patterns, indicating that political or regional factors likely play a larger role.
* **Cross-Class Consensus:** The lack of a wealth gradient suggests a degree of socioeconomic consensus (or uniform polarisation) across the analysed measures.

## 💻 Installation & Usage

1. **Clone the repo:**
   ```bash
   git clone https://github.com/yourusername/rwi-elections-ecuador.git
