# SQL

## Setup

MySQL on Docker

`$ docker run --name mysql -e MYSQL_ROOT_PASSWORD=root -d mysql`  
`$ docker exec -it mysql bash`  
`# mysql --user=root -p`  
`mysql> status`  
`mysql> use mysql;`  
`mysql> show tables;`  
`mysql> describe user;`  
`mysql> select host, user from user;`  
`mysql> exit`  
`# exit`  

## Insert Update

**Create Insert**
```sql
CREATE TABLE customer (
	id INTEGER,
	first_name VARCHAR(100),
	last_name VARCHAR(100),
	address VARCHAR(100),
	city VARCHAR(2),
	zip_code VARCHAR(10)
);
```

**Insert table**
```sql
INSERT INTO customer VALUES (1234, 'Michael, 'Westom', '123 Brickel', 'Miami', 'FL', '33135');
```

## Select
```sql
select * from employee`
```

**Row count**
```sql
select count(*) from departments;`
```

**Aliases**
```sql
select first_name as 'First Name', last_name as 'Last Name' from employees;
```

**Concat**
```sql
select concat(first_name, ' ', last_name) as 'Name' from employees
```

**Arithmetic**
```sql
select salary * .01 as weekly from salaries
```

**Data types**
![numbers](./img/numbers.png)
![datetime](./img/datetime.png)
![strings](./img/strings.png)

**Format dates**
```sql
DATE_FORMAT("2018-05-15", "%M %d %Y")
```
![dateformat](./img/dateformat.png)
![dateformat2](./img/dateformat2.png)

**Left right**
```sql
select left('asdf', 1); //a
select right('asdf', 1); //f
select first_name, last_name, concat(left(first_name, 1), left(last_name, 1)) as Initials from employees;
```

**Equals**
```sql
SELECT * from employees WHERE first_name = 'Elvis';
SELECT * from employees WHERE first_name <> 'Elvis';
SELECT * from employees WHERE first_name != 'Elvis';
```

**And Or**
```sql

```

## Grouping

**group-by**
```sql
select first_name, count(*) from employees group by first_name;
select first_name, count(*) from employees group by first_name having gender like 'M';
```

## Joins

**Inner join**
Rows returned must match the join conditions
```sql
select * from employees emp inner join dept_manager dm on emp.emp_no = dm.emp_no;
```

**Outer join**
Return all rows in one table and only the matching rows from the second table
```sql

```

**Natural join**
Join tables where columns of the same name are equal
```sql
select dept_name, first_name, last_name from employees as emp
	natural join dept_emp as de
    natural join departments as dept
    natural join titles as t;
```

**Cross join**
Return one row for each row in the first table, with each row in  the second table
```sql

```

**Union join**
Combine rows from one or more tables
```sql

```

## Insert

**Insert**
```sql
INSERT INTO departments VALUES ('d0002', 'Awesome Gurus');
INSERT INTO employees SELECT max(emp_no) + 1, '1976-01-01', 'John', 'Thompson', 'M', '2018-06-06' FROM employees;
```

## Update
```sql
UPDATE departments
SET dept_name = 'Social Media Marketing'
WHERE dept_no = 'd999';
```

```sql
drop database employees;
```

## Delete
```sql
DELETE FROM somelog WHERE user = 'jcole'
ORDER BY timestamp_column LIMIT 1;
```

## Transactions
Unit of work, one or more SQL statements  
- Commit - indicates the end of the transaction
- Rollback - revert all changes of the transaction
- Save Point - Programatic point you can set, which allows you to rollback to
```sql
begin;
DELETE FROM employees WHERE emp_no = '50000';
commit;
rollback;

set autocommit=0;
```

## Views
```sql
create or replace view some_name
as select * from products;

select * from some_name;

drop view some_name;
```

## Using SQL to create tables
```sql
CREATE TABLE salaries2 as (select * from salaries);
```

**Truncate table**
Drop and re-create table.  
Faster than SQL Delete.  
Cannot be rolled back.

## Keys
**Autoincrement**
```sql
CREATE TABLE persons (
	id int auto_increment,
	first_name VARCHAR(255),
	last_name VARCHAR(255),
	primary key (id)
);
```

**Foreign key**
```sql
CREATE TABLE drink_order (
	id int auto_increment,
	customer_id INTEGER,
	drink_description VARCHAR(100),
	primary key (customer_id),
	CONSTRAINT fk_drink_order_customer
		FOREIGN KEY (customer_id)
		REFERENCES customer (id)
);
```

