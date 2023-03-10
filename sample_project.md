## Analysis of World Bank using PostgreSQL

<img src="images/world-bank-logo.jpg?raw=true"/>

**Project description:** In this project, I pretended I was hired by the World Bank as a Data Analyst. I was tasked with using PostgreSQL to filter through the International Development Association's (IDA) historical data - their statement of grants and credits.

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

<img src="images/number of countires.PNG?raw=true"/>

Next, I wanted to find the total number of transactions the World Bank made with all 137 of those countries. I ran a count all query.

<img src="images/total transactions.PNG?raw=true"/>

This returned **2,280,240 total transactions**!

Then, I wanted to see the total amount still owed to the IDA out of those 2.28 Million transactions. I used the query below summing all individual Due to IDA balances.

<img src="images/total due to ida.PNG?raw=true"/>

This returned exactly **$41,426,949,353,204.69! Over $41 Trillion USD is owed to the IDA!**

Now, I wanted to dig into the large number owed to the IDA. I wanted to specifically find the single country that owes the most and its largest projects. To do that, I first wanted to find the top 5 countries for both number of transactions and amount due to IDA.

I discovered the top 5 countries for total transactions using the below query.

<img src="images/NUmber of Transacations by country SQL.PNG?raw=true"/>
<img src="images/NUmber of Transacations by country DATA.PNG?raw=true"/>

It can be seen here that the **country with the most transactions is India with 119,318 transactions**. India is then followed by Bangladesh, Pakistan, Tanzania, and Ghana.

I then found the top 5 countries in amount "Due to IDA" using this query.

<img src="images/amount due to IDA per country SQL.PNG?raw=true"/>
<img src="images/amount due to IDA per country DATA.PNG?raw=true"/>

It can be seen that again **India is at the top with $6,808,932,727,490.81 due to the IDA**, followed by Bangladesh and Pakistan. This makes sense because these are also the top 3 countries in total amount of transactions. The fourth and fifth countries with the most Due to IDA were Vietnam and Nigeria.

I then wanted to analyze India more because it ranked number 1 in both transactions and amount due to IDA. I decided I wanted to see what India's 5 most expensive projects were, and how much they have paid back so far on those projects.

<img src="images/India Most Expensive 5 Projects SQL.PNG?raw=true"/>
<img src="images/India Most Expensive 5 Projects DATA.PNG?raw=true"/>

I found that all 5 of India's biggest projects were for the National Rural Livelihoods Project. All 5 projects had an initial principal amount of $1,000,000,000. India has also only partially paid back 3 out of those 5 projects.

### Findings

Over the course of **12 years**, **137 countries** have totaled **2.28 Million transactions** and **owe over $41 Trillion dollars to the IDA**!
India, Bangladesh, and Pakistan rank exactly 1,2,3 in both total number of transactions and amount due to the IDA.
From **119,318 transactions, India owes $6,808,932,727,490.81 to the IDA.**
India's 5 largest projects all original borrowed **$1 Billion dollars each** - but India has only repaid **$90,820,178** on those 5 projects - roughly **1.8%**.

### Interested In More?

This was for educational and practice purposes only. I do not own any of the data used here.
Thank you for reading my World Bank Analysis project using PostgreSQL!
I would love any feedback.
Let's connect on LinkedIn at the link to the bottom left of this page - and take a look at my other projects back in my portfolio in the link using my name at the top left of this page!
