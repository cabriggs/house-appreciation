## Files included

- house-appreciation.ipynb: a Jupyter notebook containing the analysis and narrative.
- df\_citydata.csv: a data set containing information on each county in the US, including median house value during an interval
- df\_citydata\_data\_dictionary.txt: a data dictionary for df\_citydata.csv
- house-appreciation.pdf: a report of the study's findings

## Background

Recent home price volatility presents investment opportunities. The fluctuation in home prices has not been evenly distributed geographically. I used predictive analytics to predict areas of high price growth.


The model can now be deployed to predict home price growth given anticipated changes in county or city composition, or to identify counties in which prices may be primed to increase or drop. This predictive ability has business applications to investment, underwriting, etc.

## Problem statement

How much of the variation in the increase of home values across US counties can be explained by publicly available almanac data about the counties?

## What data

I gathered information from City-Data on each of the 3,141 counties in the United States. This collected information includes median income and its recent growth, demographic information (including breakdowns by age, sex, and familial status), poverty rate, percent urban, average commute times, and geographic location. Not all of the data was usable: it turns out that some of the home price levels were calculated instead of measured. But after discarding the bad data, I still had enough to proceed. I collected more than 50 pieces of information on each county. I then checked which of these were associated with home price growth - either positive or negative. 

## What methods

I trained a suite of machine learning models. Different models work better for different data sets, so I compared these models to see which would best predict the house price growth.

The best performing model was an ensemble of neural networks. This model explains about two-thirds of the change in home prices in a given county. This is a pretty good result, as we cannot expect that every factor relevant to home price change will be captured in City-Data's data sets.

### Technology

The analysis was performed in a Jupyter notebook, leveraging the pandas and scikitlearn libraries.

## What conclusions

The model can now be deployed to predict home price growth given anticipated changes in county or city composition, or to identify counties in which prices may be primed to increase or drop. This predictive ability has business applications to investment, underwriting, etc.

## What questions remain

The model, although nonlinear, can be tested for sensitivity to changes in each input over a variety of intervals. However, as the study is observational, the model does not establish causality among the variables. One way to extend this study would be to determine causality among the dependent variables and the target variable.

