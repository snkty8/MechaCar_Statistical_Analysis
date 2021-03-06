# MechaCar_Statistical_Analysis

## Overview 
AutosRUs newest prototype, MechaCar, is suffering from production troubles that are blocking the manufacturing team's progress.  Upper management called for the data analytics team to review the prodution data for insights that may help the manufacturing team.  In this challenge, we will do the following:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summmary statistics on the pounds per square inch (PSI) if the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statisical study to compare vehicle performance pf the MechaCar statiscal analysis


## Results

## Linear Regression to Predict MPG

![image](https://github.com/snkty8/MechaCar_Statistical_Analysis/blob/main/images/Linear_Regression_to_Predict_MPG_Stats.png)


The data above was created by importing MechaCar_mpg.csv into RStudio.  It was then ran through a multiple linear regression for all columns: mpg (dependent variable), vehicle length, vehicle weight, spoiler angle, ground clearance, and AWD.  Then a passed through the summary function to obtain the R-sqaured and p-values.

1. In the image above, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. According this information vehicle length and ground clearence are statistically unlikely to provide random amounts of variance to the linear model.  So, this means the length and ground clearance of the prototype has a signficant impact on mpg. 

2. The slope of the linear model is nonzero, and a positive slope.  This comes from the positive R-squared value, the multiple R-squared value: 0.7149.  These are moderately strong values that indidcate for every positive increase in one variable, there is a positive increase of a fixed proportion in the other. 

3. This linear model does an adquate job of predicting the mpg of the Mechacar prototypes. From the R-sqaured value, there is 71.5% chance for this model producing effective models for the future.  Also, the p-value of 5.35e-11, which is far less than 0.05.  This indicates the results are replicable.



## Summary Statistics on Suspension Coils

    - Total Summary
![image](https://github.com/snkty8/MechaCar_Statistical_Analysis/blob/main/images/total_summary.png)

    - Lot Summary
![image](https://github.com/snkty8/MechaCar_Statistical_Analysis/blob/main/images/lot_summary.png)

1. A large variance indicates that numbers in the set are far from the mean and far from each other. A small variance, on the other hand, indicates the opposite. As seen in the images above, lot 1 has a very small variance and lot 3 is the complete opposite. This indicates the suspensions in lot 1 are almost identical, while the ones in lot 3 are all over the place.  From the data above, lots 1 and 2 do not exceed the 100 pounds per square inch, while lot 3 does.

## T-Tests on Suspension Coils
T-test for all lots for PSI
![image](https://github.com/snkty8/MechaCar_Statistical_Analysis/blob/main/images/t_test_PSI.png)

T-test for Lot 1
![image](https://github.com/snkty8/MechaCar_Statistical_Analysis/blob/main/images/t_test_lot_1.png)

T-test for Lot 2
![image](https://github.com/snkty8/MechaCar_Statistical_Analysis/blob/main/images/t_test_lot_2.png)

T-test for Lot 3
![image](https://github.com/snkty8/MechaCar_Statistical_Analysis/blob/main/images/t_test_lot_3.png)

1. I performed a T-test to determine if all manufacturing lots and each lot individually were statiscally different from the population of 1,500 pounds per square inch. My null hypothesis was that there is no statistical difference and my alternate hypothesis was that there is a statistical difference.  The p-value for for all lots was: 0.51.  This means there is not enough statistical evidence to reject the null hypothesis.  Meaning the mean of the population for all lots are not statistically different from the manufactuers. Individually, lot 1 had a p-value of 1, lot 2 had a p-value of 0.6072, and lot 3 had a p-value of 0.04168.  Lots 1 and 2 show statiscal evidence they are different from the population, while lot 3 is not different. We can reject the null hypothesis for lot 3, while we cannot for lots 1 and 2. 

## Study Design: MechaCar vs Competition

In this section we would like to determine how MechaCar stand up statiscally stand up against competing types of cars. My null hypothesis would be there is not statically difference different between the cars.  My alternate hypothesis is there a difference between the MechaCar and other companies. A lot of companies claim do the same things and even more, but how can we prove this is or is not the case.To test these hypotheses, we can use a few different metrics including: cost, city or highway fuel efficiency, horse power, maintenance cost, and safety rating.  We should use a large sample size for each competitor, let???s say 2000 in total.  For each car we would need the final cost, fuel effiency for a certain distance, the average horsepower for the distance, maintenance costs for broken cars, and the safety rating for each. A mulitple linear test could be performed for all categories.  The cost would be the dependent variable, and the rest of the metrics as independent variables. This would tell us if there is any variance in cost amoung the competitors. An anova test could be used in the same way to determine the relationship between the dependent and independent variables.  Using MechaCar and each of the competitors, we could also use a two-sample t-test to determine the statiscal mean distrubution between them. 


