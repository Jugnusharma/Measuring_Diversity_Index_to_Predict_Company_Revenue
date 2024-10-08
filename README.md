# Calculation for Diversity Index and Predictions based on the Index

This resource covrers 3 things: 

•	How to Measure Diversity Index

•	Create a Regression model to predict a metric (in this case the revenue, in most HR use cases it is the turnover) 

•	Based on the model understand how increase or decrease in Diversity index effects a metric in this case the revenue



Simpson's indices are a way of quantifying the biodiversity of communities. The value of Simpson's index reflects how many different types of species are in a community and how evenly distributed the population of each species is. We can use this same logic in an HR setting in order to understand the diversity and the impact that it has on other variables. In this example below the effect that the index has on revenue. 

**Dataset**
Black: 0 individuals
Hispanic: 0 individuals
White: 100 individuals
Total individuals: 0+0+100=100


To calculate the Simpson's Diversity Index for 2024 we follow these steps. Note for simplicity sake I have used a total on 100 individuals, in real world the totals would be different and the proportions but would calculated  based on %:

**1. Identify the Proportions for 2024:**
Black: 0 individuals
Hispanic: 0 individuals
White: 100 individuals
Total individuals: 0+0+100=100

**2. Calculate the Proportions for Each Group:**
Proportion of Black=0/100=0 
Proportion of Hispanic=0/100=0 
Proportion of White=100/100=1

**3. Square the Proportions:**
(0)^2 = 0
(0)^2 = 0
(1)^2 = 1

**4. Sum the Squared Proportions:**
Sum of squared proportions = 0 + 0 + 1 = 1

**5. Apply Simpson's Diversity Index Formula:**
Simpson's Diversity Index is calculated as:
D=1−∑(Proportion^2)
D = 1 - (1) =0

**Result:**
The diversity index for 2024 is 0 because all the individuals belong to a single ethnic group, resulting in no diversity. This formula reflects that when there is only one group present (no diversity), the index is 0. 

**Deploy**
With this understanding in mind we can add an Diversity Index Col with the Simpson's diversity index formula that takes into account 2 elements of diversity- richness and evenness. Richness is the number of ethnic groups and evenness is the ethnic group spread.  The more ethic group present in a sample the richer the data. High Ethnic diversity index close to 1 indicates high diversity. Low ethnic diversity index close to 0 indicates low diversity 

**Create Regression Model (Fig1):**

Data Preparation: The data is first organized into a pandas DataFrame.

Simpson's Diversity Index Calculation: A function is used to calculate the Simpson's Diversity Index, which is then applied to each row in the DataFrame.

Linear Regression: The model is trained using Advertising Expense, Inclusive Score, and Ethnic Diversity Index as predictors and Revenue as the target.

![image](https://github.com/user-attachments/assets/3181e864-0882-4e99-a813-43dc3ed7f106)

**Scenario 1** - Fig 2
To predict the increase in revenue for every 1% increase in the ethnic diversity index is based on the coefficient of the ethnic diversity index from the regression model. Our dataset now has added/other variables 

Here's how it works:

**Given:**
The coefficient for the ethnic diversity index (EEE) from the regression model is approximately 868.979 (Fig 2)

**Ethnic Diversity Index Coefficient:**
This coefficient indicates the change in revenue for a unit change (which in this case is 1.0 or 100%) in the ethnic diversity index.

**Calculate the impact of a 1% change:**
Since 1% increase corresponds to 0.01 (because 1%=0.01on the scale used in the model), we multiply the coefficient by 0.01:
E = 868.979 X 0.01 = 8.68979

Thus, for **every 1% increase in the ethnic diversity index**, **the revenue is predicted to increase by approximately $8.69.**

*****************************************************************************************************
**Scenario 2** - - Fig 3
Predict the revenue based on the linear regression model 

**Given:**
The coefficient for the ethnic diversity index (EEE) from the regression model is approximately 868.979 (Fig 3)

**Predict revenue**
If given Advertising Expense = 80, Inclusive Score = 80, and Ethnic Diversity Index = 0.8 

