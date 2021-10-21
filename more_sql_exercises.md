- What is normalization?
    `The process of designing a relational database.`

- What is a "set"
    `A collection of things that have common properties`

- What is the name of the type of diagram that represents a set?
    `A Venn Diagram`

- A Primary Key will allow one NULL value, but no more than that.
    `False. (Primary keys are non-null keys)`

- What data type does a primary key have to be?
    `Either, (Integer or Text) as long as the value guarantees uniqueness`

- What happens when a Unique Constraint is violated in a database system?
    `The database does not allow the data to be written to the table and an error is returned`

- Which of the following is NOT something a database key can do?
    `Guarantee a table does not return data when queried unless a specific password is supplied`

- What are Foreign Keys?
    `They are columns that contain data which relate to the Primary Key in another table`

- Once a Foreign Key Constraint is created to enforce the referential integrity between two tables, what happens if you try to insert a value that does NOT exist in the primary key table?
    `It will NOT insert the data, and will return an error`

- The thing that defines the physical relationship between two tables in a database is called:
    `Foreign Key Constraint`

- If NO Foreign Key Constraint exists between two tables, it is possible to accidentally record data in a foreign key column that does not have a matching value in the primary key table.
    `True`

- Which relationship type is the most common in a relational database?
    `One to Many`

- What do we do to handle a Many to Many relationship between tables during the design process?
    `Add a third table between the original tables`

- Where does the INNER JOIN clause go in a SQL statement?
    `After FROM clause but before WHERE clause`