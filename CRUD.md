# Basic CRUD in PostgreSQL

C - create

R - read

U - update

D - Delete

# ```1. SELECT``` 

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

#### Get records with a limit (n)
- whatever we specify as ```n``` only ```n number``` of records will be returned
- 
 ```
        SELECT
            *
        FROM table_name LIMIT 10
  ```
## Sorting 
- we get columns
- we can sort a result, with the keywords ```ORDER BY column_name ASC```
  - accending - ```ASC```
  - descending - ```DESC```
  - by default the order is ```ASK```

```
        SELECT
            *
        FROM table_name
        ORDER BY first_name
        LIMIT 10
  ```

## Filtering 

#### ```DISTINCT```
- we get records
- we can filter all records, by removing all repeating records with - ```DISTINCT```
  
```
        SELECT
            DISTINCT department
        FROM employees
        ORDER BY department
  ```

#### ```DISTINCT ON```
- if will filter repeating records only on the specified column.
- will return the records ordered by the column, specified.
  
```
        SELECT
            DISTINCT ON (first_name), department
        FROM employees
 ```

#### ```WHERE```

##### ```Comparison Operators```
- will filter a column by a condition - ``` WHERE column_name = condition```
- the condition can be with any operator ```<, <=, >, >=, =, !=```

```
        SELECT
           department
        FROM employees
        WHERE department = 'Development'
 ```

##### ```Logical Operators```
- we filter records by more advanced conditions
- we can use ```AND(&&), OR(||), NOT(!)
- works like an if statement - ```WHERE (record from column_name = 'Development' AND ... = 'Sales')```

```
        SELECT
            first_name,
            last_name,
            gender
        FROM employees
        WHERE (department = 'Development' AND department = 'Sales')
 ```

#### ```BETWEEN```
- we give integers as limits and will return every record in between the limits

``` WHERE salary BETWEEN 5000 AND 7000;```

#### ```IN, NOT IN```
-  will return records that return YES(true) to the parameter
-  if the record is ```IN```

```
        SELECT
            first_name,
            last_name,
            gender
        FROM employees
        WHERE department IN('Development)
        ORDER BY department
 ```

#### ```Create a new table from existing records```
- will create a new table with the values specified, from another table

```
CREATE TABLE table_name AS
SELECT (
        id,
        first_name,
        last_name
)
FROM other_table_name;

```


# ```2. INSERT``` 
- it is the way we add data into our database
- we say ```INSERT``` followed by ```INTO```, and then where we are inserting.
- if we don't specify columns, we need to insert a whole record, which is all columns.

```
INSERT INTO table_name
VALUES('value', 'value');

```

- we can add parameters. The value set, and parameters given needs to be in same order.

```
INSERT INTO table_name(first_name, last_name)
VALUES(
    'John',
    'McDonald'
);

```

#### ```BULK INSERT```
- we can also insert more than one record to a table

```
INSERT INTO table_name(first_name, last_name)
VALUES
('John', 'McDonald')    -- new record
('Mark', 'Commer')      -- new record
('Steven', 'Hewbert')   -- new record
;

```


# ```3. UPDATE``` 
- it is the way we update the data in our database
- we say ```UPDATE``` followed by a table_name, and then ```SET```, and then where we are inserting.
  
#### when we make updates we always add the ```WHERE``` clause.
- if we don't add a ```WHERE``` clause, _ALL RECORDS_ will update!

```
UPDATE table_name
SET salary = 100
WHERE department = 'Development' -- ABSOLUTELY NECESARY!
;

```

#### ```Multiple UPDATE```

```
UPDATE table_name
SET salary = salary * 1.3
WHERE department = 'Development' AND department = 'Backend'
;

```


# ```4. DELETE``` 
- it is the way we delete data from our database

