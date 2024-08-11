## Executive Summary

Brooklyn home prices for single-family homes and condos likely increased significantly in Q4 2020 compared to Q3 2020. Using linear regression, I found a statistically significant positive effect at a 97.5% confidence level. While some model assumptions were violated and the confidence interval is wide, the overall trend suggests a price increase.

### Motivation

This analysis explores the change in prices for single-family homes and condos in Brooklyn between Q3 and Q4 of 2020, a period heavily influenced by the COVID-19 pandemic. Understanding these changes offers insights into the housing market's health in Brooklyn.

## Data Overview

- **Source**: Sales data for Brooklyn single-family homes and condos from 2016 to 2020.
- **Filtering**: Excluded homes sold for less than $10,000, more than $6,000,000, and certain atypical housing types (e.g., Cape Cods, mansions).
- **Final Dataset**: 13,474 sales records.

## Approach

- **Initial Analysis**: Comparing average prices between quarters could be misleading due to variations in the types of homes sold.
- **Modeling Strategy**: A linear regression model was used to control for factors such as ZIP code, neighborhood, square footage, building classification, and sale timing.

## Methodology

- **Model Construction**:
  - Variables included ZIP code, neighborhood, gross and land square footage, building classification, and sale timing.
  - ZIP codes were grouped using Tukey’s test; neighborhoods were grouped by mean purchase prices.
## Results

- **Performance**: 
  - The model explains 61% of the variation in prices, with a root mean squared error of $445,177.40.
  - The estimated increase in Q4 2020 prices over Q3 2020 is $70,459, significant at the 97.5% level.

## Limitations and Takeaway

- **Limitations**: 
  - The wide confidence interval ($8,859.37 to $132,059.50) may result from small sample sizes in Q3 and Q4 2020.
  - The model's assumptions of independent and identically distributed errors were violated.

- **Conclusion**: Despite limitations, the analysis strongly suggests that Brooklyn home prices increased in Q4 2020. While the exact amount is uncertain, the trend is clear.
