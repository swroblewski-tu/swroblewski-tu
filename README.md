# "Global : Exploring Factors that Shape Well-being"
#### Stella Wroblewski
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

7. Ensemble Models and Predictive Accuracy:
How does the predictive accuracy of ensemble models, combining various base models, compare to individual models in predicting Happiness Scores?

8. Causal Relationships between Diet and Happiness:
Can causal relationships be inferred between changes in diet composition and reported happiness, accounting for potential confounding factors?

## Project Datasets
### Diet by country

[Link to FAO food balance data](https://www.fao.org/faostat/en/#data/FBS)

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

[Link to World Happiness Report](https://worldhappiness.report/ed/2019/#appendices-and-data)

[Link to World Happiness Report data](https://worldhappiness.report/data/)

This dataset comes from the "World Happiness Report". This data is collected every year and has been cited in numerous academic studies as a way to understand percieved happiness by country. For the scope of this project we will only be using the 2019 data. A description of the metrics used taken from the project orginally can be found below. 

"The World Happiness Report is a landmark survey of the state of global happiness that ranks 156 countries by how happy their citizens perceive themselves to be. The World Happiness Report 2019 focuses on happiness and the community: how happiness has evolved over the past dozen years, with a focus on the technologies, social norms, conflicts and government policies that have driven those changes."

## Proposed Models

1. Prediction Model with Expanded Features:
Build an enhanced happiness prediction model using a combination of socio-economic features, quality of life indices, and additional features from the food dataset (e.g., diet composition, food availability).
Objective: Understand how a broader set of features, including food-related variables, contributes to predicting happiness.

2. Food Impact Analysis Model:
Develop a model to analyze the impact of different diets (e.g., Mediterranean, vegetarian) on happiness scores, considering both quality of life indices and happiness data.
Objective: Investigate the relationship between specific dietary patterns and subjective well-being, providing insights into the role of food in happiness.

3. Regional Happiness Clustering with Food Factors:
Apply clustering algorithms to group countries based on happiness scores, quality of life indices, and food-related features.
Objective: Identify regional patterns in well-being, considering both socio-economic factors and dietary habits.

4. Happiness Prediction with Ensemble Models:
Utilize ensemble models to combine predictions from multiple base models, including linear regression, random forest, and potentially models focused on food factors.
Objective: Improve predictive accuracy by leveraging the strengths of different modeling approaches.

5. Causal Inference Analysis:
Apply causal inference techniques to investigate potential causal relationships between food-related variables and happiness, addressing confounding factors.
Objective: Explore whether changes in diet composition have a causal impact on happiness, considering potential interventions.

## Exploratory Data Analysis (EDA)

### Find the top 5 countries with the highest quality of life scores:
Top 5 Countries with the Highest Quality of Life Index:
<img width="272" alt="Screenshot 2023-11-08 at 10 33 28 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/998fa9b4-bfbb-4435-8c0b-028f68c9d6df">
### Display initial summary statstics for the quality of life dataset

<img width="210" alt="Screenshot 2023-11-08 at 10 34 03 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/b28545f3-a2f4-4b6f-b02f-485beabeedfe">

### Graph 1: The bar plot shows the distribution of the quality of life scores to show the spread of values. The range, also displayed in the summary statistics above, is from 84 to 198.
<img width="582" alt="Screenshot 2023-11-08 at 10 34 21 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/5cb85c52-272a-48bb-a137-482421178e1c">

### Graph 2: the quality of life scores against cost of living. The scatter plot reveals a strong positive correlation between Quality of Life Index and Cost of Living Index. 

#### This correlation suggests that countries with higher Quality of Life tend to have higher costs of living. This may be attributed to better amenities, healthcare, and overall standards of living, which often come at a higher financial cost.
<img width="580" alt="Screenshot 2023-11-08 at 10 34 41 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/781ab2e6-a2a6-44de-8e1a-491dd097adf1">

### Graph 3: The scatter plot explores the relationship between Happiness Score and Quality of Life Index for different countries in 2019. Each point represents a country, and there's a visible positive correlation, suggesting that countries with higher Quality of Life tend to have higher Happiness Scores. 

#### The positive correlation implies that as the overall quality of life improves, citizens of that country are more likely to report higher levels of happiness. This aligns with the intuitive expectation that factors contributing to a better quality of life, such as healthcare, safety, and economic prosperity, positively influence the subjective well-being of individuals.

<img width="600" alt="Screenshot 2023-11-08 at 10 35 09 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/91205482-34bb-4ffe-ab4c-4fd65c87ac74">

### Graph 4: The scatter plot compares the actual Happiness Scores to the scores predicted by a linear regression model. Each point on the plot represents a country, where the x-axis represents the actual Happiness Score, and the y-axis represents the predicted score from the linear regression model.

#### The red dashed line serves as a reference for a perfect match between actual and predicted scores. Deviations from this line indicate the model's prediction errors. The concentration of points close to the line suggests that the linear regression model is relatively accurate in predicting Happiness Scores. However, noticeable deviations may indicate areas where the model can be further refined.
<img width="582" alt="Screenshot 2023-11-08 at 10 35 30 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/17b522c9-47d7-454b-9319-65e3060f4bdc">

#### Graph 5: The bar plot illustrates the importance of different features in predicting the Happiness Score, as determined by a Random Forest Regression model. 

#### Features such as 'GDP per capita' and 'Social support' have higher importance values.

<img width="860" alt="Screenshot 2023-11-08 at 10 35 52 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/32f9e551-c4e8-436e-8912-a9f8a0a747fd">

#### Graph 6: These graphs are a sample as we begin to look at how diet and food play into these evaluations. 

#### The bar graphs show the amount of wheat production and domestic wheat supply by country. This will factor into our analysis later. 
<img width="942" alt="Screenshot 2023-11-08 at 10 36 18 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/a79094f1-cf2e-43d1-b451-bc587df5a597">
<img width="956" alt="Screenshot 2023-11-08 at 10 36 43 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/406aa1ec-5f76-4666-ac04-876c9a7ee0d6">





