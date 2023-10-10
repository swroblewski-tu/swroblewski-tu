# Food, Quality of Life, and Happiness
##### Stella Wroblewski

## Project goals
##### The main goal of this project is to better understand how diet and food availability impact quality of life and self reported happiness by country. 

Initial questions to be answered:

   1. How healthy are the diets of each country based on different measures of a healthy diet?
      i.e. what countries come closest to a "balanced diet", a classically defined Mediterranean diet, or a vegatarian diet 

   2. Some of these particular diets are shown in research to have impacts on peoples happiness. Does reported happiness line up with the analysis of diets within each country?

   3. One may assume that quality of life would be impacted by the quality of one's diet or access to healthy food. It also makes sense that quality of life would be a direct indicator of happiness. How are these notions reflected in the data?

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

## Exploratory Data Analysis (EDA)
#### Initial Quality of Life EDA 

Selection deleted
import matplotlib.pyplot as plt

#### find the top 5 countries with the highest QOL score
Top 5 Countries with the Highest Quality of Life Index:
       Country  Quality of Life Index
0      Denmark                  198.6
1  Switzerland                  195.9
2      Finland                  194.0
3    Australia                  191.1
4      Austria                  191.1

#### Display initial summary statstics for the quality of life dataset
Summary Statistics for Quality of Life Data:
       Quality of Life Index
count              71.000000
mean              142.311268
std                32.931416
min                84.000000
25%               113.000000
50%               145.700000
75%               169.050000
max               198.600000

#### Graph the distribution of the quality of life scores to show the spread of values
#### The range, also displayed in the summary statistics above, is from 84 to 198.
<img width="475" alt="Screenshot 2023-10-09 at 8 15 47 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/ee3438e8-e9cd-4db8-85ff-6b28cfbfd4e1">

#### Graph the quality of life scores against cost of living. You can see in the graph below that there is a positive correlation. As quality of life increases, cost of living increases as well. 
<img width="495" alt="Screenshot 2023-10-09 at 8 15 53 PM" src="https://github.com/swroblewski-tu/swroblewski-tu.github.io/assets/132031363/4c7aea8f-8544-4a73-8a41-7acdd103bcff">

Correlation between Quality of Life and Cost of Living: 0.85
