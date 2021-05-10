# MechaCar_Statistical_Analysis

## Overview

MechaCar, AutosRU's newest prototype, is suffering from production troubles that are costly and run the risk of failing the teams deadlines.

The purpose of this analysis is to review production data for insights that may help circumvent manufacturing risks.


## Linear Regression to Predict MPG


Before moving on to Linear Regression, we take a look at the Correlation Coefficient Matrix to identify variables of interest.
There are no variables that share what is considered a strong correlation (1>= absolute value "r" >= 0.7), as revealed by the matrix. 

![Correlation_Coefficient_Matrix](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/corr_coeff_matrix.png)

####Correlation Coefficient Matrix Highlights
- "MPG" and "Vehicle Length" share a moderate correlation of 0.61, which is the strongest of all variables, with "MPG" and "Ground Clearance" coming in second at a weak-moderate correlation level of 0.33.
- When we square the Vehicle Length coefficient, we get R-squared of approximately 0.37.  This indicates that Vehicle length will only predict about 37% of mpg observations.   

We should run a Multiple Linear Regression model to test for more prediction reliability. 

![MPG Summary Statistics](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/mpg_summary_statistics.png)

#### Multiple Linear Regression Highlights
- According to our results, vehicle length and ground clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model.  In other words the vehicle length and ground clearance have a significant impact on mpg.
- In addition, the p-value of our linear regression analysis is 5.35e-11, which is much smaller than our assumed significance level of 0.05%.  Therefore, we can state that there is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.
- R-squared of approximately 0.71.  This indicates that the multiple linear regression will predict 71% of mpg observations.


## Summary Statistics on Suspension Coils

The design specification for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI).  We want to confirm that the manufacturing data meets this design specification for all manufacturing lots in total and each lot individually.

Weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots in the Suspension_Coil.csv dataset.  The dataset is comprised of the PSI metric for 150 vehicles produced at 3 lots. 

#### Total Summary Table
![Total Summary](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/total_summary.png)

#### Lot Summary Table
![Lot_Summary](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/lot_summary.png)

#### PSI Summary Results

- Per the Total Summary above, PSI Variance for all lots combined is 62.29 pounds per square inch. This satisfies the design specification requirements.
- Per the Lot Summary above, PSI Variance for Lots 1 thru 3 yield 0.98, 7.47 and 170.29 pounds per square inch respectively. 

Initially, we are inclined to believe that lot 3 is doing something wrong, as it is the only lot that exceeds the 100lb weight capacity.  However, looking at the Median and Mean, we can see that the data is Left Skewed which indicates there is a higher probability that lower weights exist at this location than others.  This is evidenced by the Standard Deviation being higher for this location as well. 

We recommend that the manufacturing team revisit its approach with vehicle allocation to these lots in order to normalize distributions so they each meet the design specifications. 

## T-Tests on Suspension Coils

We want to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.  Using our knowledge of R, we will perform t-tests to calculate the p-value and compare it against a significance level of 0.05.

#### Here are the T-Test results:

#### All Manufacturing lots
![All_Lots_TTest](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/one_sample_ttest.png)

At a significance level of the common 0.05 percent, our p-value of 0.06 is above the significance level.  Therefore, we do not have sufficient evidence to reject that there is a statistical difference between All Manufactuting lots and the population mean.  The two means are statistically similar.

#### Lot 1
![Lot1_TTest](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/lot1_ttest.png)

At a significance level of the common 0.05 percent, our p-value of 1.0 is above the significance level.  Therefore, we do not have sufficient evidence to reject that there is a statistical difference between Lot 1 and the population mean.  The two means are statistically similar.

#### Lot 2
![Lot2_TTest](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/lot2_ttest.png)

At a significance level of the common 0.05 percent, our p-value of 0.61 is above the significance level.  Therefore, we do not have sufficient evidence to reject that there is a statistical difference between Lot 2 and the population mean.  The two means are statistically similar.

#### Lot 3
![Lot3_TTest](https://github.com/ashley-green1/MechaCar_Statistical_Analysis/blob/main/resources/lot3_ttest.png)

At a significance level of the common 0.05 percent, our p-value of 0.042 is below the significance level.  There is sufficient statistical evidence to reject that there is a statistical difference between Lot 3 and the population mean. The two means are statistically different. 

## Study Design: MechaCar vs Competition



