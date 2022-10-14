# Objective

Use Twitter data about the Pennsylvania Senate race between Dr. Mehmet Oz and John Karl Fetterman to evaluate the trend in sentiment for each of these Senate candidates.


# Implementation

- We use snscrape to get Tweets and Comments from August 1 - October 6. This data does not contain Retweets. This is done in **DataGathering.ipynb**.

- Given the JSON's, two separate datraframes were created one for Fetterman, Oz. These datasets are filtered with tweets containing only English, removing duplicate tweets, removing tweets than contain keywords oz and fetterman etc. This is implemented in **DataPreprocess.ipynb**.

- In **DataClassificationOz.ipynb** and **DataClassificationFetterman.ipynb**, sentiments are computed for every tweets in their respective dataframes computed in **DataPreprocess.ipynb**. The sentiment indicators are computed using *VADER SentimentAnalyzer*, *TextBlob*, and *BERTTweetSentimentAnalysis*. 

- In **DataInterpretation.ipynb**, after training and predicting the sentiments based on the *VADER SentimentAnalyzer* and *BERTTweetSentimentAnalysis*,plots are geenerated for observing changes in twitter user sentiment data over time for the whole dataset,  for tweets with (!) marks, for users with relatively high number of followers etc. 
