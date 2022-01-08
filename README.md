# **Family Matters Program**

**Authors:** _Gregory Han, Ferit Yikar, Edel Prado_

<img src="images\title.PNG" width=100%>

## Overview
This project analyzes the King County Housing data to create a recommendation on which homes to buy for financially struggling families. Descriptive analysis of home features, location, and grade show that some zip codes are better suited for buying houses. The King County Housing Authority can use this analysis to better select homes that have 3-4 bedrooms with the least amount of investment.
***
## Business Problem
<img src="images\kc_neighborhood.jpg" width=80%>

King County Housing Authority (KCHA), which provides housing assistance for people with low income in King County, has received a fortune from a generous donor to purchase homes for struggling families. KCHA will be using this donation in their Family Matters Program where families would be given homes that they can manage paying the property taxes. Using the King County Housing data, we describe patterns in house sales price to predict where KCHA should buy homes, what the most important features of a home are regarding price, and how to search for the best fit home.
***
## Data
The King County Housing dataset contains 22,000+ sold homes from the past year (2014-2015). Each record lists their individual home features such as number of bedrooms, square feet of the home, and home location (in latitude and longitude).

***
## Methods
This project uses the U.S Census for 2015 which estimates that the average family size for King County is between 3-4, and the poverty guideline for the U.S. for a said family sizes are $20,090 and $24,250 respectively. We then used the 28/36 rule which is your mortgage payment not being more than 28% of your monthly pre-tax income and 36% of your total debt. Using the rule, we focused all 28% to be paid for perennial property tax which is $9.30 per $1000 in 2015. 
***
## Results

### Relationships of Features and Price
Our first step was to take a look at the relationships with price within the dataset.

<img src="images\heatmap.png" width=80%>


### Model
Based on r^2 and RMSE values, we decided to go with linear comprehensive log model.

<img src="images\visualization_of_all_models.png" width=80%><br>

### Features of a Home
Our next process was to look at the home features and their significance vs price.

Here you can see that grade and square feet living play major roles for determining price
<img src="images\significance_of_features.png" width=80%><br>


### Three Bedroom Home Maps
We used our model and specifications to find the kind of house we need and used a algorithm to determine how much that house would cost in different areas. In this case, we looked for three bedroom homes and visualized it on a map.

The more north you go, the prices of homes start to increase. Where as you go south, houses become much cheaper. 

The zip code map on the top shows the areas of lowest average price of homes (where the darker the colored area, the higher the price)  while the bottom depicts the location of homes and their price (where  the darker the color the cheaper it is). We would recommend buying homes in the lighter areas of the zip code map.

<img src="images\3_bedroom_map.PNG" width=80%>

<img src="images\3_bedroom__home_price_map.PNG" width=80%><br>


### Four Bedroom Home Maps
Here we have our 4 bedroom version which we used our algorithm again to determine how much a house would cost in different zip codes. Note that we have fewer zip codes with cheaper homes compared to 3 bedroom homes

<img src="images\4_bedroom_map.PNG" width=80%>

<img src="images\4_bedroom__home_price_map.PNG" width=80%> <br>


### Linear Regression Model
For each data point, we checked against our model. It looks like our model does a decent job with predicting price!

<img src="images\price_predictions_vs_actual_price.png" width=80%>

***
## Conclusion
This analysis gives us three recommendations for purchasing homes for KCHA's Family Matters Program:
- <u> Where should we buy homes? </u>
    - Buy the most amount of homes, target the lighter areas on the zip code map.
<br><br>

- <u>What feature is most important for prices of homes?</u>
    - Grade and square feet living are the most prominent factors in price
<br><br>
- <u>How to search for the best fit home?</u>
    - Use the Robin Hood Algorithm™  to decide whether a specific house is a good buy compared to the KC area.

***
## Next Steps
Further analyses could result with additional insights to further improve our recommendations:
- <u> Where should we buy homes? </u>
    - School district data
    - Crime rate data
    - Zip code area vs socioeconomic status
<br><br>

- <u>What feature is most important for prices of homes?</u>
    - Additional feature data such as garage, size of rooms, or if the home is furnished or not
<br><br>
- <u>How to search for the best fit home?</u>
    - More engineering to streamline the input process

***
## For More Information
Please review our full analysis in our [Jupyter Notebook](./King_House_Sales.ipynb) or our [presentation]().

For any additional questions, please contact

<img src="images\greg.png" width=10%> Gregory Han: gregoryhhan@gmail.com <br />

<img src="images\ferit.png" width=10%> Ferit Yikar: yikarferit@gmail.com <br />

<img src="images\eddie.png" width=10%> Edel Prado: edel.prado.jr@gmail.com <br />


## Repository Structure

```
├── README.md                           
├── King_House_Sales.ipynb   
├── Presentation.pdf 
├── notebooks  
├── data                                
└── images 
```
