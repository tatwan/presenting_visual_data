# Sales Analysis Activity 2

After you completed your analysis for 2017 you realized there are additional data sources that are needed for a more comprehensive analysis. This includes sales data for 2018 and 2018, as well as store and product related data.

## Load the data & transform the data

* Load `sales_2018`, and `sales_2019` data sets

  ![image-20240309184516794](images/image-20240309184516794.png)

![image-20240309175004415](images/image-20240309175004415.png)

* In order to combine the sales data (2017, 2018, and 2019) make sure you have the same columns (names, and types) for all three data sets
* If there are any “NA” text in price you can replace them with `0`
* If you see errors in one of the columns as shown you can remove error rows

![image-20240605131649048](images/image-20240605131649048.png)

Here are the columns and their data types. Make sure all three have the same 

![image-20240309183551673](images/image-20240309183551673.png)



* Select Append Queries to stack the data on top of each other (2017, 2018, and 2019)
* Select Append Queries as New

![image-20240309183425021](images/image-20240309183425021.png)

Then select `Three or more tables`

![image-20240605124925835](images/image-20240605124925835.png)

Combined 2018 and 2019 data with 2017 

![image-20240605124953977](images/image-20240605124953977.png)

* If you see the following message click `Continue`

![image-20240605125058541](images/image-20240605125058541.png)

* Select `ignore Pricacy Levels checks for this file ...`

![image-20240605125115779](images/image-20240605125115779.png)

* Keep in mind the data is all combined under the `Append1` data. Rename the data from `Append1` to `Combined`



![image-20240605125214361](images/image-20240605125214361.png)

## Load additional data to support your analysis 

* Now add three more files  `store_cities` and `producthierarchy`

![image-20240309184601493](images/image-20240309184601493.png)

* Inspect the `store_cities` dataset 

  ![image-20240605125344611](images/image-20240605125344611.png)

* Make first row as header
* Split the `state-state abr-city` columns into state, state abr, and city columns (3 columns)
* Split `lat/long` into two columns

This is the final output

![image-20240605125747446](images/image-20240605125747446.png)

* Inspect the `producthierarchy` dataset and notice we have several issues:

![image-20240605125831458](images/image-20240605125831458.png)

* Make the first row as headers 
* Click the `category || sub_category` column and split into two fields

![image-20240309192300380](images/image-20240309192300380.png)

![image-20240309192335278](images/image-20240309192335278.png)

* Rename the column as shown

![image-20240605130034647](images/image-20240605130034647.png)



---

## Group your Queries

From this 

![image-20240605131131239](images/image-20240605131131239.png)

To this

![image-20240605131215170](images/image-20240605131215170.png)



## Visualization Challenge

![image-20240605135409184](images/image-20240605135409184.png)

Note the time slider (zoom slider)

![image-20240605135503805](images/image-20240605135503805.png)

### Challenge 2 - Forecasting

![image-20240605140036080](images/image-20240605140036080.png)



### Challenge 3 - Anomalies

![image-20240605140958765](images/image-20240605140958765.png)

