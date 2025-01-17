# Data Agrregation
- combining multiple elements with a common property
- its done in SQL by ```GROUPING```



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

<img width="1321" alt="image" src="https://github.com/user-attachments/assets/8270da78-33ed-4abf-8e6c-5b220fdb9879" />


#### ```COUNT```
- takes all combined records from grouping
```count(*)``` will count all records from a table. Will return all values that are not NULL.
- all columns that are NOT aggregated on, must be grouped!

<img width="327" alt="image" src="https://github.com/user-attachments/assets/63ccc50a-d532-4cd7-b78f-feda5372c575" />

<img width="656" alt="image" src="https://github.com/user-attachments/assets/0647cefa-9e1d-4f39-b7e0-c0cfa00be724" />




## Hanving




## Conditional Statements
