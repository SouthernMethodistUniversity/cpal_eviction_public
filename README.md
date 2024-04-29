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
Next, we were able to generate many maps to show evictions by census tract, judgment amount by census tract, median contract rent by census tract, median renter income by census tract, and percent rent of income by census tract. 

![Number of Evictions](results/numevict.png?raw=true)

![Income](results/med_income.png?raw=true?raw=true)

![Judgement Amounts](results/med_jud_amt.png?raw=true)

![Percent Rent of Income](results/med_pct_rent.png?raw=true)

![Number of Evictions](results/num_evict.png?raw=true)

### Graphs
In the summer of 2023, SMU REU students explored this project further. Their main focus in regards to evictions was analyzing the judgment amounts along with the number of evictions, and evictions regarding renters. 
In order to properly analyze our data set, mainly the Historical Evictions Merged dataset, we first wanted to take out any entries that corresponded to the eviction of businesses as at this time are only interested in residential evictions. From this, we were able to create a data subset that disregarded approximately 450 of these business eviction entries. We then were interested in looking at residential eviction cases with judgements of `$0`. We were able to find that 16.874% of the eviction dataset were eviction cases that ended with `$0` in judgements. Once we were able to conceptualize this, we moved on to the non-zero judgment cases that we are more interested in and make up the majority of our data . To visualize these non-zero judgements, we created a histogram with the judgment amount and counts to see the distribution

![Distribution of Non-Zero Judgment Amounts of Residential Locations](results/distnonzerojudge.png?raw=true) 

Additionally, the distribution of Non-Zero Judgment amounts only including residential evictions was graphed. 

![Distribution of Non-Zero Judgment Amounts of Residential Locations](results/distresidentialnonzero.png?raw=true)

One problem that we encountered in the data was repeat case numbers. We were unsure whether these repeats were intentional and important to keep, so we had to do some investigating. Some of the defendants appeared multiple times with the same address, same cae number, and same file date. Although this information was all the same, the judgment amounts were different, so they may not be entirely identical. Upon talking to Dr. Spector, we concluded that these repeats may be due to multiple appearances in court. This could mean that the case was dismissed for the day due to weather or some other factor such as the case being reopened after being closed. Additionally, the different judgment amounts may be due to administrative fees. This is not entirely legal, so we may come back to analyze this further at a later time. Ultimately, the maximum number of times a case number reappeared in the data was three, so in our dataset of 8737 cases, this number is rather small, and we concluded that we were not concerned with this affecting our data much.  

Upon examining the eviction data we have, we found recurring instances of a single plaintiff address being associated with a variety of plaintiff names. We speculate several explanations for these associations. We attribute a handful of these cases to clerical errors in the case filings, such as misspelling and slight variations on the plaintiff address and/or plaintiff name across multiple cases. However, some plaintiff addresses appear to be associated with third-party real estate agents focused on property management and development. Additionally, in some cases, the third-party agent appears to be a company that specializes in evictions. This finding merits additional research to understand the potential impact of corporate residential services on eviction cases, specifically as it pertains to unequal representation and proficiency in eviction court. This could raise a legal issue with who the plaintiff really is. Finally, it is important to note that there are a variety of cases in the data that do not have a clear explanation as to why there are multiple plaintiff names associated with a single plaintiff address. Further research can be conducted to uncover underlying patterns between these ambiguous cases. 

We were able to see that there is an obvious decline with the number of evictions before Covid than after Covid. More interestingly, we were able to look at the slopes pre and post Covid. The slope post Covid is much higher and continually rising compared to the somewhat stagnant slope pre-Covid. 

![Covid Evictions](results/evictionmonths.png?raw=true)





