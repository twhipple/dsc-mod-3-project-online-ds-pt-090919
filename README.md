

# Flatiron Mod 3 Final Project
This project is the accumulation of a month long study of learning about hypothesis testing and statistical significance. In this repo you will find everything I learned about statistical analysis through data science. The Jupyter notebook will demonstrate how I examined four different questions concerning the mock Northwind dataset which was created by Microsoft for academic purposes.


## Summary
The four hypothesis tests were:
1. Does discount amount have a statistically significant effect on the quantity of a product in an order?
2. Which regions had the biggest orders and the most sales?
3. Does unit price affect quantity of order? Are more expensive items ordered the same as cheaper products?
4. Does the shipping company have an affect on the order processing speed?


## Contents
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


## Results and Conclusion
Discounted sales seemed to be the greatest factor when looking at total quantity. Certainly some discounts were more affective than others but this study did not have enough time to be more specific. Unit Price was found to be not as important on total quantity. While it seems plausible for more expensive items to be less marketable, the results showed that this was not the case. The Sales Region appears to be important but results could not be validated. This was due either to having too many regions or for the great sales variance in different regions. Furthermore, the Shipping Company proved to be a minor detail with little significance. Either the mean difference in time to ship out orders was minimal or the overall number of orders and variance makes this aspect of less a concern.


### Prerequisites
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


### Built With:
Jupyter Notebook
SQL 
Python 3.0

### Contributing
Please read CONTRIBUTING.md for details

### Authors
Thomas Whipple
Flatiron Academy

### License
Flatiron Academy - see the LICENSE.md file for details

### Acknowledgments
Thank you to my cohort team for all of their suggestions and to our instructor Abhineet Kulkarni.

