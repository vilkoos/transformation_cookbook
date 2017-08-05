# Transformation cookbook

This cookbook shows how to do data transformation in Python.

[Data transformation](http://r4ds.had.co.nz/transform.html) is one of the steps in the data science process.  
Wickham [1] visualizes that process with this figure:

![data-science-explore.png](./art/data-science-explore.png)

The transformation step starts with one ore more tidy tables.   
Tidy [2] means that we work with quality data (i.e. there are no data-problems present in our tables, hence we can use the tables safely).  
Appendix 1 looks at tidy data concept in depth. 

We start with tidy tables, so the hard work of acquiring, cleaning, integrating and relating the data is already done.  
In the transformation phase we do not add new information neither do we undo the tidy-table-form.  
We only: **select and reorder** the rows and columns, and **convert values** into a form that is more convenient. 

There is only a limited set of changes we can make.
1. Handle null values (either drop rows with na-values or impute them)
2. Select the rows and columns we need (slicing and dicing)
3. Reorder rows or columns
4. Aggregate data (work with groups of rows instead of single rows)
5. Join tables
6. Merge tables
7. Add columns that are filled with derived values  
(e.g add a column birth-year and fill it with the year that we find in birth-date)

The Python package Pandas [3][4][5] offers all the tools we need to perform these transformations.  
This cookbook will rely heavily on the use of Pandas. 

Those familiar with the SQL, will probably prefer SQL to do 2,3,4, 5 and 6.  
This cookbook will show how this can be done easily with [pandasql](http://blog.yhat.com/posts/pandasql-intro.html) [6]

# Contents

================ pre-requisites ===================================
- 101 - Pandas [Dataframe fundamentals](101_Pandas_Dataframe_fundamentals.ipynb)
- 102 - elementary dataframe properties and methods 
- 103 - How to create dataframes in Python
- 110 - How to read data from file
- 120 - Why use SQL
- 130 - Where to find the pandas documentation

================ transformations =================================
- 200 - How to handle null values
- 300 - How to select rows and columns
- 400 - How to order rows and columns
- 500 - How to work with groups of rows
- 600 - How to join tables (join on columns)
- 650 - How to merge tables (join on rows)
- 700 - How to add columns with derived data
- 710 - How to enforce order for ordinal variables
- 720 - How to convert from numerical to ordinal
- 730 - How to do brute force derivation (guilty pleasures)

================ post-requisites ===================================
- 900 - How to save transformed data to file

# Appendici

- [apdx01](apdx01_Tidy_data_V_normalization.ipynb) - Tidy tables versus data normalization
- apdx02 - an introduction to boolean logic using SQL examples
- apdx03 - an introduction to set theory using SQL examples

# References 

[1] Hadley Wickham, Garret Grolemund, R for data science, O'Reilly, 2016 (free copy at [www](http://r4ds.had.co.nz/))

[2] Hadley Wickham, Tidy data, The Journal of Statistical Software, vol. 59, 2014. (free downlaod at [www](https://www.jstatsoft.org/index.php/jss/article/view/v059i10/v59i10.pdf))

[3] William McKinney, Python for Data Analysis, O'Reilly, 2012 (free copy at [www](http://www3.canisius.edu/~yany/python/Python4DataAnalysis.pdf))

[4] Python Data Analysis Library ([www](http://pandas.pydata.org/))

[5] Official Pandas tutorial and cookbook ([www](http://pandas.pydata.org/pandas-docs/stable/tutorials.html))

[6] Yhat, pandasql: Make python speak SQL, [The Yhat Blog](http://blog.yhat.com/posts/pandasql-intro.html), 2016.

[7] Vik Paruchuri, Working with SQLite Databases using Python and Pandas, 2016 ([Blog](https://www.dataquest.io/blog/python-pandas-databases/))

[8] Karlijn Willems, Pandas Cheat Sheet: Data Science and Data Wrangling in Python, KDnuggets, 2017 ([Blog](http://www.kdnuggets.com/2017/01/pandas-cheat-sheet.html))

[9] Karlijn Willems, Pandas Tutorial: DataFrames in Python, datacamp, 2016 (free datacamp [minicourse](https://www.datacamp.com/community/tutorials/pandas-tutorial-dataframe-python/#gs.5amgiOc))