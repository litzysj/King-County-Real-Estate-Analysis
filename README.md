

## [Overview](https://www.canva.com/design/DAFFFvR5qtk/HOLc75dVN8VLML9nRzshQA/edit?utm_content=DAFFFvR5qtk&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)(link to presentation)

Airbnb Musketeers LLC was founded to help aspiring Airbnb owners to purchase a house in order to start up their Airbnb business. Arthur Macintosh, a local businessman, reached out to our company and asked for us to help him purchase a home in King County, Washington. Mr. Macintosh had specified that he wanted his house in King County to have at least 3 bedrooms, and 2 bathrooms, a view, and for it to be under $750,000. The goal of this data analysis is to give Mr.Macintosh recommendations on what houses he should consider with the specifications that he gave us. We used housing data for King County. This dataset contains house sale prices for King County, which includes Seattle. It includes homes sold between May 2014 and May 2015. The data originally consisted of 21,597 houses that were built between 1900 and 2015. We narrowed that number by dropping nulls which brought the data to 15,762 houses. We further narrowed that number by dropping houses that had more than 4 bedrooms in order get rid of outliers which left us with 14,342 houses. After all of those reductions we were left with roughly 2/3 of the data to work with. The methods we used to clean our data and. create our models were train-test-split, OLS models, removing irrelevant data, filtering unwanted outliers, handling missing data. After a deep analysis of our data we came to the conclusion that Mr. Macintosh should purchase a home in the Metro Area with Average/Below Average Square Footage 
 Bedrooms 3, Bathrooms 2 minimum

 ## Business Problem

Mr.Macintosh wants to buy a house so that he can be in the Airbnb business. He is set on the amount of money that he is willing to invest in the purchase of the house. Our predictions are important in order to be able to help Mr.Macintosh to not go over budget. This is not the only house that we are helping him purchase which is why it is important that we find a house with the requirements he set in order for him to be able to price the rental of the home at a rate that generates him the most profit. If he goes over budget that would mean less amount of money that he can spend on the other houses he is also interested on buying outside of King County, Washington.

## Data Understanding

The data that we are using came from the King County Houses database. The data relates to our analysis question because it contains all the data that we need in order to be able to deliver to Mr.Macintosh the types of houses that he should consider buying based on his prerequisites. The main target variable is price. Other variables that we intend to use are price, bedrooms(# of bedrooms in the home), bathrooms(# of bathrooms in the home), sqft_living(Square footage of living space in the home), view(quality of view from house - represented by {"NONE": 1, "FAIR": 2, "AVERAGE": 3, "GOOD": 4, "EXCELLENT": 5}), Area(the distance the home is from Seattle in miles). We cleaned up the data by removing irrelevant data, filtering unwanted outliers, scaling, and handling missing data.

- What variables were kept?

  - price
  - bedrooms
  - bathrooms
  - sqft_living
  - floor
  - zip code
  - view
  
- Were there variables you dropped or created?

  - id
  - date
  - sqft_lot
  - waterfront
  - condition
  - grade
  - sqft_above
  - sqft_basement
  - yr_ renovated
  - lat
  - long
  - sqft_living15
  - sqft_lot15
  
-How did you address missing values or outliers?

  - Dropped null values including question marks
  - Filtered out our data in order to get rid of outliers
  
-Why are these choices appropriate given the data and the business problem?

  - It was appropriate to drop the variables above because they did not have numeric values and would not fit in our model
  - It was also appropriate to filter out data because certain homes had up to around 30 bedrooms and those outliers were skewing our data. Because our end goal was   to find a vacation home for an average family it was irrelevant for us to consider a house with that amount of bedrooms.
  
-How much of the data have we dropped?

  -We narrowed the amount of data that we were working with by dropping nulls which brought the data to 15,762 houses. We further narrowed that number by dropping houses that had more than 5 bedrooms in order get rid of outliers which left us with 14,342 houses. After all of those reductions we were left we dropped 1/3 of the data leaving us with roughly 2/3 of the data to work with.
  
## Modeling

- Describe and justify the process for analyzing or modeling the data.

  - We analyzed the data by looking for variables that better correlated with price. We did this to find what variable(s) affected the overall price of the house.
  - We iterated our initial approach and made it better by taking out certain variables from our data frame that were not useful in solving our business problem. We also removed outliers and null values.
  - These choices were appropriate given our data and business problem because we were able to remove variables that skewed our data and that were not significant to consider when trying to solve our business problem.
  
 ## Interpretation
  - Most of our models explained 45-55% of our variance in price.
  - Bathrooms and Square foot of the house are statistically significant with a p-value of 0.
  - one additional bedroom unit drives down the expected price by about -6.948e+04
  - one additional sqft_living unit drives up the expected price by about 296.
  
  ## Conclusions
  
  - What would you recommend Mr.Macintosh do as a result of this work?
  
      - Purchase a home:
        - In the metro
        - With average or below average square footage
        - With 3 bedrooms or 2 bathrooms minimum
            
    - What are some reasons why your analysis might not fully solve Mr.Macintosh's problem?
   
        - The data that we used does not include the amount of houses that are used for Airbnb. Not knowing this piece of information does not let us know how much competition Mr.Macintosh will have in King County in the Airbnb business.
        - Additionally our analysis does not provide Mr.Macintosh with any useful data that he can use to determine what the nightly rate of his Airbnb house should be.
        - Our analysis does not take the attractions that can be seen from certain homes into consideration. If we could have been able to do that, we could have possibly been able to see if the view from a house had any relationship with how popular it might have been as an Airbnb house.
        
    - What else could you do in the future to improve this project (future work)?
    
        - Analyze specific AirBnB data to determine the amount of competition Mr.Macintosh should expect at King County, Washington
        - Consider the impact of how popular an Airbnb house can be based on the attractions that eithe inside or outside the city
