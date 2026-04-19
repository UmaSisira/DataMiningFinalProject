# Wikipedia Traffic and Consumer Sentiment Analysis

This project investigates the relationship between public interest in specific crisis-related topics (measured via Wikipedia pageviews) and consumer confidence (measured by the University of Michigan Consumer Sentiment Index).

## Repository Contents

### Analysis & Documentation
* **DataMining_FinalReport.pdf**: A comprehensive three-page report detailing the project's title, methodology, key findings, and significance.
* **DataMining_FinalSlides.pptx**: Presentation slides summarizing the research goals, data visualizations, and conclusions.
* **README.md**: This file, providing an overview of the project and its components.

### Code & Data
* **Data_Mining_Final.ipynb**: A Jupyter Notebook containing the full analytical pipeline, including data fetching, cleaning, normalization, and correlation analysis.
* **UMCSENT.csv**: The raw dataset for the University of Michigan Consumer Sentiment Index (sourced from FRED).
* **DataMiningFinalFigure.jpg**: The primary small-multiples visualization showing Wikipedia views versus consumer sentiment across seven categories.

### Tracked Wikipedia Articles
The analysis focuses on traffic data from the following English Wikipedia articles:
* [Pandemic](https://en.wikipedia.org/wiki/Pandemic)
* [War](https://en.wikipedia.org/wiki/War)
* [Donald Trump](https://en.wikipedia.org/wiki/Donald_Trump)
* [Inflation](https://en.wikipedia.org/wiki/Inflation)
* [Recession](https://en.wikipedia.org/wiki/Recession)
* [Unemployment](https://en.wikipedia.org/wiki/Unemployment)
* [Anxiety](https://en.wikipedia.org/wiki/Anxiety)

## Key Methodology
1. **Smoothing**: Applied a 7-day rolling mean to Wikipedia views to remove weekend variance.
2. **Normalization**: Min-max scaling (0-1) to allow comparison across topics with different traffic scales.
3. **First-Differencing**: Calculated month-over-month changes to isolate short-term co-movements (delta-r).
4. **Correlation**: Analyzed the Pearson correlation between monthly changes in view counts and sentiment scores.

## Main Findings
* **Inflation** showed the strongest "panic signal" with a delta-r of -0.28, indicating that as views for inflation spike, consumer sentiment reliably drops.
* **Economic topics** (Inflation, Recession, Unemployment) demonstrate a more consistent signal than political or baseline topics
