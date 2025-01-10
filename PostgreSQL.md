## Conventions 
  - ```all tables are named as a plural (users, employees)```
  - ```SQL keywords are CAPITALIZED```
  - ```every naming is in snake_case```
  - ```every statement ends in ;```
  - statements are written as follows ```property name``` -> ```data type``` -> ```constraints``` :: ``` id SERIAL NOT NULL PRIMERY KEY```
  - ```every query is written in multiple lines, not a single one```
  

### Schema 
- is namespace for containing a collection of files and directories
- the schema contains everything - triggers, tables, types, functions, etc...

### Table
- a name
- has columns - DataType
- has rows - Entities
  

# SQL - Structured Query Language
- imperative (we say what we want, but we dont give instructions on the implementation) programming language
- Access ```many records``` with ```one single command```
- ```Eliminates``` the need to specify how to reach a record (_imperative_)
- it is developed at IBM in the early 1970s
- the language is made to be written as you would speak in english
  ### SQL Elements
  - Queries
  - Clauses
  - Expressions
  - Predicates
  - Statements

   <img width="1271" alt="image" src="https://github.com/user-attachments/assets/368fa365-a159-40bc-bc59-a9eb24e97beb" />


  ### SQL Logical Devision
  <img width="1582" alt="image" src="https://github.com/user-attachments/assets/00b2e0d1-c6db-4dcf-b5b9-76935fe09605" />
  
   * DDL - manipulates the ```TABLE```
   * DML - manimuplates the ```DATA``` in a table
   * DCL - manipulates how the data is used, or ```POLICIES```
   * TCL - manipulates all transactions, (git)

  ### PostgreSQL Data Types
  we give explicit datatypes because of optimization
  * INTEGER
    - SMALLINT - 16 bit
    - INTEGER - 32 bit
    - BIGINT - 64 bit
   
  * Double/Floats
    - DECIMAL, NUMERIC - percision (recomended)
    - REAL, DOUBLE

  * SERIAL
    - SMALLSERIAL, SERIAL, BIGSERIAL - used for column identification
   
  * STRINGS
    - CHARACTER/CHAR[(M)] - fixed lenght --> CHAR(30) it save memory for 30 chars
    - VARCHAR[(N)] - it can hold up to N, but the memory will be updated for the chars used
    - TEXT - stores strings of ANY lenght
  * DATES
     - DATE - holds date without time
     - TIME - only time, no date
     - TIMESTAMP - both date and time
     - TIMESTAMPTZ - date, time and time zone

   ### Column Constraints
    * ```UNIQUE``` - not repeatable. It cannot be two records with the same property value
    * ```DEFAULT``` - we give a default value, which will be generated on every entity, upon creation
    * ```NOT NULL``` - needs to be a value, cannot be empty
    * ```PRIMARY KEY``` - unique identificator of a record
    * ```SERIAL PRIMARY KEY``` - automatically increment the primary key
    * ```CHECK``` - a if statement for adding a value ```CHECK(age > 18)```
  
  # SQL Queries
  - the way we communicate with the database
  - they provide greater ```control``` and ```flexibility```
    
  ### Create Table
<img width="864" alt="image" src="https://github.com/user-attachments/assets/8bb43e39-20dc-46a2-b42d-ed3e20e620b0" />


  ### Change Table - ALTER
<img width="260" alt="image" src="https://github.com/user-attachments/assets/ca077e03-3300-4185-983b-da9de6d8a456" />
<img width="1208" alt="image" src="https://github.com/user-attachments/assets/0d8608ab-4a79-4b76-965a-1bfa842657fc" />

### TRUNCATE - deletes all records from the table. The table still exists
### DROP - deletes the table



 
    
