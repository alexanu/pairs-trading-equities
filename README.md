# Building an Equity Pairs Trading Model

###### This project is meant to use python and the stattools library in building a pairs trading model. There is also code that utilizes a previously built PostgreSQL database of stock data to find pairs of stocks that exhibit cointegration. By using my equity data warehouse (built with PostgreSQL and Python) the project that follows builds a rolling cointegrated pairs trading model.


# Schema of the project:
https://bubbl.us/NDc3NDc4NC8zODg3MDM5L2QzMTFiZTAzZWFjN2FiMTFhZTAzZTk4MjNjZjA2MDI2@X?utm_source=shared-link&utm_medium=link&s=10033313



###### Link: https://medium.com/@constandinou.antonio
###### Title of blog post - *Quant Post 3.2: Building a Pairs Trading Model*

### Getting Started
If you plan on using this code along with the equity database, please reference the following link before moving forward: https://github.com/alexanu/data-warehouse-build

### Quick overview of computed iterations
I have not documented actual time taken in running the below scripts, but the original database used for this test includes ~ 505 equities and their respective historical data which totals around 1.5 million lines of historical data.

The pairs trading model will only identify pairs to trade within the same sector, and there are 11 sectors total. The total number of potential pairs tested across all sectors is roughly 14,500 pairs.

The current setup also uses 2-year's worth of market data in a rolling fashion starting in 2006 and up until 2016. That creates 11 time periods to verify all potential 14,500 pairs to trade.
