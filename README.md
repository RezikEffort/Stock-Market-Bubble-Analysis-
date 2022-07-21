# Stock-Market-Bubble-Analysis-
In this project I looked at the different bubble throughout history to understand the current market



The stock market is a great place to earn money, but it could also be the fastest way to lose money. Billions of dollars get wiped out of the market as fast as they enter. That is why I chose to analyze the stock market bubble to help investors avoid such a risk. A stock market bubble is an economic cycle that is characterized by the rapid escalation of market value. This fast inflation is followed by a quick decrease in value, which is sometimes referred to as a “crash” or a “bubble burst”. We have all heard about the major crashes in history, like the housing market crash in 2008 or the dot com bubble in the 2000s. During these crashes, billions of dollars were wiped out of the market and people lost a lot of money. The goal of this project is to help investors avoid such a crash by studying previous crashes to understand the current market. Bubbles are deceptive and hard to predict. Economists try to predict a bubble by studying previous bubbles and comparing them to the current market. Different economists have different approaches when comparing the current market to previous bubbles. Almost all investors/economists agree that there are five stages of a bubble. In this analysis, we will be using those metrics to understand the current market and determine if we are in a bubble.

To complete this analysis I first had to understand these five stages. According to Investopedia, the 5 stages of a bubble are defined as:

Displacement
This occurs when investors see opportunities caused by the new paradigm. This could be new tech, low-interest rates, and so on.

Boom
In this stage, prices rise slowly at first, following a displacement, but then gain momentum as more and more participants enter the market, setting the stage for the euphoria phase.

Euphoria
During this phase, caution is thrown to the wind, as asset prices skyrocket.

Profit-taking
In this phase, the smart money — heeding the warning signs that the bubble is about at its bursting point — starts selling positions and taking profits

Panic
It only takes a relatively minor event to prick a bubble, but once it is pricked, the bubble cannot inflate again.

In my analysis, I looked in detail at each stage and compared the current market with the previous bubbles to understand if there are similarities.

Data collection

I have gathered different types of data to support my analysis. I collected historical stock market data from 2000 until 2022 from yahoo finance API. The data I collected was the price of major US stock indexes with information about their volume, highs, lows, and adjusted closing price per stock trading day. The second data I collected were economical data that have a major influence on the stock market. These data were consumer price index(CPI), Federal funds rate, and currency in circulation. These economic data were gathered using the federal reserve(FRED) API. All of these data were dated from 2000 until 2022 and stored in a data frame.

Once I have obtained these data I used pandas to clean and filter the data I wanted to include in my analysis. After filtering the data I created a monthly average for each feature and merged them to create one data frame. I used this new data frame to complete my analysis.

Method

I used unsupervised learning techniques to find the K-means clusters. The K-means clustering approach will help me determine the similarities in my data using euclidean distance and group similar months together. I set my number of clusters to be 3 because I understand that a market generally has three sentiments regarding a bubble. It is either a normal market, a somewhat bubble, or a full bubble. I did not use the elbow method to determine the cluster because it resulted in an impractical number of clusters. So I went ahead and used my rationale to determine the number of clusters. The results looked like this.


Cluster using K-means

From the cluster, we can identify the months that were similar to the previous bubble months. We can do that because we know which months were in a bubble during the previous bubbles. I interpreted cluster one as being normal months in the stock market. Because looking back at the months that were in this cluster most of the months were considered normal months of the stock market. Cluster two can be considered a somewhat bubble cluster. This cluster included most of the months that were in a somewhat bubble market and some full bubble months. Cluster zero can be considered a full bubble cluster. It included most of the months that were in a bubble and some somewhat bubble months. This cluster included the months from the housing market crash and dot com crash. As you can see the current month of April is in the same cluster as those crashes.

Going back to the 5 Stages of the bubble.

Now that we have identified our cluster we need to find supporting information to have a better understanding of the cluster. We will use the economical market data we extracted along with some research to identify if the current market is in those stages. So let’s see if the five stages we discussed above apply to the current market.

Displacement

One of the new paradigms in the current market is the huge growth of newbie retail investors. According to JPM, more than 10 million new investors entered the market in 2020 alone. Additionally, the fed kept interest rates at nearly zero percent and continued pumping billions of dollars into the market each month. This has created a great opportunity for investors to make profits.

Boom

With these new paradigms, the market started soaring. People were making wild returns on their investments. Even the new investors who know nothing about investing made good returns. Which created a euphoria in the market.

Euphoria

Investors making these wild returns attracted more investors, The market got filled with FOMO so stocks continued to soar. One good example is the situation with meme stocks.

Profit-taking

In the past month, we are seeing some sell-off in the market due to high inflation and the fed tampering. Stocks that were overvalued due to hype or just people having money and buying it because they assumed someone would pay more for it is now slowing down. Investors are going back to the fundamentals and valuing stocks accordingly.

Panic

This is the final stage and indication of the bubble bursting. There is no sign of such a panic. The feds are doing their best to control the situation.

Summary

Although we can’t tell for sure if we are in a bubble unless it bursts, having an understanding of the current market in comparison to the previous bubble is important when making investments. This analysis gives a good summary of the current market. We have discussed how the low-interest rate and the increase in currency circulation might have resulted in high inflation. We have also seen historical market data for major stock indexes to understand the trend in the market. We also applied machine learning techniques to find clusters and find similarities of each month of the year since 2000. From this analysis, we have discovered useful insights and increased our understanding of the current market.

Given all this information, investors should take caution when trading and focus on long-term investments. Investors should look at the fundamentals of the company and focus on investing in individual stocks with high potential for growth.

Limitation

This analysis included minimal economic and stock history data. Adding more data will give the cluster more features, which could result in a better cluster. Also, understanding which economical data to include to identify a bubble would result in a better cluster. One economical data that could be important to this analysis is the labor market data. Another limitation in this analysis is not having enough historical data that represents the bubble. In my dataset, I only had data from the 2008 housing crash bubble and some part of the 2000s bubble data. I couldn’t extract economic and historical stock market data for some of the dates before 2000. I am not an expert in the stock market or the economy, so interpreting the cluster was challenging. For example, in cluster zero the month after the march of 2020 until the present is all in the same cluster that we identified as a bubble cluster. This was a bit strange and hard to interpret.
