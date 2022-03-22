# Ten-Things-I-Hate-About-You-Script-Analysis

# Required Packages 

```
library(tidyverse)
library(tidytext)
library(textdata)
library(ggwordcloud)
library(here)
library(readr)
library(tidymodels)
library(textrecipes)
library(topicmodels)
library(tm)
library(tictoc)
library(stringr)
library(themis)
library(vip)
library(stopwords)
```


# Summary

## Background 

### Data

This repo is performed using Cornell University's [Movie Dialogue Corpus](https://www.kaggle.com/Cornell-University/movie-dialog-corpus/code), which contains data from movie scripts. Within this repo, I have included all of the data sets from this corpus. However, for this analysis, I only used the following two data sets, which can be found in the data folder within this repo:

* [Movie Titles](./data/movie_titles_metadata.tsv)
* [Movie Lines](./data/movie_lines.tsv)

For this analysis, I am only analyzing the film 10 Things I Hate About You, which is one of many in the corpus. However, similar analyses can be conducted on any film in the corpus.  

## Part 1: [Sentiment Analysis](./Sentiment_Analysis.md) 

In the first part of this repo, I conduct a text analysis on the film, investigating most frequently used words by character and sentiment. I use the following two dictionaries to complete this sentiment analysis:

* Bing dictionary
* AFINN dictionary 


## Part 2: [Topic Modeling](./Tenthingsihateaboutyou_Topic_Modeling.md)

In the second part of this, I analyze the script of 10 Things I Hate About You for topic using Latent Dirichlet allocation. While I don't find dramatically clear topics, you can start to get a sense for what the film is about from the topic modeling. 


## Part 3: [Predicting Characters Based On Lines](./Character_predictions.md)

In this last part, I attempt to predict characters based on their lines. Using a random forest model, I perform the prediction first on all of the characters, then on the four main characters. In the end, the predictions are pretty inaccurate. For the first model, the accuracy is around 7% and only increases to around 30% in the second model. I conclude that the inaccuracy comes from two different limitations: firstly, this is a small data set for machine learning. Accurate machine learning requires lots of data. Secondly, the nature of the script does not lend to the task at hand. The characters talk about the same topics throughout this film, so there is likely not enough differentiation between each character's lines to know who's line it is using this type of model. 


# Useful Resources 

* [Topic Modeling Guide](https://cfss.uchicago.edu/notes/topic-modeling/#perplexity)
* [Movie Dialog Corpus](https://www.kaggle.com/Cornell-University/movie-dialog-corpus/code)
* [Sentiment Analysis Guide](https://cfss.uchicago.edu/notes/harry-potter-exercise/)
* [Predicting Song Artist from song lyrics](https://cfss.uchicago.edu/notes/predicting-song-artist/)