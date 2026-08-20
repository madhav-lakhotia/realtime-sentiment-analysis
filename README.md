
# Real-Time Social Media Sentiment Analysis Dashboard

An end-to-end NLP and data visualization pipeline designed to monitor, clean, and quantify public sentiment from text streams in real time.

## Overview
This application extracts short-form text streams, cleans raw input via regex-based natural language preprocessing, and scores emotional polarity using the VADER (Valence Aware Dictionary and sEntiment Reasoner) lexicon. The results are rendered in an interactive dashboard featuring key metrics, distribution donut charts, polarity histograms, and tabular text feeds.

## Features
* **Automated Text Preprocessing:** Strips URLs, usernames, hashtags, punctuation, and non-alphanumeric noise using regular expressions.
* **Lexicon-Based Sentiment Scoring:** Computes positive, negative, neutral, and normalized compound polarity scores (from -1.0 to 1.0).
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

```

## Installation & Setup

1. **Clone the repository:**
```bash
git clone [https://github.com/](https://github.com/)<your-username>/realtime-sentiment-analysis.git
cd realtime-sentiment-analysis

```


2. **Create a virtual environment (optional but recommended):**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

```


3. **Install dependencies:**
```bash
pip install -r requirements.txt

```


4. **Launch the Dashboard:**
```bash
streamlit run app.py

```



## Methodology

1. **Data Ingestion:** Captures text queries dynamically via live APIs, simulation streaming, or batch CSV uploads.
2. **Text Normalization:**
```text
Raw Text -> Regex Noise Removal -> Token Standardization -> Cleaned Text

```


3. **Sentiment Classification:**
* Compound Score >= 0.05 -> **Positive**
* Compound Score <= -0.05 -> **Negative**
* -0.05 < Compound Score < 0.05 -> **Neutral**


4. **Visual Analytics:** Real-time updates rendered directly via Streamlit and Plotly components.

```

```
