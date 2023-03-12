## Analysis of World Bank using PostgreSQL

**Project description:** In this project, I pretended I was hired by the World Bank as a Data Analyst. I was tasked with using PostgreSQL to filter through the International Development Association's (IDA) historical data - their statement of grants and credits.

Be sure to connect with me on LinkedIn or check out my other projects using the two links at the bottom left. 

The data used for this analysis can be found **[here](https://finances.worldbank.org/Loans-and-Credits/IDA-Statement-Of-Credits-and-Grants-Historical-Dat/tdwh-3krx)**! For this project, the data was last updated February 14, 2023 and was created April 20, 2011. The data is United States Dollars.


### What was analyzed?

When analyzing the data, I wanted to start big picture and then focus in on the country that borrows the most from the World Bank. The questions I was looking to answer are:
  1. How many different countries have borrowed from the World Bank?
  2. How many total transactions has the World Bank made?
  3. What is the total due to the IDA?
  4. What are the top 5 countries for total transactions?
  5. What are the top 5 countries that owe the most to the IDA?
  6. What are the most expensive projects within the country who owes the most to the IDA, how much have they repaid towards those projects?

### By the Numbers

  1. There are **137 different countries** that have borrowed from the World Bank.
  2. There are **2.28 Million** total transactions made between 137 countries and the World Bank over the course of 12 years.
  3. The total or sum owed to the IDA is over **$41 Trillion dollars**! The exact amount is $41,426,949,353,203.46.
  4. The top 5 countries for total transactions are India, Bangladesh, Pakistan, Tanzania, and Ghana.
  5. The top 5 countries that owe to IDA the most are India, Bangladesh, Pakistan, Vietnam, and Nigeria.
  6. The top 5 most expensive projects within India is the National Rural Livelihoods Project 5 separate times.

### The Analysis

To find that there are 137 distinct countries that have borrowed from the World Bank, I used the query below counting the number of distinct countries.

<img src="images/number of countries.PNG?raw=true"/>


