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


### Happiness by country
[Link to World Happiness Report](https://worldhappiness.report/ed/2019/#appendices-and-data)





Top 5 Countries with the Highest Quality of Life Index:
       Country  Quality of Life Index
0      Denmark                  198.6
1  Switzerland                  195.9
2      Finland                  194.0
3    Australia                  191.1
4      Austria                  191.1

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

Correlation between Quality of Life and Cost of Living: 0.85

