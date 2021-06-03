# MechaCar_Statistical_Analysis

## Overview 
AutosRUs newest prototype, MechaCar, is suffering from production troubles that are blocking the manufacturing team's progress.  Upper management called for the data analytics team to review the prodution data for insights that may help the manufacturing team.  In this challenge, we will do the following:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summmary statistics on the pounds per square inch (PSI) if the  manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statisical study to compare vehicle performance pf the MechaCar statiscal analysis


## Results

## Linear Regression to Predict MPG

Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = MechaCar_mpg_df)

Residuals:
     Min       1Q   Median       3Q      Max 
-19.4701  -4.4994  -0.0692   5.4433  18.5849 

Coefficients:
                   Estimate Std. Error t value
(Intercept)      -1.040e+02  1.585e+01  -6.559
vehicle_length    6.267e+00  6.553e-01   9.563
vehicle_weight    1.245e-03  6.890e-04   1.807
spoiler_angle     6.877e-02  6.653e-02   1.034
ground_clearance  3.546e+00  5.412e-01   6.551
AWD              -3.411e+00  2.535e+00  -1.346
                 Pr(>|t|)    
(Intercept)      5.08e-08 ***
vehicle_length   2.60e-12 ***
vehicle_weight     0.0776 .  
spoiler_angle      0.3069    
ground_clearance 5.21e-08 ***
AWD                0.1852    
---
Signif. codes:  
0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 8.774 on 44 degrees of freedom
Multiple R-squared:  0.7149,	Adjusted R-squared:  0.6825 
F-statistic: 22.07 on 5 and 44 DF,  p-value: 5.35e-11


The data above was created by importing MechaCar_mpg.csv into RStudio.  It was then a multiple linear regression was ran for all columns: mpg, vehicle length, vehicle weight, spoiler angle, ground clearance, and AWD.  Then a passed through the summary function to obtain the R-sqaured and p-value for the data.

1. 