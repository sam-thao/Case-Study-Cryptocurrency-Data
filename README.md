# Case-Study-Cryptocurrency-Data

## What’s with the hype?

* Look at historical daily prices
* How has it performance compared to the stock market?
  * Bitcoin vs S&P 500
  * Top 3 Cryptos vs S&P 500
* How has other top coins like Ethereum and Litecoin performed compared to Bitcoin
* How early can we spot major swings in momentum?

* 
## Cleaning the Data
The data extraction process involved retrieving information from www.investing.com in the form of an Excel spreadsheet for SP500, BTC, LTC, and ETH. Subsequently, a new workbook was created, and the dates and prices were copied from their respective spreadsheets.

It's worth noting that certain dates lack a value; for instance, SP500 doesn't provide prices on weekends.

A main table was created, using the current date (1/3/23) and subtracting one to obtain the dates. The formula used was =A2-1.

To pull data from the specific fund and retrieve the desired amounts for each date, the following formula was utilized: =IFERROR(VLOOKUP($A2,$H$2:$I$3525,2,FALSE),""). This formula accounts for missing values, resulting in blank cells.

Subsequently, the data was filtered to identify any zero values, which were then changed to blank cells to prevent skewing the data.

Upon completing the table, only the values were copied and pasted.

Comparing Data
Tab SP500
A CAGR (Compound Annual Growth Rate) table was created to illustrate previous years' growth. The formula employed was =($E$7/$E$6)^(1/E14)-1. This calculates the CAGR by taking the current year's fund divided by the previous year, raising it to the power of the reciprocal of the number of years, and subtracting 1.

The trendline indicates predictability.

Tab BTC
Similar to the SP500, a tab for BTC was created. A new column comparing the CAGR of SP500 and BTC was added with the formula =D15/'SP500'!$D$12.

The trendline suggests unpredictability and high volatility.

Tab SP500_BTC
A table was generated to simulate the growth of a $1 investment from the beginning of the data. The formula used was =B3001/$B$3001. This involves dividing the earliest date's value by the value on the same date, and the results show the change in the dollar's value over time.

The chart indicates the dollar staying relatively constant for SP500, while for BTC, it grew to over $7000.

Tab Cryptos
This tab compares BTC, ETH, and LTC. The data is graphed for all three coins, with ETH and LTC graphed on a second axis to showcase their performance against BTC. A test from 2016 to 1/5/23 indicates that ETH outperformed BTC.

Tab Cryptos vs SP 500
This tab compares the SP500 against the combined amounts of BTC, ETH, and LTC. After comparison, the Crypto coins outperformed the S&P 500 by 3000%.

