# Understanding the Impact of ESG Scores on Stock Prices: A Perspective for Millennials and Gen Z

### TEAM: Dov Lantsman, Neelansh Kohli, Session Mwamufiya, Tracy Ejiogu

## I. OBJECTIVE/ OVERVIEW: 

The aim of this project is to examine the correlation between Environmental, Social, and Governance (ESG) scores and the stock performance of leading Fortune 500 companies in the tech space. Our study will compare multiple categories of ESG scores and the stock price performance of their associated tickers, to determine whether these companies’ ESG performance was reflected in their market performance, and thus conclude whether ESG performance is a significant "non-financial factor" in investment decision-making, which are more widely considered by younger generations of investors (Millennials and Gen Z).<br>

It is important to note that the practice of socially responsible investing is not a novice idea, dating back to the 1960s and 1970s in response to societal concerns about issues such as the Vietnam War, apartheid in South Africa, and environmental damage. Our goal with this project is to observe and present whether higher ESG scores lead to better financial performance, measured by stock prices and returns. For Millennials and Gen Z, considering ESG scores in their investment decisions could prove beneficial in achieving their financial goals without compromising their personal convictions on ESG concerns.

## II. DATA SOURCES

* ESG Scores: we will use the free ESG dataset available on Kaggle to pull multiple categories of ESG scores for our target companies.
* Stock Prices: we will download historical stock prices for our target companies using the yfinance apis, and will select a time period that matches that of the available ESG scores.
 
## III. INSTALLATION/ USAGE: 

The analysis file 'ESG stock analysis.ipynb' can be run directly from Jupyter Lab if you clone the git repository of the project, given that there are dependencies with the ESG data found in the Sources folder. Once executed, you may interact directly with the hvplot charts to view different slices of the data.<br>

Alternatively, you can copy the cells of the ipynb file into a python doc and run it if it is in the same repository.

## IV. METHODOLOGY

Our research will be conducted in several stages:

| Activity | Sub-activity | Deliverable | Status |
| :-------- | :------------ | :----------- | ------: |
| Setup [Session] | Create GitHub repository and provide access to all team members | GitHub repository for project | 7/31/23 |
| Collect Data [Dov] | Download ESG data for top technology companies with Kaggle | ESG data from 2010 to 2022 | 8/2/23 |
|  | Download Stock Prices for the target tech companies from yfinance over the covered time period | Stock Prices of target companies | 8/2/23 |
|  | Create a data frame for the ESG scores | Data frame of ESG scores | 8/2/23 |
|  | Create a data frame combining all the tickers’ stock prices | Data frame of target ticker stock prices | 8/2/23 |
| Clean Data [Neelansh] | Add a risk-free return measure (S&P500) to the Stock Price data | Data frame of S&P500 returns over target period | 8/3/23 |
|  | Structure the ESG and Stock Price data frames similarly to facilitate analysis | Restructured ESG and/or Stock Price data frames | 8/3/23 |
|  | Observe ESG data to ensure proper load in data frame, and clean missing information or NAs | Cleaned up data frame of ESG scores | 8/2/23 |
|  | Observe Stock Price data to ensure proper load in data frame, and clean missing information or NAs | Cleaned up data frame of target ticker stock prices | 8/2/23 |
| Analyze Data [Tracy] | Perform a description analysis of the available ESG data to understand the range and spread of the information (including ESG score comparison to returns by ticker) | Summary of data characteristics | 8/3/23 |
|  | Visualize ESG scores vs. Stock Prices for each target ticker over the covered time period | Overlaid graphs of ESG scores and Stock Prices | 8/3/23 |
|  | Perform correlation analysis between overall ticker ESG scores and their corresponding Stock Prices over the covered time period | Correlation heat-map of overall ESG scores and Stock Prices | 8/4/23 |
|  | Perform correlation analysis between sub-categories of ticker ESG scores and their corresponding Stock Prices over the covered time period | Correlation heat-map of sub-categories of ESG scores and Stock Prices | 8/4/23 |
|  | Research potential drivers behind key observations | Updated README.md file | 8/4/23 |
|  | Perform additional analyses and comparisons, if dictated by findings | Updated IPYNB file | 8/4/23 |
| Summarize Findings [Session] | Synthesize report of the analysis results and their implications | Updated README.md file | 8/7/23 |
|  | Provide recommendations for investors or to help improve company performances, based on analysis results | Updated README.md file | 8/7/23 |

## V. ANTICIPATED CHALLENGES

As we conduct this project, we anticipate facing the following potential limitations or challenges, for which we will make appropriate assumptions to progress through our analysis:
* The relationship between ESG scores and stock performance is complex and may be influenced by a variety of factors that the available data doesn’t allow us to isolate.
* The data may be lacking the right level of granularity to observe enough discrete changes of ESG scores and their related impact.
* The timeframe covered may not be representative of a period in which ESG performance was a significant “non-financial factor” driving stock performance.
* While we might find some correlations, it is important to remember that correlation does not imply causation.

## VI. ACTUAL CHALLENGES

When we initiated the project, we quickly ran into a couple of obstacles with the data that we had to overcome in order to complete our analysis:
* Unavailabe year-over-year ticker prices: googlefinance() and yfinance() didn't provide any option to pull yearly ticker prices to match the frequency of returns with that of ESG scores; we pulled daily prices of the entire covered time period, and manipulated the resulting dataframes to retain only the last entry per year, thus providing us yearly price points towards the end of each year, which we used to compute yearly returns.
* Merging ticker price data with ESG data: concatenating ticker return dataframes with their corresponding ESG data for given years ran into a snag at first, and we realized that in the case of the ticker data, the Year column data type was an object whereas the corresponding column for the ESG data whas an Int; converting the dataframes of ticker prices from yfinance() to have Year as an Int data type solved that discrepancy.
* Removing the effects of the market: to obtain a truer performance of a given ticker, we had to remove the effects of the overall market; we determined excess-returns, or alpha, by netting out the returns of the S&P500, which we used as a proxy for the market, over the covered time period.
* Reduce the slew of ESG score categories: the ESG data obtained included over 40 columns of score categories; we scrubbed through the data to determine which columns were the most relevant, and reduce the set to 13 categories for observations.

## VII. DELIVERABLES:

The list of deliverables, detailed in section III, will be contained and thoroughly documented in the following outputs:
* A Jupyter Notebook containing all analysis steps, assumptions, and their results and visualizations.
* A README.md file describing our approach and methodology, summarizing the key findings from our analyses, as well as implications from these findings and potential recommendations.

## VIII. ANALYSIS RESULTS:

We observed from the ticker returns distributions that:
* Tickers like Nvidia and Apple had significantly higher returns than the rest of the pack, and they also had the highest standard deviations; reinforcing the adage that great rewards come at great risk.
* Texas Instrument had the lowest standard deviation, and still outperformed the returns for Oracle and Cisco during the covered period, indicating an overall better performance than those two tickers.

We observed from the ESG data distribution that:
* The overall ESG scores fluctuate less than those of individual categories, as they appear to average them with a specific weighting.
* ESG Controversies scores fluctuate the most, which indicates either inconsistencies in company performances in this category, inaccurate data, or a significant variance in that category between companies and across years.

We observed from the ticker returns and ESG data overlays that:
* There is no visible link between alpha returns (that fluctuate noticeably and ESG scores that remain rather flat over the same time period across all tickers, with the exception of Google who's ESG score consistantly increased from 0.4 to 0.8 over the covered time period
* Nvidia's alpha returns seem disconnected from its ESG scores over the covered period, as the returns experienced significant swings back and forth in the range of -0.25 to 2.5, all the while its ESG score remained rather steady from 0.6 to 0.78

We observed from the ticker returns and ESG data correlations that:
* None of the target tickers' alpha returns showed any significant correlation with ESG scores, as a whole or with any of its composing elements.
* The lack of correlation may be due to a couple of factors: 1) there is truly no correlation between the data, 2) the granularity of the ESG information is too limited to detect significant correlations, or 3) the time period included other economic factors that had much more impact on the returns of these tech stocks than their ESG scores had.

## IX. RECOMMENDATIONS:

As a result of our analyses, we recommend the following course of actions for companies and investors alike:
* The data did not show us much correlation between the excess returns of our target tech stocks and their respective set of ESG scores.
* The lack of correlation may be related to a variety of factors, including an actual lack of correlation, limited granularity of the data masking any relevant correlation, or inaccurate data making it difficult to represent any correlation.
* While there's a current lack of correlation with the tickers selected and the time period covered, we should not disregard ESG scores off hand as potential indicators of market performance, because at present Millenials and Gen Zers may be a relatively small composition of the investor pool, but as their predominence grows, it would be worthwhile to revisit such data to determine whether there is a stronger correlation between ESG scores and company performance.
