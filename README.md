# Home_Sales
Module 22 Challenge - DUE 5 June 2023

Home Sales Key Metrics

In this challenge, we use our knowledge of SparkSQL to determine key metrics about home sales data. Then we use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

   ![](https://github.com/mugsiemx/Home_Sales/blob/main/Images/1_read_in_AWS_S3_bucket.png)
    
# The required questions answered as follows:
First change the data types then sql query for the answers.

   ![](https://github.com/mugsiemx/Home_Sales/blob/main/Images/2_change_data_types_and_create_temp_view.png)

1- What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
    The average prices for a four bedroom
    house sold by year are as follows:

   ![](https://github.com/mugsiemx/Home_Sales/blob/main/Images/3_avg_price_4_bed.png)

2- What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

   ![](https://github.com/mugsiemx/Home_Sales/blob/main/Images/4_avg_price_3_bed_3_bath.png)

3- What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

   ![](https://github.com/mugsiemx/Home_Sales/blob/main/Images/5_avg_price_3_bed_3_bath_2_fl_2000sqft_bigger.png)

4- What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

   ![](https://github.com/mugsiemx/Home_Sales/blob/main/Images/6_avg_price_view_temp_view.png)

Compare the run times for the various methods of running the same sql query as question # 4 above:

   ![](https://github.com/mugsiemx/Home_Sales/blob/main/Images/run_times.png)

The highest run time was the sql query from the partitioned parquet files (1.04312419891357 seconds). It was 0.47975 seconds slower than the cached temporary table sql query (0.563373327255249 seconds) and 0.15167 seconds slower than the original temporary table view sql query (0.891453504562377 seconds). The cached temporary table sql query runs fast 0.32808 seconds faster than the original temporary table query.

