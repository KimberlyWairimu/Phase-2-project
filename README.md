# The Impact of Location and Property Characteristics on House Sale Prices : An Inferential Analysis

## Introduction

Real Estate agencies are business organizations that generally represent either the buyer or the seller in terms of home transactions, and work as a collective group of lincensed agents and/or brokers who operate a given geographical area. Real Estate agents are hired to market and sell properties on behalf of home sellers. They vet potential buyers, lead viewings, and help negotiate final selling price. They usually work to a base annual salary and may earn commision for house sales.

Agents who work for the seller, also known as listing agents, advise clients on how to price the property and prepare for a sale, including providing tips on last-minute improvements that can help boost the price or encourage speedy offers. Seller agents market the property through listing services, networking and advertisements. On the other hand, agents who work for the buyers search for available properties that match the buyer's price range and wish list.These agents often look at past sales data on comparable properties to help prospective buyers come up with a fair bid. 

Generally , real estate agencies act as intermidiaries between property buyers, sellers, landlords and tenants. They represent their clients' interests and work to achieve their goals in real estate transactions. This representation may involve marketing properties, identifying potential buyers or tenants, negotiating deals and handling paperwork.

This project aims to use linear regression to analyze the relationship between the location, the house characteristics and its sale price by developing a model that takes into account intrinsic characteristics of a property such as number of bedrooms , number of bathrooms , square footage of living space , level of craftmanship used to build the house, square footage of the lot and extrinsic factors such as the location of the property. By analyzing this factors, the model will be able to provide guidance to Azizi Realtors real estate agency when it comes to advising their clientel on property valuations. This approach offers a more scientific approach to real estate valuations compared to the traditional approaches that can lean towards the qualitative side. This analysis will provide valuable insights to the clientel of Azizi Realtors real estate agency helping them make informed decisions which in turn will benefit the agency by providing valuable service to their clients.


## Problem Statement
Azizi Realtors are a real estate agency that want to provide effective advice to their clientel on how the location and house characteristics may increase the estimated value of a house. For the agency to do this effectively, they need a deep understanding on the factors that influence property values. Our goal is to develop a linear regression model that uses data on past properties to accurately capture the relationship between a house's location, characteristics and sale price. This model can provide valuable insights for the analysis, allowing us to estimate how sale price changes as the independent variables change. By providing Azizi Realtors with this information, they can effectively advice their clients when it comes to buying, selling and investing in properties. By doing so we aim to increase the business value of the agency enabling them provide accurate and informed advice to their clientel , leading to increased customer flow, satisfaction and loyalty.


## The main objective
To develop a multiple linear regression model that can establish a relationship between a house's location and characteristics and their impact on the house prices inorder to help Azizi Realtors accurately advice their clientel.


## The specific objectives
- Analyzing data to identify the most important factors that affect house prices
- Building a linear regression model that evaluates a house's price and how it is impacted by location and house characteristics.
- Evaluating the models statistical significance  and coefficients to come up with interpretable results that can help the agency come up with comprehensive advice.


## Modelling
The project has four models. The first model was the baseline model which provides a point of comparison for evaluating the performance of the other models. By comparing the performance of a more complex model to the baseline model, you can determine whether the additional complexity of the model is justified by an improvement in performance.

The second model was fit with all the all the eight independent variables including the three categorical variables namely view , waterfront and grade being one hot encoded and dropping the first columns as a reference.The model was statistically significant explaining about 55% of the variance in price.

After the first model was fitted we then checked for the assumptions of linear regression with the first being multicolinearity.The variable bathrooms had a considerably high correlation with sqft_living and hence we dropped the variable to curb this issue. We then checked for linearity and realized that the variable bedrooms did not assume linearity hence we log transformed it to improve the linearity of the relationship between the independent variable and the house price in the regression model.

We then fitted the third regression model which did better than the second since it explained about 56% of the variance in house price. With the model and all the coefficients being statistically significant.We then checked for the normality of the residuals and realized that the residuals dis not assume normality. To resolve this problem we log tranformed the dependent variable price.We then fitted the final model and realized that the rsiduals now assumed normality but the R-squared was significantly lower than the previous models. The final model explained about 52% of the variance in price with the model being statistically significant and all the coefficients except view_GOOD and grade_12 Luxury being statististically significant.


## Regression Results
The final model's R-squared is 0.52 .this indicates that approximately 52% of the variation in the dependent variable price can be explained by the independent variables in the model. The F-statistic is 1254, with a p-value of 0.00, indicating that the overall model is statistically significant. All the coefficients of te model are statistically significant except view_GOOD and grade_12 Luxury. The dependent variable price has been log transformed to improve the normality of the residuals and hence stabilize the variance of the residuals.

The model has seven idependent variables four being numerical and three being catergorical.One of the numerical coefficients bedrooms has been log transformed to improve the linearity of the variable.The other three sqft_living , sqft_lot and floors have been standardized to help yield a more interpretable intercept.

- The constant is 13.2366 meaning that for a house with an average number sqft_living , sqft_lot and floors and all the other variables being zero, the expected value of the log of the dependent variable is 13.2366. To obtain the expected value of the dependent variable itself, you can take the exponential of the intercept: exp(13.2366) = 559,407.
- The coefficient of sqft_living is 0.0002 meaning that for 1 unit increase in the square footage of living space there is an associated 0.02%  increase in the price of a house.
- The coefficeint of the log of bedrooms is -0.0803 meaning than for each 1% increase in bedrooms there is an associated 0.0803% decrease in the house price.
- The floors coefficient is -0.0105 meaning that for each one unit increase in floors there is an associated 1.05% decrease in the price of the house.
- The waterfront_YES coefficient is 0.2636 meaning that  there is an expected increase of 26.36% in price of house with access to a waterfront as compared to those without access.


## Conclusions
- The model is statistically significant, with an R-squared value of 0.52, indicating that the independent variables in the model can explain approximately 52% of the variation in the dependent variable price.
- The sqft_living variable has a positive impact on the price of a house, with a 1 unit increase in square footage of living space resulting in a 0.02% increase in price.
- The number of bedrooms has a negative impact on the price of a house, with a 1% increase in bedrooms resulting in a 0.0803% decrease in price.
- Access to a waterfront has a positive impact on the price of a house, with an expected increase of 26.36% in price for houses with access to a waterfront compared to those without access.
- The number of floors has a negative impact on the price of a house, with a one unit increase in floors resulting in a 1.05% decrease in price.
- The variables view_GOOD and grade_12 Luxury are not statistically significant in the model, indicating that they may not have a strong impact on the price of a house.


## Recommendations
- Azizi real estate agency should advise their clients that the square footage of living space is an important factor that can positively impact the price of a house.
- The agency should also inform their clients that having more bedrooms may not necessarily result in a higher price for their house.
- The agency should highlight the value of waterfront access and its positive impact on the price of a house.
- The real estate company should advise their clients that having more floors may not necessarily result in a higher price for their house.

