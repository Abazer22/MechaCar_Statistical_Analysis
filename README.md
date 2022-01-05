# MechaCar_Statistical_Analysis
## Overview of Project
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help Jeremy and the data analytics team do the following:

Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
Run t-tests to determine if the manufacturing lots are statistically different from the mean population
Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Deliverable 1:
### Linear Regression to Predict MPG

![liner2](https://user-images.githubusercontent.com/90945875/148150479-2f353d15-f13b-4379-a433-961f72552449.PNG)

From the above output we can see that:

1.This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, his multiple regression model does predict mpg of MechaCar prototypes effectively.

2.The vehicle length, and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the model. That is to say, the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype. Conversely, the vehicle weight, spoiler angle, and All Wheel Drive (AWD) have p-Values that indicate a random amount of variance with the dataset.

3.The p-Value for this model, p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further indcates that the slope of this linear model is not zero.

## Deliverable 2:
###  Summary Statistics on Suspension Coils
total_summary dataframe:

![total_summary](https://user-images.githubusercontent.com/90945875/148154521-f5bb575e-4e8c-4f64-bf15-384ee350bfd1.PNG)

lot_summary dataframe

![lot_summary](https://user-images.githubusercontent.com/90945875/148154904-93b1b1f8-35d5-44b4-8113-a8172d343c8a.PNG)

When looking at the entire population of the production lot, the variance of the coils is 62.29 PSI, which is well within the 100 PSI variance requirement.

Similarly, but significantly more consistent, Lot 1 and Lot 2 are well within the 100 PSI variance requirement; with variances of 0.98 and 7.47 respectively. However, it is Lot 3 that is showing much larger variance in performance and consistency, with a variance of 170.29. It is Lot 3 that is disproportionately causing the variance at the full lot level.

## Deliverable 3:
### t-Tests on Suspension Coils

A summary of the t-test results across all manufacturing lots

![the whole](https://user-images.githubusercontent.com/90945875/148156514-ee0f1c86-e5e4-4b38-8508-0aefa71ec0c2.PNG)

From here we can see the true mean of the sample is 1498.78, which we also saw in the summary statistics above. With a p-Value of 0.06, which is higher than the common significance level of 0.05, there is NOT enough evidence to support rejecting the null hypothesis. That is to say, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500.

A summary of the t-test results across lot1

![lot1](https://user-images.githubusercontent.com/90945875/148156864-1e321694-5e0b-4310-96e3-94b7814ccc66.PNG)

Lot 1 sample actually has the true sample mean of 1500, again as we saw in the summary statistics above. With a p-Value of 1, clearly we cannot reject (i.e. accept) the null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean (1500).

A summary of the t-test results across lot2

![lot2](https://user-images.githubusercontent.com/90945875/148157194-e816eb53-7c2e-448e-8cbb-d233008b40e7.PNG)

Lot 2 has essentially the same outcome with a sample mean of 1500.02, a p-Value of 0.61; the null hypothesis cannot be rejected, and the sample mean and the population mean of 1500 are statistically similar.

A summary of the t-test results across lot3

![lot3](https://user-images.githubusercontent.com/90945875/148157368-499caf4f-18c3-49e6-b35a-4e9f76eaf818.PNG)

Lot 3, not surprisingly is a different scenario. Here the sample mean is 1496.14 and the p-Value is 0.04, which is lower than the common significance level of 0.05. All indicating to reject the null hypothesis that this sample mean and the presumed population mean are not statistically different.

