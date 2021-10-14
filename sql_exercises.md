 - In the e-commerce database we have a  `products`  table. The columns
   are  `id`,  `name`,  `description`  and  `price`.
   
   Find all the products where the pattern 't-shirt' can be found
   anywhere in the product name.

		`SELECT * FROM products WHERE name LIKE "%t-shirt%";`

 - In the  `users`  table we have the columns  `id`,  `username`,  `password`,  `first_name`  and  `last_name`.

	Find all users with the first name starting with the letter "L".

		`SELECT * FROM users WHERE first_name LIKE "L%";`

- We're back on the smartphone, but our  `phone_book`  is a mess. There's a  `phone_book`  table but there's missing information in a couple of the columns.

	The phone_book has the following columns  `id`,  `first_name`,  `last_name`  and  `phone`.

	Find all contacts in the  `phone_book`  where the phone number is missing so we can go and ask them for their 			number.

		`SELECT * FROM phone_book WHERE phone IS NULL;`

- We're still using the  `phone_book`, with the columns  `id`,  `first_name`,  `last_name`  and  `phone`.

	Imagine we're implementing the autocomplete feature for a search facility on the phone where a user can start typing a last name and suggestions will appear. Write a query to retrieve all values from the last name column where the last name value is present. Only retrieve the  `last_name`  column.

		`SELECT last_name FROM phone_book where last_name IS NOT NULL;`

- If I wanted to return rows that match either conditions, which keyword would I use?

    `SELECT <columns> FROM <table> WHERE <condition 1> OR <condition 2>;` 

- Which keyword could you use to rewrite this query in a shorter form?

    SELECT <columns> FROM <table> WHERE <column 1> = <value 1> OR <column 1> = <value 2> OR <column 1> = <value 3>;  

    Answer: `IN`

- You have a table full of words. You want to find all words ending with the `tion` at the end.

    Which query would most likely display the correct results?

    `SELECT word FROM words WHERE word LIKE "&tion";

- What's missing from this query to find all contacts without a phone number?

    SELECT * FROM contacts WHERE phone ___________ NULL;

    Answer: `IS`

