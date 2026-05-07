# Reddit Stock Sentiment Analysis

This project analyzes Reddit comments to find frequently mentioned stock tickers and estimate sentiment around them using VADER sentiment analysis.

## Project Objective

The goal is to collect recent Reddit discussion from selected finance-related subreddits, detect stock ticker mentions, count the most discussed symbols, and calculate a basic bearish/neutral/bullish sentiment score for the top tickers.

## Tech Stack

- Python
- PRAW for Reddit API access
- Pandas
- NLTK VADER
- spaCy
- Matplotlib
- Squarify

## Repository Structure

```text
.
├── reddit-sentiment-analysis.py
├── data.py
├── list of subreddits.csv
├── requirements.txt
├── mentioned.png
├── sentiment.png
└── README.md
```

## Features

- Connects to Reddit using PRAW
- Reads posts and comments from selected subreddits
- Finds uppercase stock ticker symbols
- Counts most mentioned tickers
- Applies VADER sentiment scoring
- Creates visual summaries for mentions and sentiment

## Setup

Install dependencies:

```bash
pip install -r requirements.txt
python -m nltk.downloader vader_lexicon stopwords wordnet
python -m spacy download en_core_web_sm
```

Configure Reddit API credentials in `data.py` before running the script.

Run:

```bash
python reddit-sentiment-analysis.py
```

## Important Notes

- Reddit API credentials are required.
- Sentiment analysis is rule-based, so sarcasm and slang may not be detected correctly.
- This is a learning project and should not be used as financial advice.

## What I Learned

- How to use an external API from Python
- How to clean and tokenize text
- How dictionary/set lookups help detect ticker symbols efficiently
- How sentiment scoring works at a basic level
- How to convert raw text data into summary charts

## Future Improvements

- Move configuration values out of the main script
- Add command-line arguments for subreddit and post limits
- Save results to CSV
- Add better error handling for API failures
- Add tests for ticker extraction and text cleaning

