# leverage-sentiment-analysis
MLH Local Hack Day: Build 2021 Day 2 Challenge: Leverage Sentiment Analysis

## Task Statement
Using Sentiment analysis can come in handy for many types of hacks from understanding how customers view a product to determining effective ways of communicating with your audience. Explore this topic and Submit your hack on our Day 2 Devpost!

# Submission
Simple scripts for scraping sites and performing sentiment analysis in Python using Vader, the Natural Language Toolkit (NLTK) and TextBlob.

## Getting Started
Install the code's dependencies:
`pip install -r requirements.txt`

## Scrape a Website
Input urls you'd like to scrape in the urls.txt file, then run scrape.py:
`python scrape.py`
The script will save the text it scrapes as .txt files in the project's directory. The script searches for `<p>` tags by default, but what it looks for can easily be edited in the .py file. Just change the line `paragraphs = soup.find_all('p')` to search for things other than "p".
  
## Perform Sentiment Analysis
Open python, import sentiment.py, and perform sentiment analysis on your texts using [Vader](https://www.nltk.org/_modules/nltk/sentiment/vader.html), NLTK's [Naive Bayes classifier](https://www.nltk.org/_modules/nltk/classify/naivebayes.html), or TextBlob. The training sentences for the Naive Bayes classifier can easily be swapped out for your own. 
```
>>> python
>>> from sentiment import Sentiment
>>> Sentiment.vader('your_filename.txt')
>>> [sentiment analysis of your text]
```
for the Naive Bayes classifier:
```
>>> python
>>> from sentiment import Sentiment
>>> Sentiment.naive('your_filename.txt')
>>> [sentiment analysis of your text]
```
or for TextBlob:
```
>>> python
>>> from sentiment import Sentiment
>>> Sentiment.blob('your_filename.txt')
>>> [sentiment analysis of your text]
```
