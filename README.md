# coupon

This repository is structured into 3 folders
1. data
2. images
3. ipynb code file

Coupons Analysis:

This exercise aims to extract, cleanse, and analyze various factors to highlight the differences between the drivers/customers who accepted Vs not accepting the coupons, determining the acceptance rate.

As part of the first step, we validated the data file coupons.csv to observe if there is any data we need to remove from the dataset that may impact the analysis and found that a few rows need to be removed.

1. Removed the rows where destination == 'Work and occupation = 'Unemployed
2. Convert Column Y values to a lookup with more meaningful information such as 1 --> Accepted, 0--> Rejected
3. Convert the age column to various groups
    a. Below 25
    b. Above 25

4. Values in Bar and CoffeeHouse are categorized to
    a. Never Visited
    b. 1-3 Visits
    c. More Than 3 Visits

After cleansing the data, the next step is determining each coupon's acceptance rate.

A bar plot using Plotly was created to observe the acceptance rates, indicating which coupon has the highest and lowest.
Refer to the file 'images/AcceptanceProportion.png'

Also, another bar graph using Plotly was created to show the comparison of acceptance and rejection rates for each coupon
Refer to the file 'images/AcceptanceRejection.png'

A histogram using Seaborn is created to show the temperature data
Refer to the file 'images/Temperature.png'

**Investigating the Bar Coupons**

Analyzed the data for Bar coupon explicitly to know the acceptance rate and it lead to 44%

The next steps was to perform comparison  of the acceptance rate between different combinations for Bar coupon

1. Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more.

 A bar plot using matplotlib created to show the comparison
 Refer to the file 'images/AcceptanceRateVisits.png'

 The acceptance rate for 1-3 visits category was the highest and variance between the 1-3 Vists Vs more than 3 visits was 5.33 %

2. Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to all others. Is 
   Is there a difference?

   After analyzing the data, arrived at the below conclusion

   **Total Drivers visiting Bar are  1295
   Drivers Above 25 and visiting more than once a month are  198
   Drivers of all ages excluding Above 25 years of age visiting Bar are  96
   Acceptance rate for driver above 25 years of age is 16 percent
   Acceptance rate for all others drivers excluding above 25 years of age is 8 percent
   Yes, there is a difference of 8 percent between 25 years above age Vs all others**

3. Use the same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers who were not a kid and had occupations other than farming, fishing, or forestry.

   **Total Drivers having passangers with no kids and occupation is not Farming Fishing, or Forestry are  254
     Acceptance rate for the drivers with passengers other than kids, visiting bar visiting more than once a month is 20 percent.
     Total Drivers having passangers with kids, visiting bar less than once in a month and occupation is Farming Fishing, or Forestry are      1
     Acceptance rate for the drivers with passengers other than kids, visiting bar visiting more than once a month is 20 percent.
     Acceptance rate for the drivers with passengers with kids, visiting bar visiting less than once a month is 1 percent.
    The variance between the two acceptance rate is 19 percent.**


4. Compare the acceptance rates between those drivers who:
     go to bars more than once a month, had passengers that were not a kid, and were not widowed OR
      **Total Drivers having passengers with no kids, visited bar more than once a month, and not widowed  254
      Acceptance rate for the drivers with passengers other than kids visiting bar more than once a month is  19.613899613899612**

      go to bars more than once a month and are under the age of 30 OR

      **Total Drivers who visited bar more than once a month and under age of 30 are  202
      Acceptance rate for the drivers with passengers under age 30 visiting bar more than once a month is 26 percent.**

      go to cheap restaurants more than 4 times a month and income is less than 50K.

      **Total visits to cheap restaurants is  1261
        Total Drivers visited cheap restaurant more than 4times  a month, and income less than 50k is  209
        Acceptance rate for the drivers with income less than 50k and visiting more than 4times a month 16.57414750198255 percent.**


  #1. Drivers who had visits 1-3 times a month are 13%
  #2. Drivers who had visits more than 3 times a month is 7.85%
  #3. Drivers above 25 years of age is 16%
  #4. All others drivers excluding above 25 years of age is 8%
  #5. Drivers with passengers other than kids, visiting bar visiting more than once a month is 20%.
  #6. Drivers with passengers with kids, visiting bar visiting less than once a month is 1%.
  #7. Drivers with passengers other than kids, visiting bar more than once a month is  19.61%
  #8. Drivers with passengers under age 30 visiting bar more than once a month is 26%.
  #9. Drivers with income less than 50k and visiting more than four times a month 16.57%.
      
Based on the all the above observations, it indicates that the drivers/customers under the age group of 30 have a higher rate of acceptance based on the number of visits they have made to the Bar who do not have kids as the passengers

Also, it is interesting to see that the Drivers with incomes less than 50k tend to visit more number of times to a bar in a month









