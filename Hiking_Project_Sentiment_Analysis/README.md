# Hiking_Project_sentiment_analysis
Here is a complete documentation of the sentiment analysis project on Google Play app reviews:

# Sentiment Analysis of Google Play App Reviews

## Introduction

This project performs sentiment analysis on user reviews for a Google Play app called "Hiking Project". The goal is to analyze the sentiment (positive, negative) in the reviews to gain insights into users' perception of the app.

## Methodology

The key steps are:

1. Use the `google_play_scraper` library to scrape the latest user reviews for the Hiking Project app. Reviews are scraped in English for the US store.

2. Preprocess the scraped reviews - convert to pandas DataFrame, extract key fields like review text, score, username etc. 

3. Perform sentiment analysis on the review text using the `transformers` library. Specifically, the `pipeline` for sentiment analysis is used with the pre-trained RoBERTa model. This returns the predicted sentiment (positive/negative) and score for each review.

4. Analyze the sentiment output - calculate averages, plot histograms etc. to see distribution of positive/negative reviews.

## Code Overview

The main steps in the code are:

- Import libraries: pandas, numpy, google_play_scraper, transformers, plotly
- Scrape reviews into a dict using `reviews_all()`
- Convert dict to DataFrame 
- Print sample rows to inspect data
- Calculate average review score
- Plot histogram of sentiment values
- Create sentiment analysis pipeline with RoBERTa model
- Apply pipeline to review text to get sentiment predictions 
- Extract sentiment and score into separate columns
- Analyze sentiment distribution, print mean scores
- Plot histogram of sentiment values

## Results

- The average review score is 3.75 out of 5 
- 66.5% of reviews are positive in sentiment, 33.5% are negative
- The average sentiment score is 0.997 (close to max of 1), indicating strong confidence in sentiment classification
- The histogram plots show the distribution of positive vs negative reviews

## Conclusion

This analysis provides a good overview of user sentiment based on app reviews. The majority of reviews are positive, but there is a significant minority of negative reviews. Further analysis could dig into the specific app issues mentioned in negative reviews.
