# Workbook-3/HALE

In this workbook, you will use GBD data to evaluate two questions related to **Health Adjust Life Expectancy** (_HALE_):

1. How do HALE, life expectancy, and DALY rate compare? What is the meaning of these differences?
The HALE and the life expectancy are very correlated (the correlation value was very close to positive one). This means that as the life expectancy increases, the HALE increases as well. This means that as people live longer, they live healthier lives.
The HALE and the DALY had a correlation of very close to -1. This means that the relationship between these two variables is opposite fo with the HALE and life expectancy so as the HALE increases the DALY decreases.
2. As people live longer, do they live healthier lives (i.e., is a smaller fraction of life spent in poor health)?
Yes they do live healthier lives. You can see this because by looking at the third plot from the analysis (the change plot), we can see that a positive change in life expectancy is correlated with a positive change in HALE.
And a positive change in HALE means that people live a longer portion of their time in full health meaning
that a smaller fraction of their life will be speant in poor health.

## Data Download
The following raw data has been downloaded for this example. It includes 4 different datasets from the [ghdx](http://ghdx.healthdata.org/gbd-results-tool):

1. **DALY Rate for each country**: all locations, age-standardized, both sexes, 1990 and 2016, total (all) Causes. [link](http://ghdx.healthdata.org/gbd-results-tool?params=gbd-api-2016-permalink/6f5916d248678e32b200c85a5b703604)
2. **Life expectancy for each country**: all locations, 1990 and 2016, both sexes, age _<1 year_ (because they don't currently have HALE data available for all-ages -- this appears to be an error in the tool). [link](http://ghdx.healthdata.org/gbd-results-tool?params=gbd-api-2016-permalink/d2eee117ba65fdba96c982622318a07d)
3. **HALE expectancy for each country**: all locations, 1990 and 2016, both sexes, age _<1 year_ (because they don't currently have HALE data available for all-ages -- this appears to be an error in the tool). [link](http://ghdx.healthdata.org/gbd-results-tool?params=gbd-api-2016-permalink/15ca56930c5fb7d869669806e5e179b6)
4. **Location Hierarchy**: The hierarchy of each location in the [codebook](http://ghdx.healthdata.org/sites/default/files/ihme_query_tool/IHME_GBD_2016_CODEBOOK.zip).

Files have been extracted from `.zip` folders, renamed, and saved in the `data/raw/` folder.

## Data Prep
To create the _prepped_ version of the data, simply run the `prep_data.R` file, which will do the following:

1. Limit locations to **countries only**
2. Rename columns of interest
3. Join the data
4. Save the data in a new `data/prepped/` folder

## Workbook
See instructions in the `analysis.R` file for the workbook.