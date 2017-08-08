
# This is a work in progress, all is in flux


----------


# Transformation cookbook [(toc)](./cookbook/000_data_transformation_intro.ipynb)

This cookbook shows how to do data transformation in Python.

[Data transformation](http://r4ds.had.co.nz/transform.html) is one of the steps in the data science process.  Wickham visualizes that process with this figure:

![data-science-explore.png](./cookbook/art/data-science-explore.png)

In the transformation phase we do not add new information.   
We only: **select and reorder** table rows and columns, and **convert values** into a form that is more convenient. 

There is only a limited set of transformations we can do.
1. Handle null values (either drop rows with na-values or impute them)
2. Select the rows and columns we need (slicing and dicing)
3. Reorder rows or columns
4. Aggregate data (work with groups of rows instead of single rows)
5. Join tables
6. Merge tables
7. Add columns that are filled with derived values  
(e.g add a column birth-year and fill it with the year that we find in birth-date)

The Python package Pandas offers all the tools we need to perform these transformations.  
This cookbook will rely heavily on the use of Pandas. 

Those familiar with the SQL, will probably prefer SQL to do 2,3,4, 5 and 6.  
This cookbook will show how this can be done easily with [pandasql](http://blog.yhat.com/posts/pandasql-intro.html) 


----------

[Cookbook intro and table of contents](./cookbook/000_data_transformation_intro.ipynb)


----------
