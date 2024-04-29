# cpal_eviction_public
Public facing methodology for CPAL eviction project with Professor Spector.

## Project Overview 
### Abstract
For the CPAL Eviction project, the ultimate goal is to explore the economic impact of eviction on tenants. To do so, we are able to take different approaches to the data to get a wide and encompassing picture of what this looks like in Dallas, TX. We are able to explore judgment amounts, predatory effects of payday lenders, demographics, and more from our data to create a good picture of the economic impact.  


## Data
For the project, we used datasets from different sources. DallasCounty_EvictionJudgements, DallasCounty_EvictionRecords, and DallasCounty_HistoricalEvictionRecords were provided by CPAL. EvictionJudgements contains data about judgments from the year 2021. From this dataset, we used the judgement amounts for each eviction case filed. From EvictionRecords, there is data of evictions ranging from January 2017-June 2022. We used the case number, amount filed, GEOID, Census Tract, latitude, and longitude. From this data, we were able to map the evictions in Dallas County. HistoricalEvictionRecords contains a wider selection of evictions ranging from 2000-2022. For our analysis, we focused on evictions from 2017-2022 from this dataset. As with EvictionRecords, we utilized case number, amount filed, GEOID, Census Tract, Latitude, and Longitude in order to map the evictions. NTEP_eviction_cases was also provided by CPAL. This dataset included eviction cases from 2017-2023. We utilized the eviction cases and judgment amounts for our pre and post COVID-19 analysis. The income dataset came from the 2020 Dallas County Census data. From this dataset, we used the Tract, Total Median Income, Owner Median Income, and Renter Median Income.
Finally, the Rent data set came from the American Community Survey (ACS) from the Dallas Census. This dataset was a 5 year average of median rent as of 2021 with values ranging from 2016-2021. From this dataset, we used the GEOID, Census Tract ID, and the average rent in dollars from the dataset. 


## Methods - Analysis
### Maps
what and results w/ images
### Graphs
In the summer of 2023, SMU REU students explored this project further. Their main focus in regards to evictions was analyzing the judgment amounts along with the number of evictions, and evictions regarding renters. 
In order to properly analyze our data set, mainly the Historical Evictions Merged dataset, we first wanted to take out any entries that corresponded to the eviction of businesses as at this time are only interested in residential evictions. From this, we were able to create a data subset that disregarded approximately 450 of these business eviction entries. We then were interested in looking at residential eviction cases with judgements of `$0`. We were able to find that 16.874% of the eviction dataset were eviction cases that ended with `$0` in judgements. Once we were able to conceptualize this, we moved on to the non-zero judgment cases that we are more interested in and make up the majority of our data . To visualize these non-zero judgements, we created a histogram with the judgment amount and counts to see the distribution
[Distribution of Non-Zero Judgement Amounts of Residential Locations](results/nonzerojudge.png) 
