## Overview of Project
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

In this challenge, you’ll help Jeremy and the data analytics team do the following:

* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Deliverables:
This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:

1. ***Deliverable 1:*** Linear Regression to Predict MPG
2. ***Deliverable 2:*** Summary Statistics on Suspension Coils
3. ***Deliverable 3:*** T-Test on Suspension Coils
4. ***Deliverable 4:*** Design a Study Comparing the MechaCar to the Competition

# Deliverable 1:  
## Linear Regression to Predict MPG
### Deliverable Requirements:

The `MechaCar_mpg.csv` dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. Using your knowledge of R, you’ll design a linear model that predicts the mpg of MechaCar prototypes using several variables from the `MechaCar_mpg.csv file`. 


#### Results on Deliverable:
	
![d1](https://github.com/ZZaman1989/MechaCar_Statistical_Analysis/blob/main/Resources/Images/Deliverable%201.png)

From the above output we can see that:

1. The **vehicle length**, and **vehicle ground clearance** are statistically likely to provide non-random amounts of variance to the model.

2. The p-Value for this model, ```p-Value: 5.35e-11```, is much smaller than the assumed significance level of 0.05%. This indcates that the slope of this linear model is **not zero**.

3.  This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. This model **does predict mpg of MechaCar prototypes effectively**. 

# Deliverable 2:  
## Summary Statistics on Suspension Coils
### Deliverable Requirements:

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. Using your knowledge of R, you’ll create a summary statistics table to show:

- The suspension coil’s PSI continuous variable across all manufacturing lots
- The following PSI metrics for each lot: mean, median, variance, and standard deviation.

Your `total_summary` dataframe should look like this:

![d1](https://github.com/ZZaman1989/MechaCar_Statistical_Analysis/blob/main/Resources/Images/Deliverable%202%20-%20Total%20Summary.png)

Your lot_summary dataframe should look like this:

![d1](https://github.com/ZZaman1989/MechaCar_Statistical_Analysis/blob/main/Resources/Images/Deliverable%202%20-%20Lot%20Summary.png)

Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

When looking at the entire population of the production lot, the variance of the coils is 62.29 PSI, which is within the 100 PSI variance requirement.  

Lot 1 and Lot 2 are within the 100 PSI variance requirement (0.98 and 7.47).  However, Lot 3 is showing a variance in performance and consistency(170.29).   

# Deliverable 3:  
## T-Tests on Suspension Coils
### Deliverable Requirements:

Using your knowledge of R, perform t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

There is a summary of the t-test results across **all manufacturing lots**
![d3](https://github.com/ZZaman1989/MechaCar_Statistical_Analysis/blob/main/Resources/Images/Deliverable%203%20-%20T-Test%20All%20Lots.png)

We can see the **true mean of the sample is 1498.78**.  With a **p-Value of 0.06**, which is higher than the common significance level of 0.05, there is **NOT enough evidence to support rejecting the null hypothesis**.  

**Next looking at each individual lots:**
![d3](https://github.com/ZZaman1989/MechaCar_Statistical_Analysis/blob/main/Resources/Images/Deliverable%203%20-%20T-Test%20Lot%201.png)
1. Lot 1 has **p-Value of 1**, we cannot reject the null hypothesis.

![d3](https://github.com/ZZaman1989/MechaCar_Statistical_Analysis/blob/main/Resources/Images/Deliverable%203%20-%20T-Test%20Lot%202.png)
2. Lot 2 has a **p-Value of 0.61**, we cannot reject the null hypothesis.

![d3](https://github.com/ZZaman1989/MechaCar_Statistical_Analysis/blob/main/Resources/Images/Deliverable%203%20-%20T-Test%20Lot%203.png)
3.  Lot 3 has a **p-Value is 0.04**, which is lower than the common significance level of 0.05. We can **reject the null hypothesis**.


# Deliverable 4:  
## Study Design: MechaCar vs Competition
### Deliverable Requirements:

Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

The statistical study design has the following:
- A metric to be tested is mentioned
- A null hypothesis or an alternative hypothesis is described
- A statistical test is described to test the hypothesis

#### Metrics
*  Safety Feature Rating
*  Current Price (Selling)
*  Resale Value
*  Average Annual Cost of ownership (Maintenance)
*  MPG (Gasoline Efficiency)


#### Hypothesis: Null and Alternative
 * Null Hypothesis (Ho): Car is priced correctly based on its performance of key factors for its genre.
 * Alternative Hypothesis (Ha): Car is NOT priced correctly based on performance of key factors for its genre.
 
#### Statistical Tests
A **multiple linear regression** would be used to determine the factors.

#### Data Needed
* Competitions' comparable models. 
* Cars will MechaCar be competing with head-to-head? which cars will be included in the study.
* Relevant to selling price.