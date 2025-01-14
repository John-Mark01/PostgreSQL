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
#### CONCAT_WS skips the null values, where as CONCAT will take null values in the result

<img width="1067" alt="image" src="https://github.com/user-attachments/assets/c3be1729-49e8-4420-87af-f87f507cbc1d" />


### ```SUPSTRING``` 
  - can be used in a WHERE clause
  - takes a string and two integers as params:
    - the first int will be index from where we START the subbing
    - the second in will say how many indexes after we need
    - the result will be a string starting from the first param, and ends on the second param
 
<img width="1428" alt="image" src="https://github.com/user-attachments/assets/4f1c3b35-3b75-4943-8b9e-b512912f8835" />

 - we can also pass a whole string as a parameter, with no integers, and the result will be eighter NULL, or a string that matches the substring

 <img width="490" alt="image" src="https://github.com/user-attachments/assets/9c9d04f9-6272-4cc2-b420-c04fcd58a2ab" />

 - SUBSTRING can be also used with REGEXes
 - alternative approaach:

<img width="1523" alt="image" src="https://github.com/user-attachments/assets/652eb2ee-d2da-4623-8b9c-1ddd1865cc35" />


## Math Functions
  - caluclations, working with aggregate data 

## Date / Time Functions 
  - compute a length of a date 

## Wildcards
