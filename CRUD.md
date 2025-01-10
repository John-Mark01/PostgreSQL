# Basic CRUD in PostgreSQl

C - create

R - read

U - update

D - Delete

### ```1. SELECT``` 

- in postgreSQL ```SELECT``` is the way we ```read``` data.
- ```*``` (asterix) is the wild card. It represents every record.

#### Commands / Query's
``` SELECT * FROM table_name``` - Returns every recod from a table 

``` SELECT column_name, column_name FROM table_name``` - Returns a new table with all records filled with the columnns we have specified

#### Concatenation
  - we can concatenate two columns with ```concat()``` function - ```concat(first_name, ' ', last_Name) AS "Full Name";```

#### Alias's - Transforms the name of the columns and tables with ```""```

    ```
        SELECT
        column_name1 AS "FirstName", 
        column_name2 AS "LastName
        FROM table_name AS newName
    ```
  - we can change the refference name of a table or column in a Query. This change will not affect the table itself!
    

