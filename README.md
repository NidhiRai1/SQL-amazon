# SQL-amazon
basic sql

//SQL - CRUD for the database AND TO INTERECT 
--relational 0 data store in the form of the table ,
--no relational noSQL -daat stored in the form of key value pair
horizanatal is the row 
-- primery key - it is unique and not null
CREAT TABLE table_name(
coloum_name DATATYPR comstraint ,
coloum_name DATATYPR comstraint 
) ;

CREAT TABLE coustmer(
"ID" INT primary key ,
"name" varchar NOT NULL
) ;
//INSERT 
NSERT INTO table_name (Coloum_1, Coloum_2, coloum_3, Coloum_4, coloum_5)
VALUES
(1, 'sam', 26, 'Delhi', 9008),
(2, 'Ram', 19, 'Bangalore', 11000),
(3, 'Pam', 31, 'Mumbai', 6060),
(4, 'Sam', 42, 'Pune', 10000);

NSERT INTO customer (CustID, CustName, Age, City, Salary)
VALUES
(1, 'sam', 26, 'Delhi', 9008),
(2, 'Ram', 19, 'Bangalore', 11000),
(3, 'Pam', 31, 'Mumbai', 6060),
(4, 'Sam', 42, 'Pune', 10000);

//update 
UPDATE table_name
SET "coloum_1" = 'value1' , "coloum_2" = 'value_2'
WHERE "ID" = 'value'

UPDATE customer
SET CustName = 'Xam' , Age = 32
WHERE CustID = 4

//delete use to delete the row
delete from table_name where condition ;

//alter table - is use to delete ,add or modify the coloum ,
alter table table_name 
add coloum coloum_name ; // add coloum
alter table table_name ;
drop coloum coloum_name ; //delete coloum
alter table table_name ;
alter coloum coloum_name datatype; // change the datatype of the existing coloum

--drop table - DROP TABLE table_name ; //delete the table from thr database
--truncate - TRUNCTATE TABLE table_name; // de;ete the data from the table but the table is their 

//SELECT - SELECT coloum_name1 , coloum_name2 , coloum_name3
select*from the table_name ;
--distinct   ----   select distinct coloum_name from tablr_name ;

//where 
select coloum_name1 , coloum_name2 from table_name 
where condition = ;

select salary from amazon 
where department = 'iT' AND salary > 5000000 ;

//order by 
select coloum_name from table_name 
order by coloum_name ASC/DESC ;
//LIMIT SELECT* FROM TABLE_NAME LIMIY = 5 // TOP 5 ROWS CAN BE SHOWN
