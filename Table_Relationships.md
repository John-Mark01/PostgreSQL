# Table relations in PostgreSQL


## Database Designs

  1. Identifications of the entities
     - what objects we have
     - what entities we need
     - what properties will theese entities have
     - all of those are based on the app
  2. Defining table columns
     - theese are the properties of the entities (objects)
  3. Defining the primary keys - 
     - theese are the most important for each record in a table.
     - that's how we identify each record, with it we can relate and connect tables
  4. Modeling relationships
  5. Definiing constraints
     - NOT NULL, SERIAL, etc.
     - mandatory, and not mandatory fields (columns)
  6. Fillintg test data
     - we need to test the database. And mock data for testing 


## Table Design && Rules






### ```Rules```
 ``` 1. Non repeating data```
 
 ``` 2. Unique identifiers```
 
 ``` 3. NULL only when needed```
 
 ``` 4. Integration of the references``` -  we need to use them

 ``` 5. Atomic data``` - the data should be seperated into smaller pieces. Makes fetching data faster

 ``` 6. Correct data typing``` - CHAR, VARCHAR or TEXT
 
 ``` 7. Indexation```
  
 ``` 8. Access control``` - Policies


## What are table relations
  - theese are the connections between two or more tables.
  - relations are based on PRIMARY KEY and FOREIGN KEY
      - the PRIMARY key is the OWNER entity
      - the FOREIGN key is the OWNED entity

  ```SYNTAX```
  - ```fk_country_id``` - the owned table's record pointing to the 
  - ```t.country_id``` - the owner pointing to the refferenced table

    
### Relation Types
  1. one to one
  2. one to many 
  3. many to many

## How to use Table Relations


## JOINs


## Cascade Operations


## E/R Diagrams
