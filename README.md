# MechaCar Statistical Analysis

## Overview of Analysis

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on the data analytics team to review the production data for insights that may help the manufacturing team.

The data analytics team will do the following:

* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis write a summary interpretation of the findings.

## Linear Regression to Predict MPG

<img width="818" alt="Screenshot (275)" src="https://user-images.githubusercontent.com/102890151/178132929-0df105f5-4588-4fd4-9980-2c8d888bff61.png">
above, statistical summary of the linear regression model using multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance

### Summary of Linear Regression to Predict MPG with Three Questions Addressed
 
* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

 PR(.|t|) value in the summary (image above, and below) represent the proability that each coefficient contributes a ramdom amount of variance to the linear model. 
 
<img width="426" alt="Screenshot (280)" src="https://user-images.githubusercontent.com/102890151/178148399-adc3b0aa-eda0-4e6d-aff4-5bba87e47635.png">

Looking at the individual Pr(>|t|) values, the variables that were less than 0.05 were for the intercept, vehicle length and ground clearance. This means that the intercept, vehicle length and ground clearance are statistically unlikely to provide random amounts of variance to the linear model.In other words, vehicle length and ground clearance do have a significant impact on miles per gallon (mpg). Additionally, with the intercept being significant which tells us there is a significant amount of variability in the dependent variable when all independent variables are equal to zero, we may need to scale or transform the data.


* Is the slope of the linear model considered to be zero? Why or why not?

Using a significance level of 0.05, we can reject the null hypothesis because our p-value 5.35e-11 (0.0000000000535) is < 0.05. In a typical linear regression, the null hypothesis states that slope is equal to 0. However, if the null hypothesis is rejected, as in the case here the slope is not 0.


* Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

Based on the calculations, this linear model does predict mpg of MechaCar prototypes adequately. The r-squared value showed a strong correlation ( 0.71) and p-value showed significance. 


## Summary Statistics on Suspension Coils

![Screenshot (370)](https://user-images.githubusercontent.com/102890151/178150933-d5e49690-4c75-4364-9b38-e95ed391a74c.png)

Above image. Summary of statistics on suspension coils at MechaCar. Below image. Stats summary of each manufacturing lot at MechaCar

<img width="439" alt="Screenshot (271)" src="https://user-images.githubusercontent.com/102890151/178132486-d91482f1-2533-429c-bce5-3d63c384b929.png">


### Summary Statistics on Suspension Coils

* The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

With the information from the summaries we can see that, as a total, the lots do not exceed 100 PSI (average variance). However, if we look at the manufacturing lots individually we see lots 1 and 2 are within the limits, but lot 3 exceeds the 100 PSI variance limit.


## T-Test on Suspension Coils

<img width="437" alt="Screenshot (274)" src="https://user-images.githubusercontent.com/102890151/178132456-3aaee353-64ae-4a0e-b374-c1c5f3c9e6a7.png">

<img width="492" alt="Screenshot (273)" src="https://user-images.githubusercontent.com/102890151/178132451-3c817e77-b8df-476f-81a5-0a3d3275b61f.png">

Above results of t-tests. First result, all lots followed by results from Lot 1, Lot 2 and Lot 3.


### Summary T-Test on Suspension Coils

Conducting t-test to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch and then conducting t-tests for each manufacturing lot.

#### All Lots (1,2,3)

The first t-test was used to determine if the PSI across all manufacturing lots is statistically different from the population mean (1500 psi). The result of the t-test showed that there was a sample mean of 1,498.78 and a p-value of 0.06. Because our p-value is higher than the assumed statistical significance of 0.05, we fail to reject the null hypothesis. This means that the PSI across all manufacturing lots is statistically similar to the population mean.

#### Lot 1

Lot 1's Sample mean is 1,500 and the p-value is a perfect 1. There is no statistical difference from the population mean. In this case, we fail to reject the null hypothesis.

#### Lot 2

We cannot reject the null hypothesis using a standard significance level of 0.05 because P-Value is 0.6072.

#### Lot 3

We can reject the null hypothesis using a standard significance level of 0.05 because our P-Value is 0.04168. Note that Lot 3 also has the smallest sample mean of the three lots at 1496.14.

## Study Design: MechaCar vs Competition

#### Study: How much of impact does color of vehicle have on its resale value? MechaCar vs Competition

##### A few questions that could be asked

Are wild colors ok? Do sports cars with bland colors have the same resale as brighter colors? Do the more popular, subdued, traditional colors garner a higher resale value? Is the pool smaller for brighter colors, and hence maybe less resale value? 

* What metric or metrics are you going to test? 

Measured metrics would be value of vehicle when sold, class of vehicle, color of vehicle along with other standard metrics that effect resale (condition of vehicle, miles, accident or no accident etc etc. Given two vehicles are equal, but different colors, is there a difference in price?

What is the null hypothesis or alternative hypothesis? 

The null hypothesis would be there is no relationship between the color of vehicle and resale price. The alternative hypothesis would be that there is a relationship between color and resale price of a vehicle.

* What statistical test would you use to test the hypothesis? And why? 

Since we are using both numerical and categorical data, One-Way ANOVA or Independent t test.

* What data is needed to run the statistical test? 

In order to run this test we would need the price of vehicle when resold, class of vehicle, color of vehicle along with other standard metrics that effect resale (condition of vehicle, miles, accident or no accident etc etc. Also needed is same info for competitors.
