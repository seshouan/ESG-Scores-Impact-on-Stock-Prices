# Understanding the Impact of ESG Scores on Stock Prices: A Perspective for Millennials and Gen Z

### TEAM: Dov Lantsman, Neelansh Kohli, Session Mwamufiya, Tracy Ejiogu

## I. OBJECTIVE/ OVERVIEW: 

The aim of this project is to examine the correlation between Environmental, Social, and Governance (ESG) scores and the stock performance of leading Fortune 500 companies in the tech space. Our study will compare multiple categories of ESG scores and the stock price performance of their associated tickers, to determine whether these companies’ ESG performance was reflected in their market performance, and thus conclude whether ESG performance is a significant "non-financial factor" in investment decision-making, which are more widely considered by younger generations of investors (Millennials and Gen Z).<br>

It is important to note that the practice of socially responsible investing is not a novice idea, dating back to the 1960s and 1970s in response to societal concerns about issues such as the Vietnam War, apartheid in South Africa, and environmental damage. Our goal with this project is to observe and present whether higher ESG scores lead to better financial performance, measured by stock prices and returns. For Millennials and Gen Z, considering ESG scores in their investment decisions could prove beneficial in achieving their financial goals without compromising their personal convictions on ESG concerns.

## II. DATA SOURCES

* ESG Scores: we will use the free ESG dataset available on Kaggle to pull multiple categories of ESG scores for our target companies.
* Stock Prices: we will download historical stock prices for our target companies using the yfinance apis, and will select a time period that matches that of the available ESG scores.
 
## III. METHODOLOGY

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

## IV. ANTICIPATED CHALLENGES
As we conduct this project, we anticipate facing the following potential limitations or challenges, for which we will make appropriate assumptions to progress through our analysis:
* The relationship between ESG scores and stock performance is complex and may be influenced by a variety of factors that the available data doesn’t allow us to isolate
* The data may be lacking the right level of granularity to observe enough discrete changes of ESG scores and their related impact
* The timeframe covered may not be representative of a period in which ESG performance was a significant “non-financial factor” driving stock performance
* While we might find some correlations, it is important to remember that correlation does not imply causation

## V. DELIVERABLES:

The list of deliverables, detailed in section III, will be contained and thoroughly documented in the following outputs:
* A Jupyter Notebook containing all analysis steps, assumptions, and their results
* PNG images of the visualizations as references
* A README.md file summarizing the key findings from our analyses, as well as implications from these findings and potential recommendations

## VI. ANALYSIS RESULTS:

We observed from the ticker returns distributions that:
* 
* 
* 

We observed from the ESG data distribution that:
* 
* 
* 

We observed from the ticker returns and ESG data overlays that:
* 
* 
* 

We observed from the ticker returns and ESG data correlations that:
* 
* 
* 

## VII. RECOMMENDATIONS:

As a result of our analyses, we recommend the following course of actions for companies and investors alike:
* 
* 
* 
* 
