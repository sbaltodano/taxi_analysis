# Impact of the Pandemic on Taxi Services in NY

### Method and Data Cleaning

Downloaded all CSV files for the yellow and green taxi records between January 2019 to July 2021. 

Note that for this project, I did not remove any columns from the original dataframe. My goal was to maintain the integrity of the data and allow myself the opportunity to do further analysis with it in the future. That being said, I did choose to drop outliers entirely. This was done by dropping rows from the ‘fare_amount’ column which were not within 3 standard deviations of the mean fare cost. I chose to drop outliers based on this column since it was the main attribute used in my analysis. Additionally, the majority of the fare costs that were not within 3 standard deviations of the mean were either negative fare costs due to a dispute, or extremely high fare costs that appeared to be caused by experimental or technological error and not by variability in the measurement.

1. Revenue in 2020 for both yellow and green taxis fell below one third of the revenue earned for 2019. Revenue for 2021 is on trend to perform similarly to 2020. Given that the pandemic is ongoing, it is difficult to predict whether we will see revenue as high as it once was in 2019, at over $1.4M. The negative economic impact the pandemic has had on taxi services in NYC could last longer than the pandemic itself. 

I would like to review the change in revenue for other leading ride share companies to better gauge where taxi services stand against their competitors into 2021. With more time I would like to compare revenue against peak covid outbreak months, specifically the final quarter of 2020.

I received these results by creating separate data frames by year, dropping outliers which fell above 3 standard deviations of the mean, and additionally dropping columns with negative fare values (most commonly caused by disputes). Revenue was summed by year using the ‘fare_amount’ attribute; surcharges, taxes, and driver tips were purposely excluded from revenue.


2. Across green and yellow taxis and in 2019 and 2020, the cheapest fare was only $1. There were many trips in each data frame with this cost were all very short, with only a few miles traveled.

The most expensive trip for green taxis in 2019 travelled from Williamsbridge/Olinville to Fort Greene and cost around $53, while the most most expensive in 2020 cost $58 and travelled from Erasmus to Marble Hill. In green taxis


3. The most used payment method pre-pandemic and post-pandemic was credit and debit card. The pandemic does not appear to have had a significant impact on payment methods. In fact, in green taxis there was a marginal decrease of <2% in the proportion of credit and debit card payments from 2019 to 2020. 

I attained this answer by finding the mode payment method for each year and calculating the proportion of a payment type to the total known payment methods.


4. From 2019 to 2020 in yellow taxis, the day with the highest average fare costs changed from Thursday in 2019 to Sunday in 2020. This could be due to longer trips out of town and partially influenced by the increase in remote work. Additional analysis would be needed to confirm or deny that hypothesis. For green taxis, the day with the highest average fare cost was Wednesday in 2019 and Tuesday in 2020. Overall, the average fare cost day by day varies by a few cents to a dollar.

These results were obtained by grouping the data frames by weekday and averaging the ‘fare_amount’ column. If I were to do this again I would consider adding the surcharges to the average as that fee may be a better indication of how the demand changes day by day in NYC.
