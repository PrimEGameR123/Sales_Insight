# Sales Insight
<h3> Motive </h3>
Our case study is based on a computer hardware business which is facing challenges in tracking the sales in dynamically changing market. 
<h3> Process </h3>
Director decides to invest in data analysis project and he would like to build power BI dashboard that can give him real time sales insights to take data driven decisions. <br>
<h6> Commands Used </h6>

1. Show all customer records

    `SELECT * FROM sales.customers;`
    `SELECT * FROM customers;`

2. Show total number of customers

    `SELECT count(*) FROM sales.customers;`
    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM sales.transactions where market_code='Mark001';`
    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM sales.transactions where market_code='Mark001';`
    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from sales.transactions where currency="USD"`
    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT sales.transactions.*, sales.date.* FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020;`
    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020;`
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`

1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(sales.transactions.sales_amount) FROM sales.transactions INNER JOIN sales.date ON sales.transactions.order_date=sales.date.date where sales.date.year=2020
and sales.transactions.market_code="Mark001";`
    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`

<h3> Result </h3>
Data Analysis Using Power BI
https://drive.google.com/file/d/1F0GmST-ULaNXBrSBNTgAPHIO_Vy7ZYxL/view
