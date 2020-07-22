<b>SELCECT</b> is the word that will pick all the columns has stated
<pre>
SELECT
  unit_price,
  name,
  amount
</pre>
<p>it will show up the data of unit_price, name and amount columns</p>

<b>AS</b> is the keyword that setting the title for the column
<pre>
SELECT
  unit_price,
  name,
  amount
  unit_price * 10 * 0.9 AS "discount price"
</pre>
<p>it will show up as discount price instead of <i> unit_price * 10 * 0.9</i>and the data inside will calculate as the unit_price * 10 * 0.9</p>

<b>WHERE</b> is a keyword which is similar to the if else, setting a condition to show up the data that fullfill the requirement
<pre>
SELECT * WHERE  unit_price > 10
</pre>
<p>it will only show the items which unit_price larger than 10</p>

