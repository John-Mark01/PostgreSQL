# PostgreSQL Built-In Functions


## What is a Built-In Function




## Functions


## String Functions
  - manipulate text

### ```CONCAT``` 
  - concatenetes two Strings.
  - the syntax inside the params is exactly how we want the String to end up like
  - Java approach - ```FORMAT(%s %s, firs_name, last_name)  ```
  - *We can also add strings that are not taken from a column!*

<img width="1426" alt="Screenshot 2025-01-14 at 18 13 21" src="https://github.com/user-attachments/assets/582c7ad5-f8ab-4a0c-a47e-aaf3a3297c82" />


### ```CONCAT_WS``` 
  - best used when you need to concatenate _multiple_ strings with the same delimeter.
  - first parameter in the params is the delimiter, after that - the column_names.
  - *We can also add strings that are not taken from a column!*

<img width="1067" alt="image" src="https://github.com/user-attachments/assets/c3be1729-49e8-4420-87af-f87f507cbc1d" />


## Math Functions
  - caluclations, working with aggregate data 

## Date / Time Functions 
  - compute a length of a date 

## Wildcards
