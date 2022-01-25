# MVP
## The Price of Wine

### Purpose
My client is a combination wine bar / wine store with a specific vision. They believe that good wines can come from any grape and wine-growing region, and they want to serve wines based on quality and not on hype. And from a business perspective, they want to assess whether the wines they order are overvalued or undervalued in terms of price, so they can order more undervalued wines and increase their profit margin.

### Definitions
A **region** is a specific wine-growing area somewhere in the world, like Napa Valley, CA or Piedmont, Italy. It is smaller than country or state, which are too broad to draw actionable insights from.

A **grape** is the specific grape a wine variety is made from, such as Pinot Noir or Cabernet Sauvignon.

### Data
I'm looking at data from TotalWine.com, which gives the price, name, region, and grape on each bottle of red wine (and often year). Currently I've been able to scrape region and grape from 552 bottles, but there are over 3,000 listings, and I'll pull at least 1000.

### Results 
#### Region, grape, and price
I used one hot encoding to turn my categorical columns (each region and grape variety) into numerical columns, and removed features with too few rows for analyze. This made for 91 total features. I fit a Linear Regression model and came up with an R2 value of **0.632**. This means wine pricing is indeed influenced by region and grape, though there are obviously other factors.

I will look at both year and age of the wine next. With wine, age can matter, but specific years can also be "good" or "bad" due to weather and other factors, so I do need to analyze both. I'll look at tasting keywords as well - not expecting this to have much of an impact, but it would be interesting to find out if certain keywords are used more for expensive or cheaper wines. A jointplot showing the linear regression model is below.

![](https://raw.githubusercontent.com/Elaela22/wine_prices/main/joint_plot.png)

### Recommendations
1. The biggest positive influence on price is the Napa Valley region. This could mean Napa Valley wines are overvalued, due to their enormous reputation and the region's attraction to wine tourists. To accomplish the client's specific mission to promote undervalued wines, I recommend that they order fewer Napa Valley wines. This includes Yountville, which is also technically in Napa (where the famous Michelin-starred restaurant French Laundry is located).
	* The regions of Pessac-Leognan, Bordeaux and Margaux in France also are correlated with high prices, as is Brunello di Montalcino, in Italy. These regions are all known for expensive wines. Lean away from these regions, except for Bordeaux, which offers so many wines that it should still be quite possible to select undervalued wines from wineries there.
	* Cabernet Sauvignon and Bordeaux Blend are the most expensive grapes; for full-bodied wines that are undervalued, it would be better to lean towards:
		*  Merlot
		*  Malbec
		*  Zinfandel
		*  Petite Syrah
		*  Syrah/Shiraz

2. Red blends, Pinot Noirs, and wines from the Central Coast and Paso Robles (both in CA) are most undervalued. Order more of these!


![](https://raw.githubusercontent.com/Elaela22/wine_prices/main/wine_corrs.png)
