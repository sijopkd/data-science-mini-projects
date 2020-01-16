

**Portfolio Modeling**
----------------------

### **Problem**

In this problem, we will construct three different portfolios of
exchange-traded funds, or ETFs, and use bootstrap resampling to analyze
the short-term tail risk of our portfolios.

We selected the ETFs ensuring diversity and different levels of risk.

The Ivesco QQQ trust is one of the largest, owns only non-financial
stocks and is tech-heavy. The stock had performed well in 2017 but had a
poor return in 2018.

SPY is one of the safest and largest ETFs around.

ProShares VIX Short-Term Futures ETF (SVXY) is a high risk ETF. This is
an unusual ETF since the performance is dependent on the market
volatility, not security.

ProShares UltraShort FTSE Europe (EPV) is a low performing ETF for the
past few years. iShares Core Growth Allocation ETF (AOR) is a very
diverse ETF.

In total, we have selected 6 ETFs - “QQQ”, “SPY”, “SVXY”, “EPV”, “AOR”
and “YYY”. We have considered 5 years of ETF data starting from
01-Jan-2014.

Sample Data for YYY

    ##            YYY.Open YYY.High  YYY.Low YYY.Close YYY.Volume YYY.Adjusted
    ## 2014-01-02 13.96358 13.96358 13.88534  13.89738      19600     13.89737
    ## 2014-01-03 13.98766 13.98766 13.81913  13.92145      15900     13.92145
    ## 2014-01-06 13.89136 13.93349 13.87932  13.93349       9800     13.93349
    ## 2014-01-07 13.93349 14.03581 13.93349  14.03581      10700     14.03581
    ## 2014-01-08 14.02377 14.02377 13.95756  13.97562      10400     13.97563
    ## 2014-01-09 13.93951 13.98766 13.93349  13.98766      13500     13.98766

Lets look at how the stocks are performing relative to each other. We
can see a strong correlation here. But it is complex and non-linear. As
discussed above, a few are performing well, others are not.

![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-45-1.png)

Volatility of the ETFs across the 5 year period.

![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-46-1.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-46-2.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-46-3.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-46-4.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-46-5.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-46-6.png)

Our initial wealth is $100,000

SIMULATION 1 : SAFE Portfolio

ETFs: “QQQ”, “SPY”, “SVXY”, “EPV”, “AOR”, “YYY”

For the safe portfolio, we distributed 90% of the total wealth among the
high performing ETFs - QQQ, SPY and AOR.

![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-50-1.png)

![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-51-1.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-51-2.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-51-3.png)

    ## Confidence Interval from Bootstrap Distribution (5000 replicates)

    ## 
    ## Average return of investement after 20 days 100919.1

    ## 
    ## 5% Value at Risk for safe portfolio- -5078.728

SIMULATION 2 : HIGH RISK PORTFOLIO

For the high risk portfolio, we distributed 90% of the total wealth
among the low performing ETFs - SVXY, EPV and YYY.

Average return of investement after 20 days - $100724.3  
5% Value at Risk for safe portfolio - $7850.127

![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-54-1.png)

![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-55-1.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-55-2.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-55-3.png)

    ## Confidence Interval from Bootstrap Distribution (5000 replicates)

    ## 
    ## Average return of investement after 20 days 100723.2

    ## 
    ## 5% Value at Risk for High portfolio- -7739.601

SIMULATION 3 - With equal weights for high risk and low risk

![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-57-1.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-57-2.png)![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-57-3.png)

    ## Confidence Interval from Bootstrap Distribution (5000 replicates)

    ## 
    ## Average return of investement after 20 days 100715.4

    ## 
    ## 5% Value at Risk for High portfolio- -6767.904

![](Final-Submission_files/figure-markdown_strict/unnamed-chunk-59-1.png)

#### **Summary**

For the safe portfolio, we are observing the maximum return of
investment and the lowest 5% VaR. As the portfolio risk increases, we
are able to witness the decrease in returns and increase in VaR value as
expected.

References:
<a href="https://www.bankrate.com/investing/best-etfs/" class="uri">https://www.bankrate.com/investing/best-etfs/</a>
<a href="https://etfdb.com/compare/lowest-ytd-returns/" class="uri">https://etfdb.com/compare/lowest-ytd-returns/</a>

