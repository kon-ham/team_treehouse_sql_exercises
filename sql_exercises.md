 - In the e-commerce database we have a  `products`  table. The columns
   are  `id`,  `name`,  `description`  and  `price`.
   
   Find all the products where the pattern 't-shirt' can be found
   anywhere in the product name.

		`SELECT * FROM products WHERE name LIKE "%t-shirt%";`