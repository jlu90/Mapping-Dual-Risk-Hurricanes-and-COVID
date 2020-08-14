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
**Uri speak about geoc
**Jocelyn speak about the composite score**





## Data Dictionary
---
Column | Description
- | - | 
state | a state is a constituent political entity |
county | administrative division of a state or country |
cat_1_count | a hurricane where winds range from 74 to 95 mph |
cat_2_count | a hurricane where winds range from 96 to 110 mph |
cat_3_count | a hurricane where winds range from 111 to 129 mph |
cat_4_count | a hurricane where winds range from 130 to 156 mph |
cat_5_count | a hurricane where winds range from 157 to 200 mph |
hurricane_count | total number of hurricanes of a county |
tropical_storm_count |
extratropical_system_count |
tropical_depression_count |
low_count | 
subtropical_depression_count |
dissipating_storm_count | 
current_cases | number of current people infected in a county |
deaths | number of deaths due to COVID-19 |   
previous_cases | number of cases before ...
previous_deaths |  number of deaths before ...
2019_population | total inhabitants of a county |
change_in_case_ratio | 


## Conclusion & Recommendation
---



## References
---
[Hurricane Data](https://www.nhc.noaa.gov/data/)

[COVID-19 Data](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data )

[Costliest Hurricanes](https://www.usatoday.com/story/money/2018/09/12/most-destructive-hurricanes-of-all-time/36697269/)

