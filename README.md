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
above, statistical summary of the linear regression model

### Summary of Linear Regression to Predict MPG. 3 Questions addressed
 
* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

 PR(.|t|) value in the summary (image above, and below) represent the proability that each coefficient contributes a ramdom amount of variance to the linear model. 
 
<img width="426" alt="Screenshot (280)" src="https://user-images.githubusercontent.com/102890151/178148399-adc3b0aa-eda0-4e6d-aff4-5bba87e47635.png">

Looking at the individual Pr(>|t|) values, the variables that were less than 0.05 were for the intercept, vehicle length and ground clearance. This means that the intercept, vehicle length and ground clearance are statistically unlikely to provide random amounts of variance to the linear model.In other words, vehicle length and ground clearance do have a significant impact on miles per gallon (mpg). Additionally, with the intercept being significant which tells us there is a significant amount of variability in the dependent variable when all independent variables are equal to zero, we may need to scale or transform the data.


* Is the slope of the linear model considered to be zero? Why or why not?

Using a significance level of 0.05, we can reject the null hypothesis because our p-value 5.35e-11 (0.0000000000535) is > 0.05. In a typical linear regression, the null hypothesis states that slope is equal to 0. However, if the null hypothesis is rejected, as in the case here the slope is not 0.



* Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

Based on the calculations, this linear model does predict mpg of MechaCar prototypes adequately. The r-squared value showed a strong correlation ( 0.71) and p-value showed significance. 


## Summary Statistics on Suspension Coils


<img width="439" alt="Screenshot (271)" src="https://user-images.githubusercontent.com/102890151/178132486-d91482f1-2533-429c-bce5-3d63c384b929.png">

### Summary

* The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

## T-Test on Suspension Coils

<img width="437" alt="Screenshot (274)" src="https://user-images.githubusercontent.com/102890151/178132456-3aaee353-64ae-4a0e-b374-c1c5f3c9e6a7.png">

<img width="492" alt="Screenshot (273)" src="https://user-images.githubusercontent.com/102890151/178132451-3c817e77-b8df-476f-81a5-0a3d3275b61f.png">


### Summary


## Design a Study Comparing the MechaCar to the Competition. Study Design: MechaCar vs Competition

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
In your description, address the following questions:
What metric or metrics are you going to test?
What is the null hypothesis or alternative hypothesis?
What statistical test would you use to test the hypothesis? And why?
What data is needed to run the statistical test?
