# Streaming-Finance-Data-with-AWS-Lambda

In this project, I am using the yfinance module get the pricing imformation of the following stock:

Facebook (FB)
Shopify (SHOP)
Beyond Meat (BYND)
Netflix (NFLX)
Pinterest (PINS)
Square (SQ)
The Trade Desk (TTD)
Okta (OKTA)
Snap (SNAP)
Datadog (DDOG)

The information I am interested in is one full trading day of stock high and low prices for each company listed above on Thursday, May 14th 2020, at an one minute interval.

I have created a AWS lambda function, which I call a Data Collector, to collect the stock data. This data collector is responsible for transforming the data into a JSON format. Then each transformed record was put into a firehose delivery stream and was eventually streamed into a S3 bucket.

I then set up a AWS Glue crawler so I can run AWS Athena queries data with the data. What I have generated is a csv file that contains the highest hourly stock 'high' per company listed above.

Lastly, I have created a few visualizations on the data from the results.csv.
