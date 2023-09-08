# SQL Used DDL and DML
create database employeeinfo;
use employeeinfo;
drop database sql_demo1;
show databases;
show tables;
show tables;
select*from employee;
insert into employee values("yash",100,"tcs",25000,"BBSR");
insert into employee values("ayush",101,"walmart",35000,"DELHI");
insert into employee values("ram",100,"microsoft",65000,"mumbai");
insert into employee values("shyam",103,"google",55000,"chennai");
insert into employee values("laxman",104,"amazon",45000,"BBSR");
alter table employee add( no int (9));
alter table employee drop no;
alter table employee modify company varchar (30);
alter table empoloyee drop column company;
truncate table employee;
alter table employee rename column id to employeid;
update employee set salary=5000 where employeid=100;
delete from employee where employeid=101;


