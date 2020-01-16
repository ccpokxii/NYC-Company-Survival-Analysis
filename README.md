# NYC Business Longevity Analysis

## Dataset
* [Legally_Operating_Businesses.csv](https://github.com/the-yanqi/DS1001project/blob/master/Legally_Operating_Businesses.csv)
    - Source: NYC Open Data: *Legally Operating Business*
    - URL: https://data.cityofnewyork.us/Business/Legally-Operating-Businesses/w7w3-xahh. (accessed: 11.20.2019)
    - Description: This dataset contains200375instances of the businesses that have existed or are still operating in New York City. Eachinstance contains location information: `City`, `Street`, `Zip Code`; license information: `License Type` (Businessor Personal), `License Creation/Expiration Date`; and business information: `names`, `phones` and `Industry Type`
* [new_york.csv](https://github.com/the-yanqi/DS1001project/blob/master/new_york.csv)
    * Source: Zip Code Demographics By State And County Batch Report
    * URL:https://www.cdxtech.com/tools/bulk/demographics/state-and-county/?from=singlemessage&isappinstalled=0. (accessed: 11.22.2019)
    * Description: The demographic data contains all2153zip codes of the New York state.  Demographic information includes `Population`, `Ethnicity Distribution`,`Households`, `Sex Percentage`, `Income` etc.

## Project Goal
Our project aims to 
1. predict the lifespan of a business;
2. understand how different factors impact the lifespan

from the two data sets above.

## Jupyter Notebooks
*  [Datacleaning_Attempt.ipynb](https://github.com/the-yanqi/DS1001project/blob/master/Datacleaning_Attempt.ipynb): First Attempt in data cleaning; Include brainstormed basic ideas
*  [Regression_FeatureSelection.ipynb](https://github.com/the-yanqi/DS1001project/blob/master/Regression_FeatureSelection.ipynb): Linear Regression in depth (was not included in the final report); backward selection, vif(remove colinearity), assumption check
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
>   * Model 1: Kaplan-Meier Estimate
>   * Model 2: Cox Proportional Hazards regression model
>   * Model 3: Multiclass Regression
>       * Algorithms: Random Forest, Decision Tree, K-nearest Neighbors, Logistic Regression
>       * Metrics: Confusion Matrix, Precision, Recall, F1-score