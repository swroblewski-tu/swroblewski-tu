"Global Happiness: Exploring Factors that Shape Well-being"
Stella Wroblewski
If running the notebook, please download the csv for the datasets linked below

[Link to my GitHub webpage](https://swroblewski-tu.github.io/)

## Project Questions
1. Main Research Question:
How do socio-economic factors, quality of life indices, and dietary patterns contribute to the subjective well- being of individuals in different countries?

2. Happiness and Quality of Life:
To what extent does the Quality of Life Index align with reported happiness scores in different countries?
How do specific quality of life indicators (e.g., purchasing power, safety, healthcare) correlate with reported happiness?

3. Correlation between Quality of Life and Cost of Living:
What is the relationship between Quality of Life and Cost of Living, and how does it vary among countries?

4. Feature Importance for Happiness Prediction:
Which features contribute the most to the prediction of Happiness Scores, and how do these align with conventional wisdom or societal expectations?

5. Clustering and Regional Patterns:
Are there discernible regional patterns in happiness and quality of life indices, and how are these influenced by socio-economic and food-related factors?

6. Impact of Dietary Patterns on Happiness:
To what extent do different diets, such as Mediterranean or vegetarian, impact reported happiness scores?
Can specific food-related variables from the dataset be identified as significant predictors of happiness?


## Project Datasets

### Diet by country

[Link to FAO food balance data](https://www.fao.org/faostat/en/#data/FBS)

[Link to FAO food balance data CSV (2019_food_data.csv)](https://github.com/swroblewski-tu/swroblewski-tu.github.io)

This dataset comes from the Food and Agriculture Organization of the United Nations. This data is collected every year and has been cited in numerous academic studies as well as National Geographic as a way to understand food consumption by country. For the scope of this project we will only be using the 2019 data. All data has been previously normalized to population. The main measure in this dataset that will be used is food supply quantity (how much of a certain food is in the food supply by weight). The data also divides into categories of where the food is going such as livestock, waste, seed for new crops, tourists, etc. 

### Quality of Life by country


[Link to Quality of Life data](https://www.numbeo.com/quality-of-life/rankings_by_country.jsp?title=2019)

This dataset comes from the website numbeo is the largest database of crowdsourced information regarding cost of living and quality of life. Because of the crowd sourcing nature of the data, there is a much wider scope of the countries included compared to other sources. For the scope of this project we will only be using the 2019 data. A description of the metrics used taken from the website orginally can be found below. 


"Quality of Life Index is an estimation of the overall quality of life in a city or country.It takes into account various factors that impact one's quality of life, including purchasing power, pollution levels, housing affordability, cost of living, safety, healthcare quality, commute times, and climate conditions. The index is designed to provide a comparative measure, where a higher index value indicates a better quality of life.

It's important to note that the Quality of Life Index is based on data and user surveys collected by Numbeo. The surveys capture the perceptions and experiences of visitors to the website regarding various aspects of quality of life. Numbeo strives to provide accurate and up-to-date information by filtering out potential spam and ensuring a sufficient number of contributors for each city or country.

The index is calculated using an empirical formula that assigns weights to each factor based on its importance. The specific formula used by Numbeo may vary and is subject to change. It combines the data collected for each factor to generate a numerical value that represents the quality of life in a particular location.

The Quality of Life Index (higher is better) is an estimation of the overall quality of life by using an empirical formula that takes into account the following factors:

Purchasing Power Index (higher is better)
Pollution Index (lower is better)
House Price to Income Ratio (lower is better)
Cost of Living Index (lower is better)
Safety Index (higher is better)
Health Care Index (higher is better)
Traffic Commute Time Index (lower is better)
Climate Index (higher is better)"

### Happiness by country

[Link to Quality of Life data](https://www.numbeo.com/quality-of-life/rankings_by_country.jsp?title=2019)

This dataset comes from the website numbeo is the largest database of crowdsourced information regarding cost of living and quality of life. Because of the crowd sourcing nature of the data, there is a much wider scope of the countries included compared to other sources. For the scope of this project we will only be using the 2019 data. A description of the metrics used taken from the website orginally can be found below. 


"Quality of Life Index is an estimation of the overall quality of life in a city or country.It takes into account various factors that impact one's quality of life, including purchasing power, pollution levels, housing affordability, cost of living, safety, healthcare quality, commute times, and climate conditions. The index is designed to provide a comparative measure, where a higher index value indicates a better quality of life.

It's important to note that the Quality of Life Index is based on data and user surveys collected by Numbeo. The surveys capture the perceptions and experiences of visitors to the website regarding various aspects of quality of life. Numbeo strives to provide accurate and up-to-date information by filtering out potential spam and ensuring a sufficient number of contributors for each city or country.

The index is calculated using an empirical formula that assigns weights to each factor based on its importance. The specific formula used by Numbeo may vary and is subject to change. It combines the data collected for each factor to generate a numerical value that represents the quality of life in a particular location.

The Quality of Life Index (higher is better) is an estimation of the overall quality of life by using an empirical formula that takes into account the following factors:

Purchasing Power Index (higher is better)
Pollution Index (lower is better)
House Price to Income Ratio (lower is better)
Cost of Living Index (lower is better)
Safety Index (higher is better)
Health Care Index (higher is better)
Traffic Commute Time Index (lower is better)
Climate Index (higher is better)"


## Proposed Models


1. Prediction Model with Expanded Features:
Build an enhanced happiness prediction model using a combination of socio-economic features, quality of life indices, and additional features from the food dataset (e.g., diet composition, food availability).
Objective: Understand how a broader set of features, including food-related variables, contributes to predicting happiness.

2. Food Impact Analysis Model:
Develop a model to analyze the impact of different diets on happiness scores, considering both quality of life indices and happiness data.
Objective: Investigate the relationship between dietary patterns and subjective well-being, providing insights into the role of food in happiness.

3. Regional Happiness Clustering with Food Factors:
Apply clustering algorithms to group countries based on happiness scores, quality of life indices, and food-related features.
Objective: Identify regional patterns in well-being, considering both socio-economic factors and dietary habits.

4. Causal Inference Analysis:
Apply causal inference techniques to investigate potential causal relationships between food-related variables and happiness, addressing confounding factors.
Objective: Explore whether changes in diet composition have a causal impact on happiness, considering potential interventions.


## Exploratory Data Analysis (EDA)

### Find the top 5 countries with the highest quality of life scores:
Top 5 Countries with the Highest Quality of Life Index:
<img width="237" alt="Screenshot 2023-12-13 at 5 02 21 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/b2ba61e6-8975-4cb3-b227-f114e9dca1cb">

### Display initial summary statstics for the quality of life dataset
Summary Statistics for Quality of Life Data:
<img width="190" alt="Screenshot 2023-12-13 at 5 02 38 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/1d164a1f-a602-495f-8433-9454fe117a16">


### Graph 1: the quality of life scores against cost of living. The scatter plot reveals a strong positive correlation between Quality of Life Index and Cost of Living Index. 

#### This correlation suggests that countries with higher Quality of Life tend to have higher costs of living. This may be attributed to better amenities, healthcare, and overall standards of living, which often come at a higher financial cost.
<img width="512" alt="Screenshot 2023-12-13 at 5 03 13 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/b63323d8-e8eb-4a11-9a1c-9aad91f60964">

### Graph 2: The scatter plot explores the relationship between Happiness Score and Quality of Life Index for different countries in 2019. Each point represents a country, and there's a visible positive correlation, suggesting that countries with higher Quality of Life tend to have higher Happiness Scores. 

#### The positive correlation implies that as the overall quality of life improves, citizens of that country are more likely to report higher levels of happiness. This aligns with the intuitive expectation that factors contributing to a better quality of life, such as healthcare, safety, and economic prosperity, positively influence the subjective well-being of individuals.

<img width="533" alt="Screenshot 2023-12-13 at 5 03 53 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/08f22524-65bf-4177-bab7-8d1a7e844653">


### Graph 3: The bar plot illustrates the importance of different features in predicting the Happiness Score
#### Features such as 'GDP per capita' and 'Social support' have higher importance values as you can see by the increased correlations.
<img width="606" alt="Screenshot 2023-12-13 at 5 04 26 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/9116b008-d7ed-4db1-b4c8-89aa472323ef">

### Graph 4: This graph is a sample exploring the food dataset.  

#### The bar graphs shows the 5 most common food items across all countries and the consumption rates all normalized to population size

<img width="600" alt="Screenshot 2023-12-13 at 5 04 49 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/4297f57d-6371-40ec-91c5-926bb8b3426d">

### Graph 5: This graph displays the 10 most common food items across the 20 happiest countries

#### Just by visually comparing the two graphs you can see that in the happier countries, the most common food item milk while in the least happy countries the most common food item is sugar.
<img width="601" alt="Screenshot 2023-12-13 at 5 05 14 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/2d62eb88-5830-4c6e-bce3-b6aee9087a25">
<img width="597" alt="Screenshot 2023-12-13 at 5 05 24 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/72e29aad-3376-44d6-8fc1-e40e51c3e8c3">

### Table 1: This table displays the 10 food items most correlated with happiness

#### You can see that the items with the highest correlations are cream, coffee, and bovine meat.
<img width="474" alt="Screenshot 2023-12-13 at 5 05 50 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/305ef601-7c74-4431-b6e2-9a6886433acb">

### Table 2: This table displays the 10 food items least correlated with happiness

#### You can see that the items with the lowest correlations are sugar, plaintains, and beans.
<img width="400" alt="Screenshot 2023-12-13 at 5 06 08 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/7b9172fc-d56c-4fd0-99c6-9f9a0cc8e989">

## Modeling and Analysis
<img width="603" alt="Screenshot 2023-12-13 at 5 06 34 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/b10e7e92-36a1-45f7-b52d-c0961a51e820">

### Graph 6: This graph displays a  map of the world, where countries are grouped into clusters based on certain socio-economic and quality of life factors.

#### Each cluster is represented by a distinct color on the map, with a corresponding legend to help interpret the colors. The figure also includes red points that mark the centroids of each country within its respective cluster, calculated based on the geographical shape of each country.

<img width="602" alt="Screenshot 2023-12-13 at 5 06 59 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/46ce93d7-fcc9-47ca-88d1-7b60bd23f9b5">

## Conclusions and Discussion
### Analysis
#### Model Selection Rationale
This investigation used prediction models and clustering algorithms to address the central topic of the impact of dietary components, quality of life, and socioeconomic status on well-being. The necessity to fully represent the complex interplay of various variables in happiness determinants, as demonstrated by Figure 6, led to the selection of these models in particular.
### Conclusions / Future Expansion
The outcomes validate our research questions. Figures 1 and 2 show a substantial association between happiness scores and quality of life measures, confirming the importance of these aspects in assessments of well-being. This investigation focused on the relationship between diet and happiness, and found that certain dietary components were significantly associated with greater happiness levels (Tables 1 and 2).

These findings are constrained by the features of the datasets. The extent of the dataset and the possibility of bias could limit how broadly applicable our results can be. Further research, including utilizing a wider range of data, is necessary to substantiate and broaden our findings. Further exploration of the diet factors would allow for more concrete conclusions. Currently we can't say if the food items that are correlated with happiness have anything to do with physical health or if these are simply higher cost food items (further upholding the claim that cost of living is directly correlated with happiness and quality of life). This study highlights the complex link between lifestyle factors and happiness, laying the foundation for future investigations of this kind.
