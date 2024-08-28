# Calculation for diversity_index

To calculate the Simpson's Diversity Index for 2024 we follow these steps:

**1. Identify the Proportions for 2024:**
Black: 0 individuals
Hispanic: 0 individuals
White: 100 individuals
Total individuals: 0+0+100=1000 + 0 + 100 = 1000+0+100=100

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
D=1−∑(Proportion2)
D = 1 - 1 =0

**Result:**
The diversity index for 2024 is 0 because all the individuals belong to a single ethnic group, resulting in no diversity. This formula reflects that when there is only one group present (no diversity), the index is 0. 

**Deploy**
With this understanding in mind we can add an Diversity Index Col with the Simpson's diversity index formula that takes into account 2 elements of diversity- richness and evenness. Richness is the number of ethnic groups and evenness is the ethnic group spread.  The more ethic group present in a sample the richer the data. High Ethnic diversity index close to 1 indicates high diversity. Low ethnic diversity index close to 0 indicates low diversity 
