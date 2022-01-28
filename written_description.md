# Written Description

## Abstract
I predicted wine prices using scraped data from TotalWine.com, using vintage, age, region, grape, customer reviews, and expert ratings to fit and score a linear regression model. My final model was able to predict wine prices with an r^2 value of .66 on the withheld test set. The biggest predictor was by far the winegrowing region, followed by vintage and then expert ratings. Wines from some of the Bordeaux appellations in France were the most expensive regions, along with Napa Valley, CA. Age and customer reviews were only slightly predictive.

## Components
### Design

My client is a combination wine bar / wine store looking to avoid overhyped wines and focus on quality, boosting underrated wines.

I trained and tuned a linear regression model that can take in the categorical variables of region, vintage, and grape variety, along with the numeric variables of age, expert ratings on the 100 point wine score, and customer reviews. The target prediction is the price of a 750 mL bottle of red wine.

### Data
I scraped information on 3,500 bottles of red wine from TotalWine.com, using Selenium to scrape and then BeautifulSoup to parse. After cleaning the data and tuning the model, I still ended up with almost 3,000 rows. The year and rating were missing for a number of wines, and originally I imputed the mean to replace those null values, but soon I realized that wines without years or ratings tend to be lower-priced wines. Imputing a recent year and a low rating improved model performance significantly.

### Algorithms

* Linear Regression from scikit-learn
* One hot encoding via pd.dummies() for making categorical variables numeric
* OLS from statsmodels
* z-score from scipy stats to standardize features
* Lasso regularization (experimented with it but it did not improve performance)

### Tools
* Scraping using Selenium
* Parsing using Beautiful Soup
* Exploratory data analysis in pandas
* Algorithms and calculations via scikitlearn, statsmodels, scipystats
* Python visualization via Squarely, matplotlib and seaborn

### Communication
* 5 minute slide presentation to client (wine bar / wine store) with recommendations on how to avoid overvalued wines and promote undervalued wines
* This description / abstract
