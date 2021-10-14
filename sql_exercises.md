 - In the e-commerce database we have a  `products`  table. The columns
   are  `id`,  `name`,  `description`  and  `price`.
   
   Find all the products where the pattern 't-shirt' can be found
   anywhere in the product name.

		`SELECT * FROM products WHERE name LIKE "%t-shirt%";`

 - In the  `users`  table we have the columns  `id`,  `username`,  `password`,  `first_name`  and  `last_name`.

	Find all users with the first name starting with the letter "L".

		`SELECT * FROM users WHERE first_name LIKE "L%";`