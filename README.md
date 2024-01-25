# Overview

This project utilizes text analytics techniques to transform unstructured data into actionable market insights. The aim is to identify the top automotive brands and their main rivals in the market by analyzing user comments using a bag-of-words model. To achieve this goal, user comments are gathered from Edmunds. Also, we want to discover the most important decision criteria for people when choosing a car. We also want to know how these decision criteria are associated with the most popular brands. Lastly, we try to identify the most aspirational brand, which is associated with the most positive sentiments among the customers.

The following libraries are used in this project:

- Numpy
- Pandas
- NLTK


# Data Preprocessing

The first step is to clean the corpus by eliminating unnecessary parts of the text. To do so, part of speech tags are extracted. Then, punctuations and stopwords are removed and all the tokens are converted to lowercase characters. Finally, tokens are lemmatized, which prepares the data for analysis.


# Findings

In this project, the frequency of users discussing a brand is considered as the indicator of popularity. 

## Top Brands:

The top brands based on their frequency of being mentioned by users are found to be 'BMW', 'Audi', 'Acura', 'Lexus', and 'Infiniti'. It is worth noting that the word 'seat' appears more than 'Lexus' and 'Infiniti' brands but since this analysis cannot ensure whether the user is referring to the brand 'SEAT' or car seats, this item is not considered. 

## Main Rivals:

Also, the top rivals identified are Audi-BMW, Audi-Acura, and BMW-Acura, which shows people compare these brands with each other more frequently according to the data.

## Main Decision Criteria:

According to the results, it can be concluded that the most mentioned attributes of cars in the discussion are time, price, years, dealer, miles, and sport. It can be concluded that years and miles refer to durability, time refers to comfort, dealer refers to maintenance/post-sales service, and sport refers to the car style.

## Association between Brands and Attributes:

According to the test results, it seems the word 'years' is not co-mentioned with our top brands despite being among the most frequent words in the whole dataset.

## The Most Aspirational Brand

To find the most aspirational brand, I will extract positive comments and analyze them. The most mentioned brand in positive comments would be the most aspirational brand for people to buy or own. I did some experiments with SentimentIntensityAnalyzer and it seems positive sentences usually have a compound polarity score of more than 0.5. The compound polarity score may exceed 0.6 for very positive sentences. Therefore, I will extract comments with a compound polarity score of more than 0.6 and look for the most mentioned brands in those comments. According to the results, 'BMW' is the most aspirational brand for people to buy or own.


# Conclusion

From a marketing perspective, the more a brand is mentioned, the more it is mentioned with the most mentioned attributes. It can be hypothesized that more popular brands put more effort into attributes that matter to customers. In other words, identifying customer needs and focusing on them can help a brand become more popular. Also, analyzing the ratio of a brand's mentions in positive comments to its overall mentions can help segment the market and identify competitors.
