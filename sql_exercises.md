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

- Fill in the missing keywords for the following UPDATE statement.

    ____ cars ____ model = "Ford" ____ id = 1;

        `Answer: UPDATE, SET, WHERE`

- We have an eCommerce database and it has a products table. It has the columns id, name, description and price.

    Delete all products priced at 11 or higher!

        `DELETE FROM products WHERE price >= 11;`

- The same eCommerce database has a users table. It has the columns id, username, password, first_name, and last_name.

    Delete the user with the username of poley_hands.

        `DELETE FROM users WHERE username = "poley_hands";`

- Now we're using a database from a smartphone. It has a phone_book table. It has the columns id, first_name, last_name and phone.

    Delete all contacts with the first name of Jonathan and last name of Luna.

        `DELETE FROM phone_book WHERE first_name = "Jonathan" AND last_name = "Luna";`

- Imagine you're a developer on a smartphone with an embedded database. There's a phone_book table with the fields, first_name, last_name and phone. Write the SQL query to order first by last_name and then by first_name in alphabetical order.

    Select all columns.

        `SELECT * FROM phone_book ORDER BY last_name ASC, first_name ASC;`

- In a library database there's a books table. There's a title, author, genre and first_published column.

    Order the books by the most recently published books at the top. Select all columns.

        `SELECT * FROM books ORDER BY first_published DESC;`

- We're still using the library database there's a books table. There's a title, author, genre and first_published column.

    Order all books by Genre and then by Title. Select all columns.

        `SELECT * FROM books ORDER BY genre ASC, title ASC;`

- We're using the library database again. There's a books table. There's a title, author, genre and first_published column.

    Write a query to obtain the first 5 books in the Fantasy genre ordered by the year released. Oldest first. Select all columns.

        `SELECT * FROM books WHERE genre = "Fantasy" ORDER BY first_published ASC LIMIT 5;`

- We're still using the library database with the books table. There's a title, author, genre and first_published column.

    Find the earliest Science Fiction book in our library. Only one result should be returned. All columns should be selected.

        `SELECT * FROM books WHERE genre = "Science Fiction" ORDER BY first_published ASC LIMIT 1;`

- In a library database there's a books table. There's a title, author, genre and first_published column.

    The library database is connected to a website displaying 10 books at a time, sorted by the title alphabetically.

    Write a query to bring back the second page of results. Please retrieve all columns of information.

        `SELECT * FROM books ORDER BY title ASC LIMIT 10 OFFSET 10;`

- Imagine you're developing a Contacts application on a phone. You have a database with a phone_book table. It has the columns, first_name, last_name and phone.

    The phone has a technical limitation to show 20 contacts on a screen at a time. Write the SQL query to retrieve the 3rd page of results from the phone_book table. Contacts are ordered by last name and then first name.

        `SELECT * FROM phone_book ORDER BY last_name ASC, first_name ASC LIMIT 20 OFFSET 40;`

- In the library database there's a patrons table listing all the users of the library. The columns are id, first_name, last_name, address, email, library_id and zip_code.

    Generate a list of strings that are in the following format: Andrew Chalkley <andrew@teamtreehouse.com>. Concatenate the first name, last name and email address for all users.

    Alias it to to_field. This will be used in the "To" field in email marketing.

        `SELECT first_name || ' ' || last_name || ' ' || '<' || email || '>' AS to_field FROM patrons;`

- In an ecommerce database there's a addresses table. There is an id, nickname, street, city, state, zip, country and user_id columns.

    Concatenate the street, city, state, zip and country in the following format. street, city, state zip. country e.g. 34 NE 12 st, Portland, OR 97129. USA

    Alias the concatenated string as address

        `SELECT street || ', ' || city || ', ' || state || ' ' || zip || '. ' || country AS address FROM addresses;`

- In the library database there's a books table with the columns id, title, author, genre and first_published.

    Find the book with the longest title. Show the title and then the length. Alias the result of the length calculation to be longest_length. Only retrieve the longest book.

        `SELECT title, LENGTH(title) AS longest_length FROM books ORDER BY longest_length DESC LIMIT 1;`

- In a library database there's a books table. There's an id, title, author, genre and first_published column.

    Write a query that will return only the title and author. Bring back the title in lowercase and the author in uppercase. Alias them as lowercase_title and uppercase_author respectively.

        `SELECT LOWER(title) AS lowercase_title, UPPER(author) AS uppercase_author FROM books;`

- In the library database there's a patrons table with the columns id, first_name, last_name, address, email, library_id, and zip_code.

    The library is generating new library cards that will display the full name and their library ID. The full name needs to have the last name in all caps. Create a report with two columns of results, one is an alias of full_name the second being the library_id.

        `SELECT first_name || ' ' || UPPER(last_name) AS full_name, library_id FROM patrons;`

- In the library database, how many books are in the genre of "Science Fiction"?

---



    Alias the result as scifi_book_count.

    The books table has the columns id, title, author, genre and first_published.

        `SELECT COUNT(*) AS scifi_book_count FROM books WHERE genre = "Science Fiction";`

- In the library database, how many books are by the author of "J.K. Rowling"?

    Alias the result as jk_book_count.

    The books table has the columns id, title, author, genre and first_published.

        `SELECT COUNT(*) AS jk_book_count FROM books WHERE author = "J.K. Rowling";`

- In the library database there's a books table. There are id, title, author, genre and first_published columns.

    Count all the books in each genre. Include the genre column first and the genre_count as the second column of information.

        `SELECT genre, COUNT(*) AS genre_count FROM books GROUP BY genre;`

- In the library database there's a books table. There are id, title, author, genre and first_published columns.

    Write a query to count all the unique genres in the books table. Alias it as total_genres.

        `SELECT COUNT(DISTINCT genre) AS total_genres FROM books;`

- We're in a movie database. There's a reviews table with the columns of id, movie_id, username, review and rating.

    The movie "Starman" has the id of 6. Movie ids are found in the movie_id column in the reviews table. Write a query that totals up all ratings for the movie "Starman" in the reviews table. Alias it as starman_total_ratings.

        `SELECT SUM(rating) AS starman_total_ratings FROM reviews WHERE movie_id = 6;`

- We're in a movie database. There's a reviews table with the columns of id, movie_id, username, review and rating.

    The movie "Starman" has an id of 6. Movie ids are stored in the movie_id column. Calculate the average rating for "Starman". Alias the average as average_rating.

        `SELECT AVG(rating) AS average_rating FROM reviews WHERE movie_id = 6;`

- We're in a movie database. There's a reviews table with the columns of id, movie_id, username, review and rating.

    The movie "Starman" has an id of 6. Movie ids are stored in the movie_id column. Calculate the minimum and maximum ratings for "Starman". Alias them as star_min and star_max.

        `SELECT MIN(rating) AS star_min, MAX(rating) AS star_max FROM reviews WHERE movie_id = 6;`

- In an ecommerce database we have a products table with the columns id, name, category, description, price and stock_count.

    The price is in USD. Write a query that returns the product name and price in Pounds Sterling (GBP). The current exchange rate is 1.4 USD to every 1 GBP. Alias the calculated price to price_gbp. Round to two decimal places.

        `SELECT name, ROUND(price / 1.4, 2) AS price_gbp FROM products;`

- In an ecommerce database there's an orders table with the columns id, product_id, user_id, address_id, ordered_on, status and cost.

    Count the total number of orders that were ordered today and have the status of 'shipped'. Alias it to shipped_today.

        `SELECT COUNT(*) AS shipped_today FROM orders WHERE status = 'shipped' AND ordered_on = DATE("now");`

- In an ecommerce database there's an orders table with the columns id, product_id, user_id, address_id, ordered_on, status and cost.

    Count the total number of orders that were ordered yesterday and have the status of 'shipped'. Alias it to ordered_yesterday_and_shipped.

        `SELECT COUNT(*) AS ordered_yesterday_and_shipped FROM orders
        WHERE ordered_on = DATE("now", "-1 days")
        AND status = 'shipped';`

- In a movies database we have a movies table. It has the columns of id, title, date_released and genre.

    Write a query that returns the title first and the month and year it was released alias as month_year_released. Dates should look like "04/1983" for April 1983.

        `SELECT title, STRFTIME("%m/%Y", date_released) AS month_year_released FROM movies;`