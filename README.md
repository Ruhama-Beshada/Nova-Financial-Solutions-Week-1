# Nova Financial Solutions – Stock & News Analysis Project

Welcome to the Nova Financial Solutions Stock and News Analysis project. This repository explores the relationship between stock price movements and financial news sentiment, along with technical analysis using commonly applied indicators. The work is divided into **three major tasks** that together provide a complete framework for understanding stock behavior, predicting trends, and analyzing market signals.

---

## **Project Overview**

The goal of this project is to enhance predictive analytics for stock prices by combining **technical indicators** and **news sentiment analysis**. By understanding both historical stock trends and market sentiment, we can gain insights into price movements and make better-informed trading decisions.

The dataset includes historical stock prices for six major companies: **AAPL, AMZN, GOOG, META, MSFT, and NVDA**, as well as a collection of financial news headlines with publication dates.

---

## **Task 1: Data Loading and Preparation**

In Task 1, we focused on **loading, cleaning, and structuring our raw data**:

* **Stock Data:**

  * Loaded CSV files for each stock into Pandas DataFrames.
  * Converted `Date` columns to datetime and sorted data chronologically.
  * Kept essential columns for analysis: `Date` and `Close` prices (other columns like Open, High, Low, and Volume were retained for future expansions).

* **News Data:**

  * Loaded raw analyst ratings and news headlines.
  * Cleaned and standardized dates.
  * Removed invalid entries and kept only the date portion for easier alignment with stock data.

This task ensured a **consistent, clean dataset** for all subsequent analyses.

---

## **Task 2: Technical Indicator Analysis**

Task 2 focused on **analyzing stock trends using technical indicators**:

* **Indicators Calculated:**

  * Short-term and long-term moving averages (`SMA_20` and `SMA_50`)
  * Relative Strength Index (`RSI_14`)
  * Moving Average Convergence Divergence (`MACD`)

* **Analysis Performed:**

  * Correlation matrices computed for all numeric features, focusing on relationships with the `Close` price.
  * Visualizations included scatter plots and heatmaps to identify trends and momentum.
  * Signals derived from RSI were flagged as potential buy or sell points.
  * SMA crossovers were explored as potential trend indicators.

* **Key Insights:**

  * SMAs (short-term and long-term) reliably reflect price trends, with SMA_20 often leading price movement.
  * RSI and MACD are more suitable for identifying momentum shifts or overbought/oversold conditions rather than predicting daily prices.
  * Combining multiple indicators gives a more robust view of potential trend reversals and market movements.

This task provided **strong foundation for trend analysis** and practical insights for trading strategies.

---

## **Task 3: Sentiment Analysis and Correlation with Stock Returns**

Task 3 explored **the impact of financial news sentiment on daily stock returns**:

* **Sentiment Scoring:**

  * Used TextBlob to compute polarity scores for all headlines (`-1` = negative, `+1` = positive).
  * Aggregated daily sentiment by averaging multiple headlines for the same day.

* **Stock Returns:**

  * Calculated daily percentage change for each stock's closing price.
  * Merged daily stock returns with daily news sentiment to align data chronologically.

* **Analysis and Visualizations:**

  * Scatter plots show the relationship between daily returns and sentiment scores.
  * Pearson correlation coefficients computed for each stock to quantify alignment with news sentiment.
  * Bar charts visualized which stocks were more or less sensitive to news headlines.

* **Key Insights:**

  * Most stocks show **weak to moderate correlation** between news sentiment and daily returns.
  * Some stocks are slightly more sensitive to news, but market factors beyond headlines often dominate short-term price movements.
  * Sentiment analysis alone has limited predictive power but is **valuable when combined with technical indicators**.

---

## **Overall Observations and Recommendations**

1. **Combining Indicators and Sentiment:**
   Using SMA, MACD, RSI, and news sentiment together provides a **multi-dimensional view of the market**.

2. **Stock-Specific Strategies:**
   Stable stocks (like AAPL, MSFT) often show smoother SMA trends, making technical indicators more reliable.
   Volatile stocks (like NVDA, META) may require adaptive strategies incorporating momentum indicators and sentiment signals.

3. **Future Work:**

   * Incorporate additional technical indicators such as Bollinger Bands or stochastic oscillators.
   * Explore advanced sentiment analysis using NLP models beyond TextBlob (e.g., transformers or finBERT).
   * Build predictive models combining both technical and sentiment features for algorithmic trading simulations.

---

## **Conclusion**

This repository demonstrates a structured approach to **financial data analysis**, combining historical stock trends with textual news sentiment. Through clear preprocessing, careful calculation of technical indicators, and correlation analysis, we gain **actionable insights** into stock behavior. While sentiment analysis provides limited predictive power on its own, it complements technical analysis to improve forecasting and trading strategies.

---

## **Tools & Libraries Used**

* Python (Pandas, NumPy, Matplotlib, Seaborn)
* TextBlob for sentiment analysis
* Git for version control

---

This README encapsulates the **full workflow from raw data ingestion to analysis and insights**, giving a comprehensive, human-readable summary of the project.

