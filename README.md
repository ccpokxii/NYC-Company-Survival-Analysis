# NYC Business Longevity Analysis

## Dataset
* *Legally_Operating_Businesses.csv*
    - Source: NYC Open Data: *Legally Operating Business*
    - URL: https://data.cityofnewyork.us/Business/Legally-Operating-Businesses/w7w3-xahh. (accessed: 11.20.2019)
    - Description: This dataset contains200375instances of the businesses that have existed or are still operating in New York City. Eachinstance contains location information: City, Street, Zip Code; license information: License Type (Businessor Personal), License Creation/Expiration Date; and business information: names, phones and Industry Type
* *new_york.csv*
    * Source: Zip Code Demographics By State And County Batch Report
    * URL:https://www.cdxtech.com/tools/bulk/demographics/state-and-county/?from=singlemessage&isappinstalled=0. (accessed: 11.22.2019)
    * Description: The demographic data contains all2153zip codes of the New York state.  Demographic information includes Population, Ethnicity Distribution,Households, Sex Percentage, Income etc.

## Project Goal
Our project aims to predict the lifespan of a business and understand how different factors impact the lifespan from the two data sets above.

## Jupyter Notebooks
*  [Datacleaning_Attempt.ipynb](https://github.com/the-yanqi/DS1001project/blob/master/Data-cleaning%20attempt.ipynb): First Attempt in data cleaning; Include brainstormed basic ideas
*  [Regression_FeatureSelection.ipynb](https://github.com/the-yanqi/DS1001project/blob/master/Regression_FeatureSelection.ipynb): Linear Regression in depth (was not included in the final report)
*  [Cox's_Proportional_Hazard_Analysis.ipynb](https://github.com/the-yanqi/DS1001project/blob/master/Cox's_Proportional_Hazard_Analysis.ipynb): Notebook walks through the entire project

>   ### Table of Contents
>   ***
>  * Load Raw Data
>   * Clean Raw Data
>       * Clean raw business data
>           * Remove non-NYC businesses
>           * Keep columns that are relevant to the problem of interest
>           * Check selection bias
>           * Drop rows with NaN values
>       * Clean raw nyc data
>           * Only keep columns that are relevant to the problem of interest.
>           * Create more useful features from current columns
>       * Merge two dataframe by column ZIP
>   * Feature Processing
>       * One-hot encode on industry type
>       * Create Target Variables
>       * Generate clean data for modeling
>   * Baseline: Simple Regression
>   * Model 1: Kaplan-Meier
>   * Model 2: Cox Proportional Hazards regression model
>   * Model 3: Multiclass Regression
>