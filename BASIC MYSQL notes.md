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
