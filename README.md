# ds_abhay_rawat.
Data Science Submission: Web3 Trading Team Analysis

Candidate: Abhay Rawat

This submission contains the complete analysis required for the Data Science Assignment, focusing on the relationship between trading behavior and the Bitcoin Fear & Greed Index (FGI).

Core Finding

The analysis confirms a strong contrarian signal: The observed trader cohort achieves nearly three times higher average daily profitability and exhibits the highest trading volume during periods when the market is classified as Fear. This finding advocates for a strategy that proactively increases exposure during times of extreme market instability.

Submission Structure

The repository strictly follows the mandated structure:

ds_abhay_rawat/
├── ds_report.pdf                      # Final summarized insights and strategic recommendations (2 pages).
├── notebook_1.ipynb                   # The Google Colab notebook containing all Python code.
├── historical_data.csv                # **[NOTE: File Excluded due to GitHub Size Limit (> 25MB)]**
├── fear_greed_index.csv               # Raw Input File 2
├── csv_files/
│   └── merged_trader_sentiment_data.csv   # Intermediate processed data, merging daily metrics with sentiment.
└── outputs/
    ├── mean_daily_pnl_by_sentiment.png    # Visual evidence of profitability divergence.
    └── total_volume_by_sentiment.png      # Visual evidence of activity/volume alignment.


🚨 IMPORTANT NOTE REGARDING historical_data.csv

The raw file historical_data.csv exceeds GitHub's maximum file size limit (25MB+). It has been omitted from this repository.

To access this file, please use the original Google Drive link provided in the assignment instructions:
https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing

The code in notebook_1.ipynb successfully accesses this file via the Colab environment, where the analysis was performed.

Code and Methodology

1. Code Environment

All code was executed in Google Colab and is contained within notebook_1.ipynb.

The code successfully handles two common errors/warnings:

Date Parsing: Uses pd.to_datetime(..., errors='coerce') to handle malformed timestamps in the raw data.

DtypeWarning: Uses low_memory=False to suppress the mixed-type column warning upon loading historical_data.csv.

2. Analysis Steps

Aggregation: Granular transaction data was aggregated daily to calculate Total PnL, Total Volume, and Unique Traders.

Standardization: F&G classifications were standardized into Fear, Greed, and Neutral categories.

Integration: The daily trader metrics were merged with the FGI sentiment data on the common date column.

Comparison: Final metrics (e.g., Mean Daily PnL) were grouped by the standardized sentiment category to derive the core findings.
