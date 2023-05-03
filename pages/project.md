---
layout: post
title: My projects
nav: Projects
nav_order: 3
---

# Data Analysis for Credit Score  

### Exploratory Analysis
The data set of Train consists of 21 measurements on 800 individuals. For each individual, credit score (in CreditScore) has been measured, along with the following 20 variables:

status. (“Negative”,“Small”,“Large”,“None”); Duration. History.(“A”,“B”,“C”,“D”); Purpose.(“NewCar”,“UsedCar”,“Other”,“Furniture”,“Television”,“Domestic”,“Repairs”,“Education”,“Training”,“Business”); Amount; Savings(“Low”,“Medium” “Large”,“VeryLarge”,“Unknown”); Employment.(“Unemployed”,“Short”,“Medium”,“Long”,“VeryLong”); Disposable; Personal(“M:DivSepMar”,“F:DivSepMar”,“M:Single”,“F:Single”); OtherParties(“None”,“Coapp”,“Guarantor”); Residence; Property(“House”,“Savings”,“Car”,“None”); Age; Plans(“Bank”,“Stores”,“None”); Housing(“Rent”,“Own”,“RentFree”); Existing; Job(“Unemployed”,“Unskilled”,“Skilled”,“Management:Self”); Dependants; Telephone(“No”,“Yes”); Foreign(“Yes”,“No”);

Status, History, Purpose, Savings, Employment, personal, OtherParties, Property, Plans, Housing, Existing, Job, Dependants, Telephone and Foreign should clearly be treated as categorical variables (factors).  

-----------------------------------------
-----------------------------------------

The following plot shows the pairwise scatter plots of each of the continuous measurement.

 {% include figure.html img="https://sm.ms/image/3IYihqNX4gjfupb" %}  
 
The scatter plots matrix suggests correlation between some of covariates and credit scores. The plot shows that Individuals with higher duration of requested loan(Duration) and higher amount requested in months(Amount) have lower credit scores(CreditScore). The relationship between Credit scores and other covariates is not clear.However, it is still important to note that there exists correlation between some of the potential explanatory variables. For example, duration of requested loan(Duration) increases as the amount requested(Amount) increases. Furthermore, due to the data of disposable, residence, existing, dependants are discrete, the scatter plot can not tell the relationship between them as it is hard to investigate the number of points overlapped.  

-------------------------------------------
-------------------------------------------
We now consider the factor variables  

 {% include figure.html img="https://sm.ms/image/A4PpKMrmf7L81ZX" %} 
 {% include figure.html img="https://sm.ms/image/oBTk4jxbmd5HpnA" %} 
 {% include figure.html img="https://sm.ms/image/9hjXpJcrM8GSx1v" %}   
 
 ---------------------------------------------------------------------
 ----------------------------------------------------------------------
Based on the plots, individuals with the following characteristics seem to have higher credit score: Large amount of balance on current account, loan for business or training, Very Large amount of savings, female, believe in Coapp, other current loan plan for stores, foreign worker. The relationship between History and CreditScore needs particular attention as it shows individual with worse credit history earn higher credit score, which violates the common sense.
