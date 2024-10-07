# Project Week 3

<h1>Covid 19 and the Stock Market<h1>
  
<h2>Introduction<h2>
This project aims to research the impact of the COVID-19 pandemic on the stock markets in the United States and Germany. By analyzing stock prices from key companies in these countries and comparing them with the progression of the pandemic, we seek to identify trends and correlations between COVID-19 cases and stock market performance.

<h2>Data Overview<h2>
  
1. COVID-19 Data
The dataset used for this project is sourced from Kaggle's COVID-19 Cases Daily Updates. This dataset provides daily updates on all confirmed cases and deaths of Coronavirus (COVID-19) across all countries. The data is collected primarily from the World Health Organization's (WHO) Coronavirus Dashboard and is updated daily. Additional information regarding hospitalizations, ICU admissions, testing, and vaccinations is sourced from the Our World in Data team.

Strengths:
Comprehensive global coverage with daily updates on COVID-19-related metrics.
Data is sourced from trusted organizations like WHO and Our World in Data.

Weaknesses:
Delays in reporting can result in discrepancies between actual cases and reflected data.
Some regions may report data with delays, causing spikes that do not reflect daily trends accurately.

Challenges:
Adjusting for missing data and delayed reports in the daily COVID-19 dataset.
Ensuring that the data is aligned properly when aggregating to a weekly format.

2. Stock Market Data (via Yahoo Finance API)
The second dataset was pulled using the Yahoo Finance API, containing stock tickers for S&P 500 companies in the U.S. and the 100 largest German companies. The data spans from the start of the COVID-19 pandemic until now. The stock data was then grouped by sectors (e.g., Aviation, Defense) to investigate sector-specific trends.

Strengths:
Provides real-time and historical data for major U.S. and German companies.
Allows for sector-based analysis, enabling more granular insights.

Weaknesses:
Companies delisted or merged during the pandemic may result in data gaps.
Historical stock data may be incomplete for companies that exited the indices during the pandemic.

Challenges:
Addressing missing or incomplete data for delisted companies.

<h2> Research Questions <h2>
Question 1:
Hypothesis: COVID-19 outbreaks had a negative impact on the stock markets in both the United States and Germany.

Conclusion: Falsified. No negative correlations were found for the overall stock markets. Negative effects were observed in specific industries, likely due to the diversified nature of the stock market, where losses in some sectors were offset by gains in others.
Question 2:
Hypothesis: COVID-19 had a greater impact on the U.S. stock market compared to the German stock market.

Conclusion: Falsified. Stronger correlations were observed between COVID-19 variables and stock prices in Germany than in the U.S. One possible reason is that the U.S. market is broader, with a larger proportion in tech stocks, which were less affected or even positively impacted by the pandemic.
Question 3:
Hypothesis: Different industries were affected by COVID-19 to varying degrees.

Conclusion: Confirmed. There were clear variations in how different industries responded to COVID-19, with some industries (e.g., Aviation, Defense) being more affected than others.
Question 4:
Hypothesis: The effects of COVID-19 on the stock market varied between years.

Conclusion: Confirmed. Correlations between COVID-19 variables and stock prices varied across years, although some differences were small (e.g., Germany 2020-2024 vs. 2021-2022). As the pandemic progressed, the perceived risk shifted, leading to differing market reactions to new cases over time.


<h2> Methodology <h2>
  
Data Selection
We identified key variables (e.g., new cases, vaccinations, ICU patients) that could impact the stock market and focused on those for the analysis.

Date Alignment & Merging DataFrames
We standardized the dates using Python's dt functions, aggregated daily data into weekly values, and created a yearly_weekly column to merge datasets that spanned multiple years.

Outlier Handling
We applied the z-score function to handle outliers in the data.

Sectoral Grouping & Correlation Analysis
We grouped the data by sector and yearly_weekly, then performed basic exploratory data analysis (EDA) to find correlations between stock performance and COVID-19 variables.

Tools and Libraries Used

pandas for data manipulation
matplotlib and seaborn for visualization
requests for the Yahoo Finance API
numpy for numerical computations

<h2>Conclusions<h2>

Overall Market Impact: COVID-19 did not have a uniformly negative effect on the U.S. or German stock markets. Specific industries were more affected, but overall market diversification helped offset losses.

National Market Differences: Stronger correlations between COVID-19 variables and stock prices were observed in Germany than in the U.S. This difference may be due to the broader scope of the U.S. market, particularly its large tech sector.

Sectoral Variation: Different industries were impacted to varying degrees. Sectors like aviation and defense were more affected, while the tech industry remained resilient.

Temporal Variation: The effects of COVID-19 varied across different years, with the most significant impacts seen early in the pandemic. Market reactions changed as the perceived risk of COVID-19 evolved.


<h2>Further Questions<h2>
  
Can a causal relationship be established between COVID-19 and stock price fluctuations through techniques like Granger causality tests?
What are the long-term effects of COVID-19 on industries like aviation and biotechnology?
How did investor sentiment evolve throughout the pandemic, and what role did it play in driving stock price trends?
Could we use similar methods to study the stock market's response to future global crises?

Links
Kaggle Dataset on COVID-19 Cases
Presentation: https://docs.google.com/presentation/d/1licqptrShY0f9w1tirYdT3Q6B3lnwadz6XmNYHd5qSA/edit?usp=sharing


