# PostgreSQL Built-In Functions


## What is a Built-In Function




## Functions


## String Functions
  - manipulate text

#### ```CONCAT``` 
  - concatenetes two Strings.
  - the syntax inside the params is exactly how we want the String to end up like
  - Java approach - ```FORMAT(%s %s, firs_name, last_name)  ```
  - *We can also add strings that are not taken from a column!*

<img width="1426" alt="Screenshot 2025-01-14 at 18 13 21" src="https://github.com/user-attachments/assets/582c7ad5-f8ab-4a0c-a47e-aaf3a3297c82" />


#### ```CONCAT_WS``` 
  - best used when you need to concatenate _multiple_ strings with the same delimeter.
  - first parameter in the params is the delimiter, after that - the column_names.
  - *We can also add strings that are not taken from a column!*
#### CONCAT_WS skips the null values, where as CONCAT will take null values in the result

<img width="1067" alt="image" src="https://github.com/user-attachments/assets/c3be1729-49e8-4420-87af-f87f507cbc1d" />


#### ```SUPSTRING``` 
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


#### ```LEFT, RIGHT```
  - works like a substring but can return a string from LEFT side, as well as RIGHT side
  - takes a string and a an integer:
    - the string that we will supstring
    - the integer will say how many indexes forward *(can be a negative number)*

    ```LEFT('Hello', 2) ——> 'He'```
  
    ```RIGHT('Hello', 3) ——> 'llo'```

#### ```REPLACE```
  - performs a case sensitive search
  - takes 3 strings
  - the flow goes like - if 2nd paramater is found in 1st parameter, it will be replaced with the 3rd parameter

<img width="1419" alt="image" src="https://github.com/user-attachments/assets/6268bbe4-0af4-48de-b3e1-d3cd9fc3ce22" />

  - does not change the database when used in SELECT, but can be used with UPDATE as well.
    
<img width="498" alt="image" src="https://github.com/user-attachments/assets/05a6125d-782d-4556-9695-1c6269cba538" />


#### ```TRIM```
  - removes the whitespaces from both sides if no parameters passed
  - if the is a paramter, it trims occuring paramter in the string (both sides)

    ```TRIM('    Hello    ') ———> 'Hello')```

    ```TRIM('*******Hello****', '*') ———> 'Hello')```

  - we can also remove chars from a ceratin side
    
    ```LTRIM('*******Hello****', '*') ———> 'Hello****')```

    ```RTRIM('*******Hello****', '*') ———> '******Hello')```

#### ```LOWER / UPPER```
  - makes a string UPPERCASED, or LOWERCASED

    ```UPPEER(params)```
  
    ```LOWER(params)```

<img width="447" alt="image" src="https://github.com/user-attachments/assets/910e4045-5f9d-4a3a-9deb-52412d447d86" />


#### ```REVERSE```
  - reverses a string
      
    ```REVERSE('bobi') ———> 'ibob'```

#### ```REPEAT```
  - repeats a string
    
    ```REPEAT('bobi', 10) ———> 'bobi' x10 times```

#### ```LENGTH / CHAR_LENGTH / BIT_LENGTH```
  - returns the count of a string
  
    ```LENGTH('bobi') ———> 4 ``` 
  
    ```CHAR_LENGTH('bobi') ———> 4 ```
  
    ```BIT_LENGTH('bobi') ———> 32 ``` = the sum of the chars bites in the string

#### ```POSITION```
  - return on which position you have found a pattern
    
    ```POSITION('bobi' IN 'hello bobi') ———> 7 ```





## Math Functions
  - caluclations, working with aggregate data 
  - supports basic arithmetic operators 

<img width="1088" alt="image" src="https://github.com/user-attachments/assets/2462bae1-1aef-47bd-9c2a-ac99a180cc89" />


#### ```FLOOR```
  - will evaluate a Double, to the nearest whole number, downwards

<img width="918" alt="image" src="https://github.com/user-attachments/assets/a3519c65-baa6-427d-b2d7-e0a13e94758e" />

#### ```CEILING```
   - will evaluate a Double, to the nearest whole number, upwards

<img width="905" alt="image" src="https://github.com/user-attachments/assets/c579db1a-40ea-45ad-9112-c58115f9f663" />


#### ```ROUND```
  - rounds a decimal number
  - we can add a parameter, to say to which decimal number we want round the number
    - the parameter are how many 0's from the decimal point we want to round

```ROUND(33.62, 2) ——> 33,70 ```

<img width="973" alt="image" src="https://github.com/user-attachments/assets/68e9d98f-ce53-4418-8118-c242c6135d39" />


#### ```TRUNC```
  - removes a number's

<img width="699" alt="image" src="https://github.com/user-attachments/assets/5c9cf21a-29d0-46a0-9b02-56fbe8d04b18" />


## Date / Time Functions 
  - compute a length of a date(TIMESTAMP)

#### ```EXTRACT -- SQL Standart```
#### ```DATE_PART -- Postgre syntax```
  - return a part of a date
  - we can extract: MONTH, DAY, YEAR, TIME

<img width="1246" alt="image" src="https://github.com/user-attachments/assets/7a790fad-2730-4b76-a166-67ceb89fb3d5" />

  - part is MONTH, DAY, YEAR, HOUR, MINUTE, SECOND, etc.

#### ```AGE```
  - find the difference between two dates
  - it will return a timestamp of the difference between two dates
  - furthermore we can only extract different parts of the result - ```EXTRACT(HOURS FROM AGE(date1, date2));```
    
<img width="1272" alt="image" src="https://github.com/user-attachments/assets/469d5cdd-dd14-4992-a9fe-9e2590579564" />

#### ```NOW```
  - returns a TIMESTAMPTZ of the time of submit.
    
#### ```CURRENT_DATE```
 - returns a DATE (14.12.2025) of the time of submit.

#### ```TO_CHAR```
 - formats a timestamp to a string, based on a pattern, like - ```dd MMMM yyyy```
 - the pattern can be also typed as ```day/Day month/Month year/Year```

```TO_CHAR(date1, 'it is yyyy') ———> 'it is 2025'```

#### ```BOUNS```
  - ```INTERVAL```, takes a string
  - add more time in a timestamp

<img width="490" alt="image" src="https://github.com/user-attachments/assets/4a1967e1-41c4-469c-adc2-a49674ba8a50" />

  - ```EPOCH FORM TIMESTAMP```, it returns the timestamp in seconds (TimeInterval in Swift)

    



## Wildcards




