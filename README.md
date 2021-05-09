# MechaCar_Statistical_Analysis

## Overview

MechaCar, AutosRU's newest prototype, is suffering from production troubles that are costly and run the risk of failing the teams deadlines.

The purpose of this analysis is to review production data for insights that may help circumvent manufacturing risks.


## Linear Regression to Predict MPG


Before moving on to Linear Regression, we take a look at the Correlation Coefficient Matrix to identify variables of interest.
There are no variables that share what is considered a strong correlation (1>= absolute value "r" >= 0.7), as revealed by the matrix. 

![Correlation_Coefficient_Matrix](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/corr_coeff_matrix.png)

Correlation Coefficient Matrix Highlights
- "MPG" and "Vehicle Length" share a moderate correlation of 0.61, which is the strongest of all variables, with "MPG" and "Ground Clearance" coming in second at a weak-moderate correlation level of 0.33.
- When we square the Vehicle Length coefficient, we get R-squared of approximately 0.37.  This indicates that Vehicle length will only predict about 37% of mpg observations.   

We should run a Multiple Linear Regression model to test for more prediction reliability. 

![MPG Summary Statistics](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/mpg_summary_statistics.png)

Multiple Linear Regression Highlights
- According to our results, vehicle length and ground clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model.  In other words the vehicle length and ground clearance have a significant impact on mpg.
- In addition, the p-value of our linear regression analysis is 5.35e-11, which is much smaller than our assumed significance level of 0.05%.  Therefore, we can state that there is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.
- R-squared of approximately 0.71.  This indicates that the multiple linear regression will predict 71% of mpg observations.

