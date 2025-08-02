# Predicting Economic Development Through Urban Growth Patterns

**A Data-Driven Approach to City Planning**

This project builds a predictive model using multiple linear regression to explore how different urban development strategies—densification, public transportation ridership, walkability, building compactness, and traffic congestion—affect the GDP of the 30 largest U.S. metropolitan statistical areas (MSAs).

## Data Sources

- **Census Reporter** – demographic data for the 30 largest MSAs  
- **Statista** – real GDP figures by metropolitan area  
- **APTA** – public transportation ridership statistics  
- **Walk Score** – city walkability indices  
- **Urban Stats** – building compactness and traffic congestion metrics

## Methodology

1. **Feature Selection & Collinearity Check**  
   - Examined five predictors: land density, walkability, public transport ridership, building compactness, traffic congestion.  
   - Ran Pearson correlation; none exceeded |r| ≥ 0.8, so we retained all variables.

2. **Model Building**  
   - Employed Ordinary Least Squares (OLS) via Python’s `statsmodels` to estimate coefficients.  
   - Final model:  
     > GDP = −178.43 + 0.31·(Land Density) − 1.40·(Walkability) + 11.35·(PT Ridership) + 2.21·(Building Compactness) + 109.17·(Traffic Congestion)

3. **Validation**  
   - R² = 0.879 (adjusted R² = 0.854), F-statistic p < 0.001.  
   - Spearman rank correlation between predicted and actual GDP: r ≈ 0.73.

## Results

- The model explains ~88% of the variance in GDP across the sampled MSAs.  
- Public transport ridership and land density emerged as the strongest positive predictors.  
- Visualizations show close alignment of predicted vs. actual GDP, with slight overestimation at the extremes.

## Future Work

- **Expand geographic scope**: include smaller MSAs or international cities.  
- **Additional features**: factor in income inequality, green space, or housing affordability.  
- **Non-linear models**: explore random forests or gradient boosting for potential performance gains.  
- **Interactive dashboard**: build a Flask/Streamlit app to let users tweak feature weights and visualize projections in real time.

## Authors

- **Zoe Hightower**  
- **Yve Hu**  
- **Tylan Joshi**  
