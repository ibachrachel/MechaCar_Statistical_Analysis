# Module 15 Challenge

## Overview: 

*Background*

Jeremy is the primary analytic for AutosRUs and has been with the company for 10 years. The company's decision making process needs to be upgraded into the 21st century. Data analytics needs to be included when studying design for future product testing, study design, and other analysis for the manufacturing process. Jeremy and the rest of the Analytics team are using the statiscal language of R to work with summary statistics, visualization, and interpretations of test results. Critical thinking will definitely help the manufactuing process improve. 

*Purpose*

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

The following tasks will help the manufacting team make a decison going forward: 

- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.


## Deliverables

*Linear Regression to Predict MPG*

![Summary of Linear Regression Model](https://user-images.githubusercontent.com/102566199/182046100-3dc2d387-784f-4df4-91be-9714ddedf2c1.png)

### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

The vehicle ground clearance and the vehicle length both provided a non-random amount of variance to the MPG values within the data. They both are statistically likely to have a significant effect on the MPG on the MechaCar. 

The rest of the variables (vehile weight, spoiler angle, and all wheel drive) are not indicated as providing a non-random amount of variance to the MPG values. This means that they are not going to signficantly alter the MPG.

### Is the slope of the linear model considered to be zero? Why or why not?

The slope of the linear model is considered to be NOT zero because the p-value that was calculated was 5.35e-11. This is important because the p-value is compared to a set significance level of 0.05%. The resulting p-value was much lower than the assumed significance level, which allows the rejection of the null hypothesis. The null hypothesis was that there was no effect by any of the factors influencing the dependent variable, so once this is rejected, it can be claimed that the slope of linear model is not zero because there was an effect on the dependent variable. 

### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The linear model does predict the MPG of the MechaCar prototypes effectively because the linear model has an r-squared value oc 0.7149. This is equivalent to 71.5% of all the MPG predictions can be determined using the created model. 

*Create Visualizations for the Trip Analysis*

### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

![Lot Summary](https://user-images.githubusercontent.com/102566199/182047471-b0972680-6599-4eae-8f71-62c399a8e164.png)

![Total Summary](https://user-images.githubusercontent.com/102566199/182047477-ddbd960d-ea52-45f5-8bf9-ea37f1d9d86f.png)

The total summary of all the lots shows a variance of 62.29 PSI, which meets the design specifications that dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. 

The lot summary that is broken up between 1, 2, and 3 offers a bit more insight into the data though. Lot 1 and 2 are both within the 100 PSI design specification because they both have variances of 0.98 and 7.47, respectively. Lot 3 is a very different though, with a variance of 170. This means that lot 3 is having a huge effect on the total lot summary. 

### T-Tests on Suspension Coils
