# Sentiment Analysis and Stock Price Prediction 

## Overview

This project investigates the relationship between public sentiment and stock prices. By leveraging sentiment analysis on news headlines and financial data, we aim to develop a predictive model that could inform trading decisions. The project includes data collection, sentiment analysis, stock data retrieval, sentiment-adjusted moving averages, signal generation, and performance evaluation.

## Project Structure

- `data/`: Directory containing collected datasets and preprocessed data.
- `notebooks/`: Jupyter notebooks for data exploration, sentiment analysis,and model training.
- `scripts/`: Python scripts for web scraping, data preprocessing, and sentiment analysis.
- `models/`: Directory for saving trained models and relevant outputs.
- `results/`: Directory for storing evaluation metrics, visualizations, and final results.

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/sentiment-stock-prediction.git
   cd sentiment-stock-prediction
   ```

2. Create a virtual environment and install dependencies:
   ```sh
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

3. Set up necessary API keys:
   - **New York Times API Key**: Sign up for a key at https://developer.nytimes.com/apis.
   - **Yahoo Finance API Key**: Sign up for a key at https://www.yahoofinanceapi.com/.

   Create a `.env` file in the root directory and add your API keys:
   ```sh
   NYT_API_KEY=your_nyt_api_key
   YAHOO_FINANCE_API_KEY=your_yahoo_finance_api_key
   ```

## Usage

### Data Collection

1. **Scrape News Headlines**: Use Selenium to scrape news headlines from Yahoo Finance.
   ```sh
   python scripts/scrape_yahoo_finance.py
   ```

2. **Fetch Articles from New York Times**: Use the New York Times API to fetch articles related to the stock.
   ```sh
   python scripts/fetch_nyt_articles.py
   ```

### Sentiment Analysis

1. **Analyze Sentiment of Headlines**: Use VADER sentiment analysis to score news headlines.
   ```sh
   python scripts/sentiment_analysis.py
   ```

### Stock Data Retrieval

1. **Fetch Stock Data**: Use Yahoo Finance API to retrieve stock price data.
   ```sh
   python scripts/fetch_stock_data.py
   ```

### Data Integration

1. **Merge Sentiment and Stock Data**: Combine sentiment scores with stock data for analysis.
   ```sh
   python scripts/merge_data.py
   ```

### Model Training and Evaluation

1. **Train Sentiment Prediction Model**: Train a Random Forest classifier to predict sentiment from headlines.
   ```sh
   python scripts/train_sentiment_model.py
   ```

2. **Generate Trading Signals**: Create trading signals based on sentiment-adjusted moving averages.
   ```sh
   python scripts/generate_signals.py
   ```

3. **Evaluate Trading Strategy**: Assess the performance of the trading strategy.
   ```sh
   python scripts/evaluate_strategy.py
   ```

### Visualization

1. **Visualize Results**: Plot stock prices, sentiment scores, buy/sell signals, and portfolio value.
   ```sh
   python scripts/visualize_results.py
   ```

## Results

The results, including performance metrics, visualizations, and final evaluation, are stored in the `results/` directory. Key metrics include the Sharpe Ratio, win ratio, and overall portfolio value.


