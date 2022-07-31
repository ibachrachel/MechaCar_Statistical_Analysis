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

T-Test of All the Manufacturing Lots:

![All Manufacturing Lots](https://user-images.githubusercontent.com/102566199/182047841-f74411a5-11e6-4f6f-8ff4-6a178f4b55bf.png)

To compare to the calculated T-test, we must assume a population mean of 1500. The mean of the total lot summary is actually 1498.78. As seen by the p-value of 0.06028, we must fail to reject the null hypothesis because the p-value is not below the assumed significance level of 0.05. The mean of the three lots is statistically similar to the presumed population mean of 1500.

![Lot1T-Test](https://user-images.githubusercontent.com/102566199/182047873-b568f5cf-df43-4e10-8f94-d06326b22701.png)

Lot 1 actually does have a true sample mean of 1500, which was the presumed mean. The p-value is exactly 1, which means we fail to reject the null hypothesis. The null hypothesis states that there is no statistical difference between the presumed mean of 1500 and the true sample mean of 1500.

![Lot2T-Test](https://user-images.githubusercontent.com/102566199/182047893-c1b30eb2-1207-4e67-b572-af77bcd74215.png)

Lot 2 has the sample mean value of 1500.02 and a p-value of 0.61; therefore, we fail to reject the null hypothesis in this lot as well. The sample's true mean of 1500.02 and the presumed mean of 1500 are statistically similar. 

![Lot3T-Test](https://user-images.githubusercontent.com/102566199/182047904-aa1d3026-e29d-4d55-8c7a-c89da56ad1d1.png)

Lot 3 was a much different situation when it was observed in the design specifications, so we expect to find something awry in this T-test, as well. The sample mean is 1496.14 with a p-value of 0.04. In this scenario we can reject the null hypothesis due to the p-value being lower than the statistically significance level of 0.05. This means that the sample mean of 1496.14 and the presumed mean of 1500 are statistically different. We now know for sure that something went wrong in the testing, which was demonstrated in the data collected in lot 3. The manufacturing process needs to start removing the coils that are causing this disproportate effect on the data. 

### Study Design: MechaCar vs Competition

To create a statistical study that would help to compare against our competitors, it would be important to focus on a measure that would help to improve upon. I would like to improve the fuel economy of the MechaCar prototypes so that the company can pitch the prototype as a way to combat high gas prices.
 We have already found that the ground clearance the vehicle length had an effect on the dependent variable, so my plan is to improve upon the variables that can be improved. 

- What metric or metrics are you going to test?

Fuel Efficiency: how the vehicle's components affect fuel usage. 

- What is the null hypothesis or alternative hypothesis?

H0, Null Hypothesis: The fuel economy of the MechaCar prototype is not signicantly different that the fuel economy of the equivalent vehicle type of a competitor company.

HA, Alterative Hypothesis: The fuel economy of the MechaCar prototype is significantly different than the fuel economy of the equivalent vehicle type of a competitor company.

- What statistical test would you use to test the hypothesis? And why?

A two-sample T test would be the best test to use in this study design because the distribution between the means from two samples are being analyzed for statistically difference. We are going to be comparing the AutosRUs prototype to the Competitors vehicle.

- What data is needed to run the statistical test?

The data that would be needed to run the statistical test would be the following:

a. Vehicle weight

b. Acceleration/Deceleration Capabilities




