# Financial_data_analysis_1

* This projects aims to analyse a stock portfolio that contains the following stocks: 'LVMUY', 'MSFT', 'WMT', 'GLD', 'T' by finding their hitorical return, covariance and correlation.
* Scraped 10 years of stock data from Yahoo finance API

* Project details  
The securities under this portfolio are picked from a wide range of different sectors in order to achieve portfolio diversification and lowering risk.
1. technology (MSFT)  
2. telecommunications (T)  
3. consumer goods (WMT)  
4. Healthcare: (XOM)  
5. luxury goods: (LVMUY)  

* The log Return of a Portfolio of Securities from 2013 - 2023 historical data is then calculated and visualised in the below graph:

![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/Normalised%20Portfolio%20stock%20price%202013-2023'.png)
* Findings: 
1. MSFT has the most significant growth   
2. GLD has the lowest return, yet it has a stable performance.

* The project then explores the covariance and correlation between difference stocks, with results visualised as follows:
 
![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/Portfolio%20annualised%20covariance%20matrix%20heatmap.png)  
It is noted that all stocks show a low covariance towards each other.  

![](https://github.com/GISOGISO/Financial_data_analysis/blob/main/images/Portfolio%20correlation%20matrix%20heatmap.png)

**Findings:**  

**Correlation matrix**  
Most of the stocks show a low corerlation of less than 0.4.  
GLD shows the weakest correlation against all other stocks in the portfolio.  GLD is considered an independent stock.  
LVMUY and MSFT has the highest correlation of 0.51, it is a surprise finding as the stocks belongs to completely different sectors, i.e. the former in luxury goods and the latter in technology sector. The below provides brief analysis on the relatively high correlation for the 2 stocks:  
1. Both LVMUY and MSFT are large, multinational companies with diverse revenue streams, hence their stock prices may be influenced by similar macroeconomic factors such as global economic trends and political events.
2. Both LVMUY and MSFT are considered as high-quality, blue-chip companies, hence they are generally considered as stable and reliable investments. Investors may therefore be more likely to hold both stocks in their portfolios as a way to diversify their holdings and reduce risk.

**Overall comments:**  
Overall, the correlation and covariance matrices above suggest that the variables are not highly correlated with each other, indicating that this is a diversified portfolio. 

Note. Please refer to the next financial analysis for further analysis on the portfolio.




