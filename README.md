# Surfs Up
## Weather Data Analysis for Investors

### Overview of the Analysis:

A business proposal has been drafted for an ice cream and surf shop to be built on the Oahu island of Hawaii.  With ample customers, locals and vacationers alike, it is unlikely the consumer base would not respond well to a shop with two offerings both demographics enjoy.  Though this initial proposal seems to have a lot of potential to be very successfull, there is one major conern, the weather.  For the majority of the year, the weather on Oahu is ideal for ice cream and surfing, but one of the investors had a business venture in Hawaii that underperfomed and failed due to the unexpected negative impact of the weather.  Further analysis was requested by this investor to compare and contrast the temperature variances between the months of June and December.  The analysis was performed by querying an SQLite file consisting of temperatures and precipation recorded for Hawaii between the years of 2010 and 2018.

### Results:

In order to acquire the necessary data to perform the requested analysis, queries were written for both June and December to filter all of the data collected within the SQLite database.  These are the queries that were written:

June:

![June Query](https://github.com/matthewdouglasmartin/surfs_up/blob/main/PNG_Resources/June_Query.png)

December:

![December Query](https://github.com/matthewdouglasmartin/surfs_up/blob/main/PNG_Resources/December_Query.png)

Once the queries were established to pull the specific data, the results from these queries were saved into a list and then converted into a Pandas dataframe.  Summary statistics were then provided for each dataframe by performing the .descibe() method on each dataframe.  Below are the summary statistics returned:

June Summary Statistics:

![June Query as DF](https://github.com/matthewdouglasmartin/surfs_up/blob/main/PNG_Resources/June_Query_as_DF.png)

December Summary Statistics:

![Dec Query as DF](https://github.com/matthewdouglasmartin/surfs_up/blob/main/PNG_Resources/Dec_Query_as_DF.png)

There are three main differences between the weather in June and December, listed below:

* The average temperature for June is 74.944° and it is 71.042° for Decemember.  There is only about a 3.902° variance between the two months.
* The largest difference for June and December are the minimum temperatures recorded for each month.  In June the minimum temperature was recorded at 64.000° and in December it was recorded at 56.000°.  There is a 9.000° variance between the two, with 56.000° being too cold for must customers to want ice cream or to surf.
* The standard deviation of temperatures for June and December can be used as well to provide more insight into the conistency of appropriate temperatures for an ice cream surf shop.  June's standard deviation is 3.257° and December's is 3.746°.  There is some difference between these two statistics, but taking into consideration the averages for both months- this standard deviation is not enough to deter patrons from conducting business at the shop year round.
  
### Summary:
Though there are differences that exist between the summary statistics for June and December, there is not enough variance between the two sets of resutls to conclude that a Ice Cream and Surf Shop would not be sustainable year round on Oahu in Hawaii.  This analysis only takes into consideration the temperatures between the two months.  Another aspect of weather in addition to the temperature that should be taken into consideration is the precipation.  A query could and should be written to acquire this data from the SQLite database to retrieve precipation data, because though the temperature might be ideal for the shop- heavy amounts of rain will most likely be less than ideal.  In order to provide more insight into the weather conditions on the island of Oahu, queries could be written that retrieve data from stations that are within a resonable radius of Oahu.  These queries would provide more specific statistics for the particular island in question instead of providing statistics for all of Hawaii.  