# Real-Time Social Media Sentiment Analysis Dashboard

An end-to-end NLP and data visualization pipeline designed to monitor, clean, and quantify public sentiment from text streams in real time.

## Overview
This application extracts short-form text streams, cleans raw input via regex-based natural language preprocessing, and scores emotional polarity using the VADER (Valence Aware Dictionary and sEntiment Reasoner) lexicon. The results are rendered in an interactive dashboard featuring key metrics, distribution donut charts, polarity histograms, and tabular text feeds.

## Features
* **Automated Text Preprocessing:** Strips URLs, usernames, hashtags, punctuation, and non-alphanumeric noise using regular expressions.
* **Lexicon-Based Sentiment Scoring:** Computes positive, negative, neutral, and normalized compound polarity scores ($[-1.0, 1.0]$).
* **Interactive Visualization:** Dynamic Plotly charts and Streamlit interface with customizable search queries and sample sizes.
* **Dual Execution Modes:** Supports live API ingestion (Twitter/X API v2) alongside built-in simulation fallback and custom CSV dataset uploads to prevent service disruption from rate limits.

## Tech Stack
* **Language:** Python 3.9+
* **NLP & Text Analytics:** NLTK (VADER Lexicon), RegEx
* **Data Manipulation:** Pandas, NumPy
* **Visualization & Web Interface:** Streamlit, Plotly Express
* **API Integration:** Tweepy

## Repository Structure
```text
├── app.py                 # Streamlit application and NLP pipeline
├── requirements.txt       # Project dependencies
└── README.md              # Project documentation