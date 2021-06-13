# MechaCar_Statistical_Analysis

## Overview of Project
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help Jeremy and the data analytics team do the following:

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.


## Deliverables:
This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:

- Deliverable 1: Linear Regression to Predict MPG
- Deliverable 2: Summary Statistics on Suspension Coils
- Deliverable 3: T-Test on Suspension Coils
- Deliverable 4: Design a Study Comparing the MechaCar to the Competition

## Deliverable 1: Linear Regression to Predict MPG

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using your knowledge of R, you’ll design a linear model that predicts the mpg of MechaCar prototypes using several variables from the file.

### Results:
mpg = (6.267)vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0). Statistical summary can be seen here ![here](https://github.com/MuddassirR/MechaCar_Statistical_Analysis/blob/main/d1-LinearReg.png). From the statistical summary, we see that ground clearance and vehicle length are likely to provide non-random amounts of variance. Furthermore, because the p-value is 5.35e-11 is less than the signficance level of 0.005%, this indicates that the slope of the model is not zero. Finally, since the r-squared value is 0.7149, the variables included account for 71.5% of impact on mpg, which shows that the variables chosen were correct to be included. 

## Deliverable 2: Summary Statistics on Suspension Coils
The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. Using your knowledge of R, you’ll create a summary statistics table to show:

- The suspension coil’s PSI continuous variable across all manufacturing lots
- The following PSI metrics for each lot: mean, median, variance, and standard deviation.

### Results: 
- ![Summary statistics for all manufacturing lots](https://github.com/MuddassirR/MechaCar_Statistical_Analysis/blob/main/total_lot_summary.png).
- ![Summary statistics for each manufacturing lot](https://github.com/MuddassirR/MechaCar_Statistical_Analysis/blob/main/manufactoring_lot_summary.png).
- When looking at the entire population of the production lot, the variance of the coils is 62.29 PSI.
- Lot 3 has much larger variance, Thus, Lot 3 is disproportionately causing the variance at the full lot level. This boxplot shows the differences between the lots: ![boxplot](https://github.com/MuddassirR/MechaCar_Statistical_Analysis/blob/main/boxplot2.png).

## Deliverable 3: t-Tests on Suspension Coils

Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

### Results

Using population mean of 1500, here is a summary of the t-tests across all manufacturing jobs: ![t-test summary](https://github.com/MuddassirR/MechaCar_Statistical_Analysis/blob/main/t_test_all.png). True mean of the sample is 1498.78 and p-value is 0.006, hence, we cannot reject null hypothesis meaning that all 3 lots are statistically similar to the population mean of 1500. However, looking into each lot, we see that lot 1 has sample mean of 1500 and p-value above 1, lot 2 has sample mean of 1500.02 with p-value of 0.61, and lot 3 has sample mean of 1496.14 and p-value of 0.04. This implies that we cannot reject null hypothesis for lot 1 and 2 that there is no statistical difference between the sample and population mean, but we can reject the null hypothesis for lot 3 as there is a statistically significant difference. This can be seen by the image below ![t-tests by lots](https://github.com/MuddassirR/MechaCar_Statistical_Analysis/blob/main/t_test_lots123.png). 

This implies that lot 3's production cycle has issues and needs to  checked. Suspension coils should be checked for quality control. 


