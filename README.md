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

## T-Tests on Suspension Coils
![lot_all](/Image/lot_all.png) <br><br>

![lot1](/Image/lot1.png) <br><br>

![lot2](/Image/lot2.png) <br><br>

![lot3](/Image/lot3.png) <br><br>

## Study Design: MechaCar vs Competition

