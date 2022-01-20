# Project Proposal
## The Price of Wine
### Question/need:
* *What is the framing question of your analysis, or the purpose of the model/system you plan to build?*

What makes a wine more or less expensive? Wine pricing has always seemed subjective to me; I've really enjoyed some $7 bottles, and hated some $90 bottles. If I have access to data on key features such as region, year, grape, and even tasting keywords, can I create a model to predict the wine's price?

* *Who benefits from exploring this question or building this model/system?*

Buying wine can be intimidating to beginners; it is helpful to understand what characteristics in a wine may make it more expensive. Wine stores may also benefit from understanding the value of a bottle programmatically when deciding its resale value, and if a wine is selling above or below its true value.

-------

### Data description:
* *What dataset(s) do you plan to use, and how will you obtain the data?*

I plan to scrape TotalWine.com to get data on their red wines (over 3,000 listings), using Selenium to grab text within HTML elements by their class names.

* *What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?*

The unit of analysis is each bottle of red wine on TotalWine.com. I expect to work from all or some of these features: year, region, grape, and tasting keywords.

* *If modeling, what will you predict as your target?*

The target will be the price of an individual bottle of red wine (750mL).

-------

### Tools:
*How do you intend to meet the tools requirement of the project?*

* I'll use Selenium to scrape 32 pages of data from Total Wine's website, and Beautiful Soup to parse the HTML.
* I'll use pandas to clean and compile the dataframes, and visualize results using matplotlib and seaborn. 
* I'll use the Linear Regression model from scikit-learn to create a model to predict price, using training, validation, and test datasets to refine the model and measure against performance.

*Are you planning in advance to need or use additional tools beyond those required?*

No specific plans to do so.

-------

### MVP goal:
* *What would a minimum viable product (MVP) look like for this project?*

A minimum viable product would consist of a Linear Regression model, chosen and refined using a validation set and ultimately measured against a test set. At minimum, it will predict price based on at least two features, using at least one page of data from TotalWine.com (120 bottles/rows).