## Executive Summary

Using linear regression, I estimate that Brooklyn purchase prices for single-family homes and condos significantly increased in Q4 2020 compared to Q3 2020. A linear regression model is an appropriate tool to determine shifts in Brooklyn home purchase prices, as it allows for the disentanglement of the price effect from other factors influencing sale prices. Although a wide confidence interval and violations of ordinary least squares model assumptions mean the exact scale of the increase cannot be confidently assessed, the positive result is statistically significant at a 97.5% level. Thus, I am reasonably confident that the true price effect is positive.

### Motivation

This report seeks to answer how prices of single-family homes and condominiums changed between Q3 and Q4 of 2020 in Brooklyn, NY. The housing market has been significantly impacted by the COVID-19 pandemic, and changes in Brooklyn home prices between these two quarters may serve as a proxy for the health of the housing market in this area.

## Data Overview

- **Data Source**: The analysis includes sales of single-family homes and condos in Brooklyn from 2016 to 2020.
- **Filtering**: Excluded homes sold for less than $10,000 or more than $6,000,000, as well as Cape Cods, summer cottages, mansions, and condominium rentals. 
- **Final Dataset**: Contains 13,474 records of housing purchases after exclusions.

## Approach

- **Initial Consideration**: Simply comparing the mean prices of homes sold in both quarters could be misleading, as it doesn’t account for the variability in the types of homes sold.
- **Modeling Strategy**: A linear model was used to isolate the time effect on sale prices, controlling for ZIP code, neighborhood, square footage, building classification, and timing of the sale.

## Methodology

- **Linear Model Construction**: 
  - Included ZIP code, neighborhood, gross and land square footage, building classification, and timing of sale as predictors.
  - ZIP codes were grouped using Tukey’s Honestly Significant Difference test.
  - The model includes interaction terms between gross and land square feet and discretizes the sale date.
  - The model’s equation:
    \[
    \text{Price} = \beta_0 + \beta_1 \times (\text{Gross Sq. Ft.}) + \beta_2 \times (\text{Land Sq. Ft.}) + \beta_3 \times (\text{Gross Sq. Ft.} \times \text{Land Sq. Ft.}) + \text{Other Predictors} + \epsilon
    \]

## Results

- **Model Performance**: 
  - The model explains 61.02% of the total variation in home purchase prices with a root mean squared error of $445,177.40.
  - The estimated coefficient for Q4 2020 indicates an average price increase of $70,459 when compared to Q3 2020, significant at a 97.5% level.

## Limitations and Takeaway

- **Limitations**: 
  - The confidence interval for the price increase is wide ($8,859.37 to $132,059.50), likely due to small sample sizes for Q3 and Q4 2020.
  - The model violates the assumptions of ordinary least squares regression, as the error terms are not independent and identically distributed.
  
- **Main Takeaway**: Despite these limitations, the positive and significant increase in prices suggests that Brooklyn home purchase prices likely rose in Q4 2020. The exact magnitude of the increase remains uncertain, but the overall trend is clear.
