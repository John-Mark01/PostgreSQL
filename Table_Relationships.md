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
      - the PRIMARY key is the OWNER/Parent entity
      - the FOREIGN key is the OWNED/Child entity

  ```SYNTAX```
  - ```fk_country_id``` - the owned/child table's record pointing to the
    - (fk)foreignKey_(name that points to the owner table)
  - ```t.country_id``` - the owner/parent pointing to the refferenced table
    - (t)this_(name of the child table)

    
### Relation Types
  1. one to one - country / capital
  2. one to many - mountain / peaks
    - we operate with 2 tables - an Parent, and a Child
  <img width="1310" alt="image" src="https://github.com/user-attachments/assets/ef63a5ae-908d-4adf-8fa2-696c68d722e4" />

  3. many to many - strudent / courses
    - it is basically 2 one-to-many relations
    - we operate with 3 tables - two tables are childs, and the middle(junction) table is the Owner
    - also the middle(junction) table's fk.id's will have unique records.
    - each Parent can have multiple Childs, and each Child can have multiple Parents. The specified number of parents, and childs are stored in the junction table.

## How to use Table Relations

- OWNER/Parent has a ```PRIMARY KEY```
  
<img width="1348" alt="image" src="https://github.com/user-attachments/assets/0163812b-6276-473a-bfb2-f39cde0510c4" />

- OWNED/Child has a ```FOREIGN KEY```

<img width="1397" alt="image" src="https://github.com/user-attachments/assets/646eb7a2-0bef-4986-8970-4f08107972d7" />

<img width="1158" alt="image" src="https://github.com/user-attachments/assets/a30d6c73-dc59-4afb-8f49-d7ba661aca23" />



## JOINs


## Cascade Operations


## E/R Diagrams
