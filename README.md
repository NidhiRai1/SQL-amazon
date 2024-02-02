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

//where - condition with select 
select coloum_name1 , coloum_name2 from table_name 
where condition = ;

select salary from amazon 
where department = 'iT' AND salary > 5000000 ;

//order by 
select coloum_name from table_name 
order by coloum_name ASC/DESC ;
//LIMIT SELECT* FROM TABLE_NAME LIMIY = 5 // TOP 5 ROWS CAN BE SHOWN

//string 
select upper(coloum_name) from table_name 
replace upper with lower() , length()  , watch 8th
//Group BY - aggregate count() , sum() , svg() , max() , min() , round()
select sount(coloum_name) from table_name //total no. of rows

group by coloum_name(S) 
from table_name 
group by coloum_name(s) ;

select mode , sum(amount) as new
from customer
group by mode   -- jo select statement me aata h wo same coloum geoup by me v aayega 
order by total ASC  

//HAVING - it is use when u wanyt ti apply condition in group by.

select coloum_names 
from table_name 
wgere conditions 
group by coloum_names 
having conditions

select mode , count(amount) as new
from customer
group by mode  
having count(amount) >= 3
order by tottal dec

--- order is : Select, From, Where, Group By, Having, Order By, Limit.

//timestamp - 
time - HH:MI:SS
date - YYYY-MM-DD
year - YYYY OR YY
timestamp - YYYY-MM-DD HH:MI:SS
timestamptz - TIME AND TIME ZONE 

SHOW TIMEZONR -- 
SELECT NOW()  -- YYYY-MM-DD HH:MI:SS
SELECT TIMEOFDAY() -- DAY MONTH DATE HH:MI:SS
SELECT CURRENT_TIME()
SELECT CURRENT_DATE()

//EXTRACT 
SELECT EXTRACT(month from date_coloum) as coloum_name from table_name
   SELECT EXTRACT(month from payement_date) as payment_month from customer
    replace month with DOW  , ct coloum_name(S)
   from tableA
   INNER JOIN  tableB 
   ON tableA.col_name = tableB.col_name 

    select c.col , p.col1 , p.col2
   from customer as c
   INNER JOIN  payment as p 
   ON c.customer_id = p.customer_id

   gull join add all the coloum 
