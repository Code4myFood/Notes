# Basic MYSQL notes

<b>SELCECT</b> is the word that will pick all the columns has stated
<pre>
SELECT
  unit_price,
  name,
  amount
</pre>
<p>it will show up the data of unit_price, name and amount columns</p>
<br />
<b>AS</b> is the keyword that setting the title for the column
<pre>
SELECT
  unit_price,
  name,
  amount
  unit_price * 10 * 0.9 AS "discount price"
</pre>
<p>it will show up as discount price instead of <i> unit_price * 10 * 0.9</i>and the data inside will calculate as the unit_price * 10 * 0.9</p>
<br />
<b>WHERE</b> is a keyword which is similar to the if else, setting a condition to show up the data that fullfill the requirement
<pre>
SELECT * WHERE  unit_price > 10
</pre>
<p>it will only show the items which unit_price larger than 10</p>
<br />
<b>AND</b> and <b>OR</b> is the keyword in MYSQL instead of using && and ||
<pre>
SELECT * WHERE  unit_price > 10 AND amount > 1000
</pre>
<p>it will only show the items which unit_price larger than 10 <strong>and</strong> amount is over 1000</p>

<pre>
SELECT * WHERE  unit_price > 10 OR amount > 1000
</pre>
<p>it will only show the items which unit_price larger than 10 <strong>or</strong> amount is over 1000</p>

<pre>
SELECT * WHERE  unit_price > 10 OR amount > 1000 and name = 'ABC'
</pre>
<p>AND hava a higher order than or so it will look into the amount > 1000 and name = 'ABC' part first</p>
<p>which same as 
SELECT * WHERE  unit_price > 10 OR (amount > 1000 and name = 'ABC')</p>

<br />
<b>NULL</b> is the operator which there is a missing data
<br />

<b>LIKE</b> is the operator show the string have specific pattern
<pre>
SELECT *
FROM table
WHERE last name LIKE 'b%'
</pre>
<p>it will show the word starting with b</p>
<p>% means there is any digit after the character and _ meant exact one digit after the character</p>
<br />

<b>REGEXP</b> is the operator show the string have specific pattern like the advance LIKE operator
<pre>
SELECT *
FROM table
WHERE last_name REGEXP "field$|mon|rose"
</pre>
<ul>
  <li>| logical or</li>
  <li>$ end$</li>
  <li>^ ^begin</li>
  <li>[abcd]</li>
  <li>[a-h]</li>
</ul>
<br />
<b>ORDER BY</b>is the operator for sorting 
<pre>
SELECT *
FROM table
ORDER BY name
</pre>
<p>the order will sorted by the name</p>
<b>DESC</b> is the operator means decending order
<pre>
SELECT *
FROM table
ORDER BY name DESC
</pre>
<p>the order is sorted in descending order</p>
<pre>
SELECT *
FROM table
ORDER BY name, age
</pre>
<p>the data will sort in name first if the name is same then the order will be sorted in age</p>
<br />
<b>LIMIT</b>is the operator to set the number of data return 
<pre>
SELECT *
FROM table
LIMIT 3
</pre>
<p>only the first three data will return to the user</p>
<br/>
<pre>
SELECT *
FROM table
LIMIT 5,3
</pre>
<p>only the first five data will be skipped, which data 6, 7, 8 will return to the user</p>
<br />
<b>BETWEEN</b> is the operator for the value in range
<pre>
SELECT *
FROM table
WHERE amount BETWEEN 0 and 10
</pre>
<p>the data which teh amount is within 0 to 10 will be returned</p>
<br />
<b>INNER JOIN</b> is the operator that link two table together
<pre>
SELECT customer.Name, order.OrderID
FROM customers
INNER JOIN order 
ON orders.customer_id = customers.customer_id
</pre>
<p>if the data have the same customer_id in customers table and orders table. THhe customer Name will in the same row with the OrderID</p>
<br />


