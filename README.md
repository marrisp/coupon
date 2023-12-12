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











