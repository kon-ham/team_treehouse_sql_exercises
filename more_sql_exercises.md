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

- What is the most common type of JOIN?
    `INNER JOIN`

- What is a JOIN?
    `It is how a SQL query combines data from two tables into one result set`

- A left outer join returns all data from the first -- or left -- table and only the data with matches in the second table.
    `True`

- Which is the valid SQL statement with JOIN
    ```
    SELECT *
    FROM TableA
    INNER JOIN TableB ON TableA.ColumnID = TableB.ColumnID
    ```
- In a car database there is a Model table with columns, ModelID, MakeID and ModelName and a Car table with columns, CarID, ModelID, VIN, ModelYear and StickerPrice.

    For all cars in the database, show Model Name, VIN and Sticker Price in one result set.

        ```
        SELECT ModelName, VIN, StickerPrice
        FROM Model
        INNER JOIN Car ON Model.ModelID = Car.ModelID;
        ```

- In a car database there is a Make table with columns, MakeID and MakeName, a Model table with columns, ModelID, MakeID and ModelName and a Car table with columns, CarID, ModelID, VIN, ModelYear and StickerPrice.

    For all cars in the database, show Make Name, Model Name, VIN and Sticker Price from the Model and Car tables in one result set.

        ```
        SELECT MakeName, ModelName, VIN, StickerPrice
        FROM Make
        INNER JOIN Model ON Make.MakeID = Model.MakeID
        INNER JOIN Car on Model.ModelID = Car.ModelID;
        ```
- In a car database there is a Sale table with columns, SaleID, CarID, CustomerID, LocationID, SalesRepID, SaleAmount and SaleDate. The database also has a SalesRep table with columns, SalesRepID, FirstName, LastName, SSN, PhoneNumber, StreetAddress, City, State and ZipCode.

    Show the First and Last Name of each sales rep along with SaleAmount from both the SalesRep and Sale tables in one result set.

        ```
        SELECT FirstName, LastName, SaleAmount
        FROM Sale
        INNER JOIN SalesRep ON Sale.SalesRepID = SalesRep.SalesRepID;
        ```

- In a car database there is a Model table with columns, ModelID, MakeID and ModelName and a Car table with columns, CarID, ModelID, VIN, ModelYear and StickerPrice.

    Show all Model names from the Model table along with VIN from the Car table. Make sure models that aren’t in the Car table still show in the results!

        ```
        SELECT ModelName, VIN
        FROM Model
        LEFT OUTER JOIN Car ON Model.ModelID = Car.ModelID;
        ```

- In a car database there is a Sale table with columns, SaleID, CarID, CustomerID, LocationID, SalesRepID, SaleAmount and SaleDate. The database also has a SalesRep table with columns, SalesRepID, FirstName, LastName, SSN, PhoneNumber, StreetAddress, City, State and ZipCode.

    Show all SaleDate, SaleAmount, and SalesRep First and Last name from Sale and SalesRep. Make sure that all Sales appear in results even if there is no SalesRep associated to the sale.

        ```
        SELECT SaleDate, SaleAmount, FirstName, LastName
        FROM Sale
        LEFT OUTER JOIN SalesRep ON Sale.SalesRepID = SalesRep.SalesRepID;
        ```

- Which Operator eliminates duplicates while combining multiple data sets into one result set?
    `Union operator`

- Which Set Operation is used to return only the results that are NOT in another table?
    `Except operator`

- It is valid to have fewer columns in the query that comes after the UNION operation.
    `False. (They must be equal)`

- There are two tables Fruit and Vegetable table. The Fruit table has a FruitID and a Name column and the Vegetable table has a VegetableID and Name column.

    Create a distinct result set of fruit and vegetable names.

        `SELECT Name FROM Fruit UNION SELECT Name FROM Vegetable;`

- There are two tables Fruit and Vegetable table. The Fruit table has a FruitID and a Name column and the Vegetable table has a VegetableID and Name column.

    Create a list of all fruits and vegetables starting with the letters A through K . In other words all fruit and vegetables that don't start with the letter L to Z.

        ```
        SELECT Name FROM Fruit 
            WHERE Name < "L"
        UNION 
        SELECT Name FROM Vegetable
            WHERE Name < "L";
        ```

- There are two tables Fruit and Vegetable table. The Fruit table has a FruitID and a Name column and the Vegetable table has a VegetableID and Name column.

    Create a list of fruits and vegetables that includes any potential duplicate values. Ensure that it is in alphabetical order so that the duplicates are next to each other!

        ```
        SELECT Name FROM Fruit
        UNION ALL
        SELECT Name FROM Vegetable
        ORDER BY Name;
        ```

- There are two tables Fruit and Vegetable table. The Fruit table has a FruitID and a Name column and the Vegetable table has a VegetableID and Name column.

    Create an alphabetical list of produce that is considered both a fruit and a vegetable.

        ```
        SELECT Name FROM Fruit
        INTERSECT
        SELECT Name FROM Vegetable
        ORDER BY Name;
        ```

- There are two tables Fruit and Vegetable table. The Fruit table has a FruitID and a Name column and the Vegetable table has a VegetableID and Name column.

    Create an alphabetical list of fruits that are NOT considered a vegetable.

        ```
        SELECT Name FROM Fruit
        EXCEPT
        SELECT Name FROM Vegetable
        ORDER BY Name;
        ```

- There are two tables Fruit and Vegetable table. The Fruit table has a FruitID and a Name column and the Vegetable table has a VegetableID and Name column.

    Create an alphabetical list of vegetables that are NOT considered a fruit.

        ```
        SELECT Name From Vegetable
        EXCEPT 
        SELECT Name FROM Fruit
        ORDER BY Name;
        ```

- Why must a derived table be aliased?

    `Because a derived table is temporary, it must be aliased because it has no name. Because it has no name, the database wouldn't be able to reference its data set.`