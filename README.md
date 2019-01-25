# Seattle AirBnB Analysis using CRISP-DM


### Table of Contents

1. [Libraries Used](#libraries)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Summary of Results](#results)
5. [Acknowledgements](#acknowledgements)

## Libraries Used <a name="libraries"></a>

This project was implemented using the Anaconda distribution of Python 3.0. The specific python libraries that were used are:

1. NumPy
2. Pandas
3. Matplotlib
4. Seaborn
5. NLTK 
6. Collections
7. Sklearn

## Project Motivations<a name="motivation"></a>

For this project, I was interested in exploring the AirBnB dataset for Seattle. The 3 key themes for my data exploration were to better understand pricing trends, review sentiments and pricing prediction. Some of the questions I analyzed were:

1. How does pricing increase or decrease by season and what is the peak season in Seattle?
2. How does pricing increase or decrease by neighborhood and which ones are the priciest neighborhoods in Seattle?
3. How does property types within neighborhoods impact price for the most expensive neighborhoods and most common property types?
4. How can we categorize reviews based on sentiments?
5. Can we map positive and negative sentiments from reviews to neighborhoods to understand which neighborhoonds rank higher on the positive sentiment scale and which ones rank higher on the negative sentiment scale?
6. Can we explore some of the worst reviews for additional insights?
7. Can we predict price for a given listing?
8. What factors of the listing correlate best for predicting price?


## File Descriptions <a name="files"></a>

There is 1 Jupyter notebook available here to showcase the analysis done in order to explore the Seattle AirBnB dataset, the data prepartion and wrangling as well as building of the prediction models in order to answer the above questions. The notebook contain markdown cells to assist with documentation of the steps as well as to communicate findings based on each analysis.

An HTML version of the notebook is also available for reference.

Lastly, the seattle folder contains the dataset from Kaggle (https://www.kaggle.com/airbnb/seattle). It contains 3 files:
- calendar.csv: calendar availability of listings and price
- listings.csv: information about all the available listings
- reviews.csv: listing reviews by users

## Summary of Results<a name="results"></a>

The key findings from the analysis are summarized below:

1. It was found that the peak season in Seattle were during the summer months from June through August, with the peak month being July. 
2. The Southeast Magnolia neighborhood was the priciest neighborhood in Seattle, followed by Portage Bay. Rainier Beach was the cheapest.
3. Looking further at neighborhoods and property types, it was found that Houses in Portage Bay are the most expensive followed by Houses in West Queen Anne and Westlake. In Westlake, both Houses and Apartments could be found at approximately the same price range.
4. With the help of SentimentIntensityAnalyzer, I was able to map reviews to their respective sentiments of positive, negative or neutral. It was found that 97.2% of reviews were mostly positive, with 1% negative reviews and 1.8% of reviews that were neutral.
5. In exploring review sentiments by neighborhoods, it was found that Roxhill, Cedar Park and Pinehurst were the neighborhoods with the most positive reviews, while University District, Holly Park and View Ridge ranked lower.
6. In exploring the worst reviews, it was found that SentimentIntensityAnalyzer associate non-English reviews with negative sentiments. 
7. Using LinearRegression, I was able to predict price based on a prepped and cleaned dataset, with an r2score of 0.62 on both training and test datasets.
8. It was found that the features that had the most impact on price were a combination of host details as well as descriptive information about the listing.

## Acknowledgements<a name="acknowledgements"></a>

Huge credit to the AirBnB dataset published by AirBnB and Kaggle for hosting it, the dataset used can be found here: https://www.kaggle.com/airbnb/seattle

SentimentIntensityAnalyzer example was adapted from: https://medium.com/analytics-vidhya/simplifying-social-media-sentiment-analysis-using-vader-in-python-f9e6ec6fc52f

Heatmap reference from: https://stackoverflow.com/questions/12286607/making-heatmap-from-pandas-dataframe
