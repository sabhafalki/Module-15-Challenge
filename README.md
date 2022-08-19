# Module-15-Challenge  MechaCar_Statistical_Analysis
# Overview of Project #
The purpose of this Project is to help the AutosRUs, new prototype,the MechaCar, by analysing the insights of production data provided by the manufacturing team. So, that they can progress the production.

The analysis consisted of the following:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes. 
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

# Resources #
- **Data Source**: MechaCar_mpg.csv,Suspension_Coil.csv.<br>
- **Data Tools**: tidyverse, dplyr, ggplot2 and MechaCarChallenge.RScript.<br>
- **Software**: RStudio and R.<br>

# Summary
## Linear Regression to Predict MPG
**Results of linear regression function:**<br>
![linear_regression1](/Image/linear_regression1.png) <br><br>

**Results of linear regression model - p-value and r-squared value:**<br>
![Summery](/Image/Summery.png) <br><br>

**1) Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?**<br>
Using the Pr(>|t|) values generated in the linear regression model, we see that vehicle length and ground clearance, along with the intercept, provide a non-random amount of variance to the mpg values in the dataset.
- vehicle_length with p-value = 2.60e-12 which is « 0.05
- ground_clearance with p-value = 5.21e-08 which is « 0.05

**2) Is the slope of the linear model considered to be zero? Why or why not?**<br>
Since p-value is less than zero (5.35e-11), the slope is not equal to zero. There would be no correlation between mpg and the independent variables. 

**3) Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**<br>
According to the summary output, the r-squared value is 0.71, which predicts that approximatley 71% of all mpg predictions will be correct when using this linear model.

## Summary Statistics on Suspension Coils
**Total Summary Table**<br>
![Summary_group_by](/Image/Summary_group_by.png) <br><br>

**Lot Summary Table**<br>
![lot_summary](/Image/lot_summary.png) <br><br>
1) The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?<br>
- The summary statistical data for suspension coils across all lots, manufacturing is meeting specifications. However, when broken down to individual lot variance, lots 1 & 2 meet specs, but lot 3 is out of spec with a variance of 170.29 psi, exceeding the 100 psi variance max design specification.
## T-Tests on Suspension Coils
**All Three Lots Combined Test**<br>
![lot_all](/Image/lot_all.png) <br><br>
The p value is over the significance level of 0.05 which means that the null hypothesis cannot be rejected and the mean of all the lots combined is statistically similar to the population mean of 1500.
**Lot 1 Test**<br>
![lot1](/Image/lot1.png) <br><br>
The p value is over the significance level of 0.05 which means that the null hypothesis cannot be rejected and the mean of lot 1 is statistically similar to the population mean of 1500.
**Lot 2 Test**<br>
![lot2](/Image/lot2.png) <br><br>
The p value is over the significance level of 0.05 which means that the null hypothesis cannot be rejected and the mean of lot 2 is statistically similar to the population mean of 1500.
**Lot 3 Test**<br>
![lot3](/Image/lot3.png) <br><br>
This time, the p value is under the significance level of 0.05 which means that the null hypothesis can be rejected and the mean of lot 3 is not statistically similar to the population mean of 1500.
## Study Design: MechaCar vs Competition
In this section,comparing MechaCar to its competitor’s other metrics that could be of interest to a consumer,could include cost, car color, city fuel efficiency, highway fuel efficiency, horsepower, maintenance cost, or safety rating.
1) What metric or metrics are you going to test?
- The costs of vehicles will be compared to their fuel efficiency, safety rating, and technology package.
2) What is the null hypothesis or alternative hypothesis?
- The null hypothesis is that the mean of the safety rating is zero.The Alternative Hypothesis is that they are not all the same.
3) What statistical test would you use to test the hypothesis? And why?
- Multiple linear regression would show how the variables impact the safety ratings for MechaCar and their competitors.
A  t-test allows us to test whether a sample mean significantly differs from a hypothesized value.
4) What data is needed to run the statistical test?
- A random sample of n > 30 for MechaCar and their competitor, would need to be collected including the safety ratings, highway fuel efficiency, and horsepower plus running the data through RStudio.

