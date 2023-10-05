[Didact AI - Features](https://principiamundi.com/posts/didact-anatomy/)

Raw Features Extracted from Feature Groups
- Price/volumes
- Options chains
- Sentiment extracted from text data

Basic Feature Engineering
- Measure of where closing price was in relation to overall range established for the day
- Scores of other features computed

Contextualization and Normalization
- Comparison against peers in same sector, industry, index or exhibited co-ownership pattern
- Percentiles and other measures computed

Prior History Contextualization
- Closing price compared against last year's closing price
- Percentiles, ratios, standard deviation, skew, and kurtosis computed on rolling window basis

Cross-Group Features
- Price-to-sales
- Price delta over sentiment delta, etc.

Trading Strategy-Based Features
- Technical analysis
- Momentum/trend following
- Value
- Quality
- Low volatility
- Skew
- Glamor
- Predictions captured as features

Market Regime-Based Features
- VIX term structure
- S&P 500's current position w.r.t. 200-day moving average
- Shape of US yield curve
- Realized trajectories of macroeconomic releases (unemployment, housing starts, etc.)

Financial Data Complexity
- Multi-modal (text, time series, implicit network graphs)
- Options datafeed (bids/asks, volumes, open interest, implied volatility, etc.)

Corporate Changes
- Name change, ticker change, stock split, reverse split, spinoff, merge, acquisition, etc.
- Tooling to track and trace changes
- Rich sources of informative features

Index Reconstitution
- Announced in advance for major indices (S&P 500, Russell 1/2/3000 series)
- Triggers massive capital flows in and out of specific stocks, sectors, and industries
- Marginal alpha to be obtained by capturing events as informative features

Important Dates to Track
- Federal Reserve FOMC meetings
- Holidays
- Options and futures expiry days
- Macro-economic releases

Earnings Call Transcripts and EDGAR Filings
- Text-based and amenable to analysis by SOTA language models
- Crucial insights about corporate officers' uncertainty around future prospects
- Changes and variance in topics, word frequencies, and sentiment
- Aggregate features useful for indicating better-than-average market performance
{% endplantuml %}

