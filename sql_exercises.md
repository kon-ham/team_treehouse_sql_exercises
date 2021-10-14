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