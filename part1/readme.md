# Project summary
* The project is interested in analysing the returns, covariance and correlation of the Portolio [MSFT, T, WMT, XOM, LVMUY] by scraping 10 years of stock data from Yahoo finance API and visualising the result.

# Project details:
 * The securities are picked from a wide range of different sectors in order to achieve portfolio diversification and lowering risk.
1. technology (MSFT)  
2. telecommunications (T)  
3. consumer goods (WMT)  
4. Healthcare: (XOM)  
5. luxury goods: (LVMUY)  
* The log Return of a Portfolio of Securities from 2013 - 2023 historical data is first calculated and visualised in the below graph:

![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/Normalised%20Portfolio%20stock%20price%202013-2023'.png)
* Findings: 
1. MSFT has the most significant growth   
2. GLD has the lowest return, yet it has a stable performance.

* The project then explores the covariance and correlation between difference stocks, with results visualised as follows:
 
![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/Portfolio%20annualised%20covariance%20matrix%20heatmap.png)  
It is noted that all stocks show a low covariance towards each other.  

![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/Portfolio%20correlation%20matrix%20heatmap.png)

**Analysis:**  

**Correlation matrix**  
Most of the stocks show a low corerlation of less than 0.4.  
GLD shows the weakest correlation against all other stocks in the portfolio.  GLD is considered an independent stock.  
LVMUY and MSFT has the highest correlation of 0.51, it is a surprise finding as the stocks belongs to completely different sectors, i.e. the former in luxury goods and the latter in technology sector. The below provides brief analysis on the relatively high correlation for the 2 stocks:  
1. Both LVMUY and MSFT are large, multinational companies with diverse revenue streams, hence their stock prices may be influenced by similar macroeconomic factors such as global economic trends and political events.
2. Both LVMUY and MSFT are considered as high-quality, blue-chip companies, hence they are generally considered as stable and reliable investments. Investors may therefore be more likely to hold both stocks in their portfolios as a way to diversify their holdings and reduce risk, which in turn increasing the correlation of the stocks.

**Overall comments:**  
Overall, the correlation and covariance matrices above suggest that the variables are not highly correlated with each other, indicating that this is a diversified portfolio. 

Note. Please refer to part 2 for further analysis on the portfolio.



2. Identify the optimal securities portfolio for investors with varying risk appetites that maximise returns while minimize risk using the Markowitz portfolio optimization theory and finding the efficeint frontier.
 
* Then, Markowitz portfolio optimization theory and various Python simulations were  The aim is to identify two portfolios that suit investors with different risk appetite: one with the minimum volatility (lowest risk) and another with the maximum Sharpe ratio (highest expected return). These portfolios are calculated, and the efficient frontier is plotted to visualize the results.

Using the same securities, the portfolio is further analysed using the Markowitz portfolio optimization theory and writing correpsonding simulations to identify the portfolio with the minimum volatility(lowest risk) and the portfolio with the maximum Sharpe ratio(highest expected return) and plot the efficient frontier. Both portfolios are calculated in this project analysis in order to suit investors with different risk appetite.

According to the Markowitz theory, investors can optimize their portfolios by selecting the combination of assets that provides the highest expected return for a given level of risk. 

Risk-free rate is defined as the US 10 year Treasury yield as at 16 Mar 2023 (3.45%	) in this analysis

Below are the details of the simulation: 

The code first simulates 30000 random portfolios with positive weights and calculates their annualized returns, volatilities, and Sharpe ratios using the mean returns and covariance matrix of the assets in the portfolio.  
The Sharpe ratio is then calculated using the formula (portfolio return - risk-free rate) / portfolio volatility.  
As it is assumed that this portfolio only allows long position, all securities weightings should be in positive values, hence, the code filters out any portfolios with negative weights.  
The resulting portfolios are stored in a pandas DataFrame and the portfolios with the highest Sharpe ratio as well as the portfolio with the minimum volatility are identified among the set of optimal portfolios.  

The efficient frontier is then plotted to visualize the sets of optimal portfolios with maximum Sharpe ratio and minimum volatility.  The volatility and return of an equal-weighted portfolio is also plotted for comparison purposes.

![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/Efficient%20Frontier%20with%20Max%20Sharpe%20Ratio%2C%20min%20volatility%20and%20equal%20weights.png)  

Then,  the respective weights of the assets of the 2 protfolio are identified, with results visualised as follows:  

![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/max%20return%20pie%20chart.png)
![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/min%20vol%20pie%20chart.png)

Brief analysis:
The two portfolios have very different compositions and weightings.  

*Maximum Sharpe ratio portfolio*
1. The portfolio with the maximum Sharpe ratio is primarily composed of growth assets including technology companies (MSFT, 49.5%) and  the  luxury goods conglomerate (LVMUY, 26.1%). These companies are generally expected to grow faster than the overall market and have the potential for higher returns, yet, they are more volatile and contains higher risks. 
2. It is noted that GLD and AT&T have a minimal weighting in the portfolio, both stocks have low returns and volatility and are considered defensive stocks. 

*Minimum volatility portfolio*
1. The portfolio with the minimum volatility is primarily composed of defensive assets, such as gold (GLD, 53.6%) and Walmart (WMT, 26.6%). These assets are typically considered safe-haven investments as they tend to perform well during economic downturns and times of market volatility. 
2. 
3. On the other hand, the minimum volatility portfolio has the largest weight given to Gold (GLD, followed by Walmart (WMT, 26.6%). This suggests that the portfolio is skewed towards defensive stocks such as gold, and consumer staples like Walmart and AT&T, which are considered to be relatively stable sectors.

For instnace, the telecommunications company, AT&T (T), which is also known for its defensive characteristics, as it provides essential services that people are unlikely to cut back on even during economic hardship.





