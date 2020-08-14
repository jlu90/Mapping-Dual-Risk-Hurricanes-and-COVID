# Project 5 - Identifying the Risk of COVID-19 and North Atlantic Hurricanes
Authors: Jocelyn Lutes, Quinton Lopez, Uriel Eckmann

## Problem Statement
---
Use machine learning cluster to identify areas at higher risk for COVID-19 and North Atlantic Hurricanes.

The east coast endures more storms yearly than any other area of the country. The warm temperatures of the Atlantic increase the power of hurricanes. That combined with the common patterns of winds moving east to west after being formed in the eastern Atlantic make threats to residents homes, businesses, and way of life every hurricane season. From June 1st to November 30, citizens must remain aware of hazardous weather conditions except this year, an unexpected global pandemic could cause even more worry. The number of confirmed cases have passed 5 million and deaths have reached over 160,000 in the United States. There is no vaccine created and the close proximity of large groups of people significantly increases the chances of becoming infected. Identifying the areas at risk for Covid-19 and other natural disasters can help provide proper guidance for evacuating families and prevent the further spread of Covid-19. 

## Executive Summary
---
In this project, we collected datasets for COVID-19 and North Atlantic Hurricanes to analyze and highlight the areas that showed an increase in risk.
With the focus of natural disasters in the United States, and because of the process of origination when tropical cyclones are created, this places greater emphasis on the eastern coastline compared to any other area of the country. Hurricanes have caused the most damage compared to any other climate catastrophe. Damage from Hurricane Katrina in 2017 was estimated at $160 billion for the most in U.S. history. Adding to the danger is COVID-19, which quickly spreads through airborne transmissions and is known to be deadly. With the long term effects still unknown, this disease has and could potentially attack almost anything within the body. COVID-19 has cost millions of workers their jobs and simultanesouly could impact residents in their ability to seek shelter during hurricane season or evacuate. This also places tremendous pressure on states and cities who will need aid for COVID-19 treatment, economic recovery, along with potential natural disaster aid. 

Our approach, after collecting a good amount of credible data, was to clean and combine the two datasets so they could explored and fed into a model. By imputing the features of hurricanes and COVID-19 in a clustering model, we would be able to identify the areas at higher combined risk of safety. 

In order to properly combine our two dataframes we needed to find a way to utilize common areas. To do this we used `geopandas` and `plotly`. These packages allowed us to create maps and additional features that we could aggregate our data on. The hurricane dataset included latitude and longitude locations of each hurricane. By converting the dataframe into a geopandas dataframe, a new column was created called `geometry` which stored the latitude and longitude as points. We then downloaded state and county maps of the USA that included a `geometry` column that was the latitudinal and longitudinal shapes of each location. We then utilized geopandas `within()` function to map each hurricane point to specific counties and states. The COVID data was already organized by counties, allowing us to aggregate both dataframes together. 

In addition to the aggregate storm feature and COVID-19 features that we have already engineered, we also wanted to engineer a composite feature to capture the overall historical risk of the hurricanes. Because Category 3, Category 4, and Category 5 hurricanes are the most destructive, we also wanted these storms to carry a higher weight in our composite score. Therefore, a `storm_composite` feature was engineered that was the sum of counts of tropical depressions, tropical storms, category 1 storms, category 2 storms, and the square of counts of category 3 storms, category 4 storms, and category 5 storms.

To gather, clean, and run models for the COVID-19 and hurricane dataset, you would need these software requirements. 
1. pandas
2. geopandas
3. matplotlib
4. seaborn
5. time
6. datetime
7. numpy
8. sklearn
9. plotly
10. geocode

## Contents of Repository
1. [Raw Data](https://git.generalassemb.ly/jlu90/project_5/tree/master/data)
2. [Hurricane Data Cleaning Notebook](https://git.generalassemb.ly/jlu90/project_5/blob/master/code/01_hurricane_data_cleaning.ipynb)
3. [COVID-19 Data Cleaning Notebook](https://git.generalassemb.ly/jlu90/project_5/blob/master/code/02_covid_data_cleaning.ipynb)
4 .[Project Notebook](https://git.generalassemb.ly/jlu90/project_5/blob/master/code/03_project_nb.ipynb)
[Presentation Slides](https://docs.google.com/presentation/d/1KPo8Ws_MwPrIWB6ChViykOxra26IR08ocLea3Y_8qLc/edit?usp=sharing)

## Data Dictionary
---
Column | Description
|- | - |
state | a state is a constituent political entity 
county | administrative division of a state or country 
cat_1_count | a hurricane where winds range from 74 to 95 mph 
cat_2_count | a hurricane where winds range from 96 to 110 mph 
cat_3_count | a hurricane where winds range from 111 to 129 mph 
cat_4_count | a hurricane where winds range from 130 to 156 mph 
cat_5_count | a hurricane where winds range from 157 to 200 mph 
hurricane_count | total number of hurricanes of a county 
tropical_storm_count | total number of tropical storms of a county
extratropical_system_count | total number of extratropical_system of a county
tropical_depression_count | total number of tropical depressions of a county
low_count | low pressure storm system
subtropical_depression_count | total number of subtropical depressions of a county
dissipating_storm_count | total number of dissipating storms of a county
current_cases | number of current people infected in a county 
deaths | number of deaths due to COVID-19 
previous_cases | number of cases on or before August 4, 2020
previous_deaths |  number of deaths before on or before August 4, 2020
2019_population | total inhabitants of a county 
change_in_case_ratio | the number of current cases minus previous cases divided by population multiplied by 100,000


## Conclusion & Recommendation
---
Overall, our model was able to identify clusters to ascertain relative risk in comparison to other clusters, but the significance of clusters is difficult to comprehend. Because we did not have a lot of variation in our hurricane-related features or COVID-19 features, we were not able to identify a locatation that was at an extremely high risk for COVID-19 and hurricanes. Four out of five of our clusters have an average change in COVID-19 cases per week that was greater than 100, meaning that they are considered a COVID-19 red zone. We were able to capture the geographic risk of tropical storms, but COVID-19 poses a risk across the board.

Natural Disasters can be incredibly destructive. Whether it's the cost of lives or the billions of dollars in damage, when an area is hit with Earthquakes, Hurricanes, Tornadoes, or Fires, the affect can be devastating. This is why they are taken so seriously - knowing that incoming storms can be so destructive causes people to react in an appropriate manner - whether that means evacuation, stocking up on food and ice, or taking whatever preventative measures are necessary. However, what we've seen from our data is that when you compare cost of lives of all the major storms over the last 170 years, it pales in comparison to the number of lives lost to COVID - 19. Hurricane Katrina, a storm that took over 1200 lives is less than 1 percent of the number of people lost to COVID _so far_. Our clustering data clearly emphasizes how COVID is far more dangerous than just about any other hurricane, which illustrates that the appropriate preventative measures need to be taken _more seriously_ than a natural disaster. Unfortunately, we are seeing the effects of what happens when people relax that prevention. The way people are disregarding social distancing is practically comparable to just going for a walk during a category 4 hurricane. This data also illustrates how areas in which social distancing has been maintained have lowered their case rates and potentially saved lives. 



## References
---
[County Populations Data](https://www.census.gov/data/tables/time-series/demo/popest/2010s-counties-detail.html) 

[COVID-19 Data](https://github.com/nytimes/covid-19-data)  

[IBTraACS Data](https://www.ncdc.noaa.gov/ibtracs/index.php?name=introduction)  
[U.S. Counties Shape File](https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html)  

[What is a COVID-19 red zone? by Fast Company](https://www.fastcompany.com/90529280/what-is-a-covid-19-red-zone-do-you-live-in-one-heres-how-to-find-out) 

[Strong Winds](http://ww2010.atmos.uiuc.edu/(Gh)/wwhlpr/hurricane_saffirsimpson.rxml#:~:text=Once%20it%20becomes%20a%20hurricane,The%20scale%20is%20listed%20below.&text=The%20Saffir%2DSimpson%20scale%20categorizes,scale%20from%201%20to%205)