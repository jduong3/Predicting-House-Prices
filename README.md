# Predicting-House-Prices
## Introduction

For one of my course projects, I chose house prices as the focus, recognizing the relevance and insights it could offer in the ongoing housing crisis. The project required analyzing the "House Prices – Advanced Regression Techniques" dataset from Kaggle, a comprehensive collection of 1,460 residential homes in Ames, Iowa, each characterized by 80 unique features. These features ranged from garage quality to the type of foundation, underscoring the complexity of factors influencing house prices beyond mere location and the number of bedrooms. The challenge presented by the project was to build a machine learning model capable of accurately predicting the sales prices of homes in a separate testing dataset, which consisted of 1,458 houses with the sales prices withheld.

## Importance

The decision to delve into this dataset stemmed from the urgent need to empower home buyers in a market where demand far outstrips supply, leading to inflated prices and potential exploitation. By using machine learning, I aimed to provide buyers with the tools to estimate reasonable prices based on various house features, enabling them to make informed decisions, whether that meant adjusting their expectations within a preferred area or considering alternatives in neighboring regions. Similarly, I saw the potential benefits for sellers, who could identify the features that most significantly drive sales, thereby contributing to a market that better meets current demand.

## Techniques

My approach began with a thorough cleaning of the data. I meticulously checked for duplicates and missing values, addressing the latter by categorizing them as either numerical or categorical. For categorical data, I replaced missing values with a placeholder, and for numerical data, I used the median to fill gaps. With a clean dataset in hand, I conducted exploratory data analysis, starting with the distribution of the target variable, "SalePrice." This revealed a right-skewed distribution, indicating that the majority of homes fell within a lower price range.

To identify the most significant predictors of "SalePrice," I examined correlations across the 80 features. Notably, "OverallQual," "GrLivArea," and "GarageCars" emerged as the top predictors. I visualized these relationships through scatterplots and boxplots, confirming strong positive correlations—particularly between "GrLivArea" and "SalePrice," as well as between "OverallQual" and "SalePrice." Interestingly, while "GarageCars" also showed a positive correlation, this relationship plateaued after a garage capacity of three cars.

Following this analysis, I prepared the data for machine learning by converting categorical variables to numerical values and splitting the dataset into training and testing subsets. I then trained and evaluated three models: Neural Network, Random Forest, and Gradient Boosting. Gradient Boosting emerged as the most accurate, achieving a 90% accuracy rate and outperforming the other models in handling the skewed distribution of house prices. Given its sequential learning process, Gradient Boosting was particularly effective at reducing both bias and variance.

## Model Results

The predictions made by the Gradient Boosting model aligned closely with the insights gained during exploratory analysis, further validating the model’s robustness. For instance, homes with higher overall quality, larger ground living areas, and larger garages commanded higher prices, consistent with my expectations.

## Conclusions & Future Improvements

In conclusion, Gradient Boosting proved to be the most effective model for predicting house prices in this dataset, largely due to its ability to refine its predictions iteratively. While the project provided valuable insights into the Ames, Iowa housing market, I recognize the potential for future research to extend these findings to other regions, such as California, where location might play an even more significant role in determining house prices. Comparing the importance of different features across various cities and states could offer a broader understanding of the factors that drive housing prices nationwide.


