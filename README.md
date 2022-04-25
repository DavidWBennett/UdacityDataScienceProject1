# UdacityDataScienceProject1
This is my Project 1 Work for the Udacity Data Science Nanodegree.

This project analyzes the [Seattle AirBnB](https://www.kaggle.com/datasets/airbnb/seattle) dataset found on Kaggle.
Only standard libraries such as pandas, matplotlib, and zipfile are required.

Three questions were presented and then answered:
1. Do rooms get booked more frequently on the weekends?
2. Do rooms that mention the word 'view' in their description charge more?
3. Are guests more likely to write a review if they want to give a very good or very poor review?

The first file- Cleaning.ipynb- is a good place to start. It reads in the raw data as zipped CSV files and does some data preparation. There are three files that are genearted, Calendar, Listings, and Reviews. After the cleaning only two files are required, CalendarCleaned and ListingCleaned. The review dataset was not used as part of this analysis.

Question1.ipynb is used to answer the question "Do rooms get booked more frequently on the weekends?" To do this I grouped the CalendarCleaned data by the percentage of days the room was booked according to the day of the week. For example, there were approximatly 3,800 properties in this dataset spanning one year (2016), allowing for 3800 properties * 52 weeks = about 197,600 Mondays avaialble for bookings. These options were booked approximatley 67% of the time.
There was no discernible difference between Sunday-Thursday and Friday-Saturday, suggesting that weekends are not booked more frequently than weekdays.

Question2.ipynb is used to answer the question "Do rooms that mention the word 'view' in their description charge more?" The price per night was average from the CalendarCleaned dataset, the description was gathered from the ListingsCleaned dataset. To try and standardize the dataset a litte bit only rooms that had the same number of bedrooms were considered. Square feet may have been a better metric but the number of bedrooms field was much better populated than the square feet field. A further analysis was conducted to see if the average price stratified by number of bedrooms was different for rooms that mentioend a 'view' or not. The conclusion is that there is no discernable difference in the average nightly rate between rooms that mention the word 'view' and those that did not. It appears that having a view is not a top priority for guests looking to book an AirBnB in Seattle. The biggest price different was with AirBnBs that had 3 bedrooms, but it was still not very significant.

Question3.ipynb is used to answer the question "Are guests more likely to write a review if they want to give a very good or a very poor review? A commonly held assumption is that guests will only write a review if they have a strong positive or negative reaction to a stay. To test this hypothesis I looked at the average rating and the number of reviews for each listing. I looked at the correlation coefficient and a scatterplot. I suspected there would be a correlation between the number of ratings and the rating score and that in the scatterplot there would be a cluster indicating lots of reviews around a low rating (under 20) and a high rating (over 80). The data did not support this hypothesis. The correlation Coefficient was 0.036 (very poor) and the scatterplot mostly only indicated that most listings have fewer than 100 ratings. There were no obvious clusters around lots of reviews and high (or low) ratings.

