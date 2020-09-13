
# Northwind Hypothesis Testing

![](https://raw.githubusercontent.com/twhipple/dsc-mod-3-project-online-ds-pt-090919/master/Images/mailsparky_gone-south-1229875-639x426.jpg)
*A change in the north wind moving from SQL to pandas, Source: mailsparky, freeimages.com*


## Flatiron Mod 3 Final Project


## README Outline
* Introduction 
* Project Summary
* Repo Contents
* Libraries and Prerequisites
* Feature and Definitions
* Results
* Future Work
* Built With, Contributors, Authors, Acknowledgments


## Introduction
This project is the accumulation of a month long study of learning about hypothesis testing and statistical significance. In this repo you will find everything I learned about statistical analysis through data science. The Jupyter notebook will demonstrate how I examined four different questions concerning the mock Northwind dataset (which was created by Microsoft for academic purposes) using Python and SQLite.


## Project Summary
The four hypothesis tests were:
1. Does discount amount have a statistically significant effect on the quantity of a product in an order?
2. Which regions had the biggest orders and the most sales?
3. Does unit price affect quantity of order? Are more expensive items ordered the same as cheaper products?
4. Does the shipping company have an affect on the order processing speed?

![](https://raw.githubusercontent.com/twhipple/dsc-mod-3-project-online-ds-pt-090919/master/Images/Northwind_ERD_updated-Copy1.png)
*Image: The Northwind relational data schema, Source: Microsoft*


## Repo Contents
This repo contains the following:
* README.md - this is where you are now!
* Final_Notebook.ipynb - the Jupyter Notebook containing the finalized code for this project.
* LICENSE.md - the required license information.
* Blog Post - the link to my Medium blog post pertaining to this project.
* Executive Summary Presentation (slide show) .pdf and link
* Northwind_small.sqlite - the file containing the SQL dataset.
* CONTRIBUTING.md 
* Mod 3 Flatiron Final Project Specifications - an explanation of the project.
* video_link - https://drive.google.com/file/d/1ueAFJc2KdOzWoUx8hKfnAkJgqmP_QfZm/view?usp=sharing
* Northwind_ERD_updated.png - the SQL schema for the dataset

![](https://raw.githubusercontent.com/twhipple/dsc-mod-3-project-online-ds-pt-090919/master/Images/Screen%20Shot%202020-09-13%20at%2012.34.07%20PM.png)
*Manipulating the json database using pandas and the groupby method to create new dataframes*


## Libraries & Prerequisites
These are the libraries that I used in this project.
* import pandas as pd
* import sqlite3
* import json
* import numpy as np
* import matplotlib.pyplot as plt
* import seaborn as sns
* %matplotlib inline
* import scipy.stats as stats
* import statsmodels.api as sm
* from statsmodels.formula.api import ols - for ANOVA testing


## Conclusions
Discounted sales seemed to be the greatest factor when looking at total quantity. Certainly some discounts were more affective than others but this study did not have enough time to be more specific. According to my Welch's t-test results, the p-value is small enough that I can safely reject the null - This means that there is enough evidence to state that the sales will be larger with the discounted group. You can also see in the histograph above where dicounted and non-discounted orders overlap that the discounted orders have much higher count numbers that further states that they are more likely to sell more.

![](https://raw.githubusercontent.com/twhipple/dsc-mod-3-project-online-ds-pt-090919/master/Images/Screen%20Shot%202020-09-13%20at%2012.26.31%20PM.png)
*Histogram for quantity of product sold - depending on discount*

Unit Price was found to be not as important as total quantity. While it seems plausible for more expensive items to be less marketable, the results showed that this was not the case. I attempted to break the regions up into fewer groups but the ANOVA test didn't respond. I also attempted to perform a 'groupby' in order to simplify the Discounted Sales column but again, the ANOVA test wouldn't work. 

![](https://raw.githubusercontent.com/twhipple/dsc-mod-3-project-online-ds-pt-090919/master/Images/Screen%20Shot%202020-09-13%20at%2012.29.32%20PM.png)
*Another histogram based on the unit price - here I binned the products into expensive verses inexpensive*

The Sales Region appears to be important but results could not be validated. This was due either to having too many regions or for the great sales variance in different regions. According to the results of experiment number 3 and a p-value greater than 0.05, there was no difference between the quantity of cheap items bought and the quantity of expensive items bought. We can not reject the null. The power shows us that this experiment is valid. Even though I would assume that cheaper items would be easier to sell and perhaps more profitable for a company, this test shows that this is not the case. I also tried binning items into a few different price groups but the results were inconclusive

![](https://raw.githubusercontent.com/twhipple/dsc-mod-3-project-online-ds-pt-090919/master/Images/Screen%20Shot%202020-09-13%20at%2012.27.43%20PM.png)
*Colorful bar graph of the total sales by region*

Furthermore, the Shipping Company proved to be a minor detail with little significance. Either the mean difference in time to ship out orders was minimal or the overall number of orders and variance makes this aspect of less a concern. According to the results of the power test, I am confident that the difference in shipping companies is not statistically significant. 


## Future Work
Obviously I would like to review different discounts and determine which values bring in the most orders - but I would also like to have a control group were there are no discounts offered. Perhaps the money lost on discounts is made up for with additional sales. It would be helpful to have more information on the actual cost of items to be able to compare specific unit prices, markup values, and overall net profit. With Sales Region I recommend focusing on the countries with the least number of total orders. Again, using a control group that receives no additional sales support, marketing, or increased product push might allow for some curious data that would help focus on the weaker sales regions. Lastly, knowing when a product was delivered as well as any specifics on the quality of the delivery, packaging, and distances travelled to destinations might offer more information of how the specific shipping companies are doing overall.


## Built With:
Jupyter Notebook
SQL - sqlite 
Python 3.0

## Contributing
Please read CONTRIBUTING.md for details

## Authors
Thomas Whipple
Flatiron Academy

## License
Flatiron Academy - see the LICENSE.md file for details

## Acknowledgments
Thank you to my cohort team for all of their suggestions and to our instructor Abhineet Kulkarni. Thank you to Microsoft as well for providing this rich dataset for academic purposes.

