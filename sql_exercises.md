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

- I want to categorize products by price on a website. Cheap is defined by the prices from 0.01 and 9.99. Enter the missing keywords.

    `SELECT name, description FROM products WHERE price BETWEEN 0.01 AND 9.99;`

- We have an eCommerce database and it has a products table. It has the columns id, name, description and price.

    Add a new product to the products table. Use any valid values you want. All columns are required. The id column is auto incrementing.

        `INSERT INTO products (id, name, description, price) VALUES (NULL, "Tee Hee", "Sour Candies", 4.99);`

- The same eCommerce database has a users table. It has the columns id, username, password, first_name, and last_name.

    Add a new user to the users table. Use any valid values you want. All columns are required. The id column is auto incrementing.

    (Don't enter a real password you'd really use!)

        `INSERT INTO users (id, username, password, first_name, last_name) VALUES (NULL, "zzzxxx", "123abc", "Johnny", "Appleseed");`

- Now we're using a database from a smartphone. It has a phone_book table. It has the columns id, first_name, last_name and phone.

    Add a new contact to the phone_book table. Use any valid values you want. All columns are required. The id column is auto incrementing.

        `INSERT INTO phone_book (id, first_name, last_name, phone) VALUES (NULL, "Johnny", "Appleseed", "123-123-1234");`

- How many rows will this statement insert in to the cars table?

    INSERT INTO cars (make, model) VALUES ("Fiat", "Fiat 500"),
    ("Fiat", "Fiat Multipla"),
    ("Cadillac", "Cadillac Fleetwood"),
    ("Cadillac", "Cadillac Eldorado");

        `Answer: 4`

- What character should you replace the ? with to create a valid INSERT statement?

    INSERT INTO awesome_people (first_name, last_name) VALUES ("Grace", "Hopper")? ("Ada", "Lovelace");

        `Answer: ,`

-  What does the acronym CRUD stand for?

    `Create, Read, Update, Delete`

- Given the database table imaged above, how would you complete this INSERT statement.


    INSERT INTO countries (population, _____) VALUES (4596700, "New Zealand");

        `Answer: name`

- Fill in the missing keywords:

    INSERT  tv_shows (show, network)  ("Super Girl", "CBS");

        `Answer: INSERT INTO tv_shows (show, network) VALUES ("Super Girl", "CBS");`

- We have an eCommerce database and it has a products table. It has the columns id, name, description and price.

    The warehouse is closing down. There's a clearance sale and all products need to be priced 0.99.

        `UPDATE products SET price = "0.99";`

- Now we're using a database from a smartphone. It has a phone_book table. It has the columns id, first_name, last_name and phone.

    Update all contacts to have the first name of "Mystery" and last name of "Person".

        `UPDATE phone_book SET first_name = "Mystery", last_name = "Person";`

- UPDATE shows SET title =  "Friends";

    What's the missing operator?

        `Answer: = `

