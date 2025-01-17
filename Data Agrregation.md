# Data Agrregation
- combining multiple elements with a common property
- its done in SQL by ```GROUPING```
- can be used only with ```SELECT``` 



## Grouping - ```GROUP BY``` 

<img width="871" alt="image" src="https://github.com/user-attachments/assets/e676cf0c-ab00-4561-9b01-ed1da682e500" />

- allows taking data into ```separate groups``` based on a common property
- grouping will take all records from a column that we group with, and will return only the ```DISTINCT```(non repeating) records.
- all records that are repeating, they will be combined, and will be returned as one record.
- we always group by all columns we SELECT in our Query. If you SELECT first_name, last_name, we need to ```GROUP BY``` those two columns.

**From departments: Development, Support, HR, Development, HR, HR, if we group our query by departments, it will return -> (Development, Support, HR)**

<img width="256" alt="image" src="https://github.com/user-attachments/assets/b511b9e4-8c70-427b-bf28-c0a47d51d804" />


- we can group more than one column.

<img width="310" alt="image" src="https://github.com/user-attachments/assets/d14488cc-1d73-48e9-8501-c03159fb75b0" />

## Agrregate Functions ```MIN```, ```MAX```, ```AVG```, ```COUNT```, ```SUM```

- they are used after grouping.
- USED TO OPERATE OVEr ONE or MORE groups performing data analysis
- they can be used on all groups we create
- if we SELECT only a a agrregate function with a column, we don't need to group the query.
- ALIAS can be added

<img width="1321" alt="image" src="https://github.com/user-attachments/assets/8270da78-33ed-4abf-8e6c-5b220fdb9879" />


### ```COUNT```
- takes all combined records from grouping
```count(*)``` will count all records from a table. Will return all values that are not NULL.
- all columns that are NOT aggregated on, must be grouped!
- count must be placed AT THE END of the SELECT statement, and before 

<img width="327" alt="image" src="https://github.com/user-attachments/assets/63ccc50a-d532-4cd7-b78f-feda5372c575" />

<img width="656" alt="image" src="https://github.com/user-attachments/assets/0647cefa-9e1d-4f39-b7e0-c0cfa00be724" />

### ```SUM```
- sums the values in a column bsed on grouping criteria.
- it takes a parameter(column) and will return the sum of the combined records, based on the specified parameter

<img width="1203" alt="image" src="https://github.com/user-attachments/assets/444df9ff-f736-457c-b0b2-bf4c60571358" />

### ```MAX```
- takes the maximum value from a column.
- 

<img width="1351" alt="image" src="https://github.com/user-attachments/assets/21656036-2d60-4f6e-8f94-71d1bdd2e9e2" />

### ```MIN```
- takes the minimum value from a column.
- syntacsis is the same as ```MAX```


### ```AVG```(Average)

- calculates the average value in a column
- takes all values and then divides it by the count of values.
- syntaxis in the same as ```MIN```, ```MAX```, ```SUM```

  <img width="1346" alt="image" src="https://github.com/user-attachments/assets/09ae21d8-e429-4ca5-bb76-bb26f4dd43fb" />


## Having
- a predicate while grouping.
- cannot be be used without aggregating, and without grouping
- ```HAVING ``` clause is used to filter data based on aggregate values 
- it will filter the data after everything is ran, or after the aggregation is done.
- ```HAVING ``` will be another level of conditioning.
####  ```WHERE``` will fiter records that will be aggregated and grouped, while ```HAVING``` filters what the result of query will be. What the user will see. It's not part of the calculations.

#### ```WHERE``` is the filter logic, ```HAVING``` is the presentation logic


## Conditional Statements
- works like IF-ELSE statements
- conditions are called ```cases```
- we can add a conditional statements to a WHERE clause, Aggragate functions, etc.
Statement syntax:
```
CASE
   WHEN -> condition -> THEN
END
```

<img width="754" alt="image" src="https://github.com/user-attachments/assets/4ad08bb2-d23b-4422-9d9e-4f41758598e0" />












