# Project summary  
The project aims to identify the optimal securities portfolio for investors with varying risk appetites that maximise returns while minimize risk using the Markowitz portfolio optimization theory and finding the efficeint frontier through writing various Python simulations and visualising the results.
 
# Project details  
According to the Markowitz theory, investors can optimize their portfolios by selecting the combination of assets that provides the highest expected return for a given level of risk. 

Risk-free rate is defined as the US 10 year Treasury yield as at 16 Mar 2023 (3.45%	) in this analysis

Below are the details of the simulation: 

The code first simulates 30,000 random portfolios with positive weights and calculates their annualized returns, volatilities, and Sharpe ratios using the mean returns and covariance matrix of the assets in the portfolio.  
The Sharpe ratio is then calculated using the formula (portfolio return - risk-free rate) / portfolio volatility.  
As it is assumed that this portfolio only allows long position, all securities weightings should be in positive values, hence, the code filters out any portfolios with negative weights.  
The resulting portfolios are stored in a pandas DataFrame and the portfolios with the highest Sharpe ratio as well as the portfolio with the minimum volatility are identified among the set of optimal portfolios.  

The efficient frontier is then plotted to visualize the sets of optimal portfolios with maximum Sharpe ratio and minimum volatility.  The volatility and return of an equal-weighted portfolio is also plotted for comparison purposes.

![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/Efficient%20Frontier%20with%20Max%20Sharpe%20Ratio%2C%20min%20volatility%20and%20equal%20weights.png)  

Then,  the respective weights of the assets of the 2 protfolio are identified, with results visualised as follows:  

![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/max%20return%20pie%20chart.png)
![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/min%20vol%20pie%20chart.png)

**Brief analysis:**  
The two portfolios have very different compositions and weightings.  

*Maximum Sharpe ratio portfolio*
1. The portfolio is primarily composed of growth assets including technology companies (MSFT, 49.5%) and  the  luxury goods conglomerate (LVMUY, 26.1%). These companies are generally expected to grow faster than the overall market and have the potential for higher returns, yet, they are more volatile and contains higher risks. 
2. It is noted that GLD and AT&T have a minimal weighting in the portfolio, both stocks have low returns and volatility and are considered defensive stocks. 

*Minimum volatility portfolio*
1. The portfolio is primarily composed of defensive assets, such as gold (GLD, 53.6%) and Walmart (WMT, 26.6%). These assets are typically considered safe-haven investments as they tend to perform well during economic downturns and times of market volatility. 

## Implications to investors: 

1. Higher risk tolerance investors: 
- If the investor has a higher risk tolerance and is willing to accept more volatility in exchange for potentially higher returns, then the maximum Sharpe ratio portfolio may be more suitable. This portfolio is designed to maximize expected returns for a given level of risk, and as a result, may outperform the minimum volatility portfolio in certain market conditions, e.g. during a bull market.

2. Lower risk tolerance investors: 
- If the investor has a lower risk tolerance and prioritizes capital preservation over potentially higher returns, then the minimum volatility portfolio may be more appropriate. This portfolio is designed to minimize risk for a given level of expected returns, and may be more resilient during market downturns.  

Ultimately, investors should carefully consider their investment goals, risk tolerance, and investment horizon when deciding between the two portfolios. It is also important to note that these portfolios are not static and require periodic adjustments.


