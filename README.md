# Home_Sales

In this challenge, we use SparkSQL to determine key metrics about home sales data. We then use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

Using Google Colab, we import the necessary PySpark SQL functions for this challenge. Afterwards we read the home_sales_revised.csv data into a Spark DataFrame to then create a temporary table called home_sales.

With the temporary table, we use SparkSQL to answer the following questions using SparkSQL:

1- What is the average price for a four-bedroom house sold for each year? Rounding off the answer to two decimal places.

2- What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Rounding off the answer to two decimal places.

3- What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Rounding off the answer to two decimal places.

4- What is the "view" rating for homes costing more than or equal to $350,000? We determine the run time for this query, and rounding off the answer to two decimal places.

We cache the temporary table home_sales table and check to confirm the temporary table is cached. Using the cached data, we run a query that filters out the view ratings with an average price of greater than or equal to $350,000. We display the runtime and compare it to uncached runtime from our 4th question.

We partition by the "date_built" field on the formatted parquet home sales data and create a temporary table for the parquet data. We run the query that filters out the view ratings with an average price of greater than or equal to $350,000. We display the runtime and compare it to the uncached runtime.

We finally uncache the home_sales temporary table and verify that the home_sales temporary table is uncached using PySpark.
