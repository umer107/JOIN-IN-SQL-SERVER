
**JOINS IN SQL-SERVER**
SQL Server (Transact-SQL) JOINS are used to retrieve data from multiple tables. A SQL Server JOIN is performed whenever two or more tables are joined in a SQL statement.

**There are 4 different types of SQL Server joins:**

 1. SQL Server INNER JOIN (or sometimes called simple join) SQL Server
 2. LEFT OUTER JOIN (or sometimes called LEFT JOIN) SQL Server RIGHT
 3. OUTER JOIN (or sometimes called RIGHT JOIN) SQL Server FULL OUTER   
4. JOIN (or sometimes called FULL JOIN)


**INNER JOIN (simple join)**

The SQL Server INNER JOIN would return the records where table1 and table2 intersect.

    Select * from Followit_account..[User] as usr
    inner join 
    Followit_account..[UserRoles] as usrRoles
    on usr.UserId = usrRoles.UserRoleId
    
**Visual Illustration**

In this visual diagram, the SQL Server INNER JOIN returns the shaded area:


----------
![enter image description here](https://www.techonthenet.com/sql/images/inner_join.gif)

**LEFT OUTER JOIN**

The SQL Server LEFT OUTER JOIN would return the all records from table1 and only those records from table2 that intersect with table1.

    Select * from Followit_account..[User] as usr
    left  join 
    Followit_account..[UserRoles] as usrRoles
    on
    usr.UserId  = usrRoles.UserId

In this visual diagram, the SQL Server LEFT OUTER JOIN returns the shaded area:
![enter image description here](https://www.techonthenet.com/sql/images/left_outer_join.gif)

**RIGHT OUTER JOIN**

This RIGHT OUTER JOIN example would return all rows from the orders table and only those rows from the suppliers table where the joined fields are equal.

    Select * from Followit_account..[User] as usr
    right join 
    Followit_account..[UserRoles] as usrRoles
    on usr.UserId = usrRoles.UserId

**Visual Illustration**

In this visual diagram, the SQL Server RIGHT OUTER JOIN returns the shaded area:

![enter image description here](https://www.techonthenet.com/sql/images/right_outer_join.gif)


**FULL OUTER JOIN**

Another type of join is called a SQL Server FULL OUTER JOIN. This type of join returns all rows from the LEFT-hand table and RIGHT-hand table with nulls in place where the join condition is not met.

    Select * from Followit_account..[User] as usr
    FULL OUTER JOIN 
    Followit_account..[UserRoles] as usrRoles
    on usr.UserId = usrRoles.UserId
**Visual Illustration**

In this visual diagram, the SQL Server FULL OUTER JOIN returns the shaded area:
![enter image description here](https://www.techonthenet.com/sql/images/full_outer_join.gif)

