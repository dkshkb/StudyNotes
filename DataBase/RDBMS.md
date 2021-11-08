# Relation Database Management System (RDBMS)

Database stores user information
- Usernames
- Passwords
- Transactions

The management system allows
- Store
- modufy
- extract
Uisng a function called **Querying**

## Relational Database   
Store data in terms of tables.  
Column: field (maintain information)  
Row: records (row entry)

Important features:  
Single database -> several tables  

Unlike flat-file -> self-contained in a single table

## Querying

### SQL: Structural Querying Language  

a series of commands to retrieve or update data 
- Select
- Insert
- Drop
- Delete

### Select
To retrieve data from a large database  
Decide what we want to select, and where we want to select it from  
Example:
SELECT Student ID FROM MSBM1

MSBM1
| Name | Gender | Age | Student ID |
| :--- | :---   | :---| :---       |
| John | Male   | 21  | 1234567    |
| Ben  | Male   | 20  | 18664      |
| Sarah| Female | 22  | 344556     |

| Student ID|
|:---|
|1234567|
|18664|
|344556|

#### WHERE 
SELECT Student ID FROM MSBM1 WHERE Gender = 'Male'

| Student ID|
|:---|
|1234567|
|18664|

## Advantages:
1. Can be access by many people
2. Information presented in clear and concise manner
3. Ability to carry out different complicated commands

## Disadvantages:
1. Complicated to implement
2. Hard process
    - Complexicity of the information/data
    - Connection and speed of the computer
3. 

## Different versions of RDBMS
- MySQL
    - Free and paid versions
- MS SQL Server
- Oracle 
    - Multi-use DMS
    - Preferred database server for client/server computing
    - Supporting all major opeation platforms
- MS Access
    - entry level RDBMS
    - Easy to use intuitive graphical interface
    - Inexpensive

## References
- [Learn RDBMS in 6 minutes!](https://youtu.be/t48TGntrX4s)
