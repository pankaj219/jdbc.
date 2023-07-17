# jdbc.

Executing query
===============

1) Create Statement object
2) Eexcute query

creating Statement object
=========================
It could be an object of following interface 
1) Statment interface
2) PreparedStatement interface
3) CallableStatement interface : This object should be created when our program wants to excute sql stored produre and SQL functions

Statement interface 
===================
Object of this interface should be created when our program wants to excute SQL non-parameterized quries(the query that does not takes any input/value from the user)

All DDL quries are non - parametrized
Select * from tablename 
delete from tablename 

Command to create statement object
==================================
Statement st=cn.createStatement(); //cn is object fo cnnection interface 
Statement interface has following three method to excute SQL queries
1)execute():call this method execute DDL.
2)excuteUpdate():for DML
3)excuteQuery():for DQL

getconnection method
====================
It is an overloaded static method of DriverManger class Return type of this method is java.sql.Connection interface .
It returns an object of Connection interface to the caller method 
Remember connect() method of loaded driver class creates and return object of Connection interface to the getConnection() method .

Static Block
============
We can define this block inside class by using static keyword.THis block is excuted automatically on class loading. Remember every class(that your are using in program) will be loaded by JVM IN MEMORY FIRST since static block is excuted on class loading so code written inside static block will be excuted only once during the life cycle of class.


Java.sql.DriverManager class
============================

As we know connect() method of java.sql.Driver interface should be called to make connection with database
we do not need to write code to call connect() method .This code is already written inside getconnection() method of DriverManager Class .So we will have to write code to call getconnection () method will call connect() method of driver class.

As we know method can not be called without refrence of the object,so getconnection() method of DriverManager class must have refrence of required driver class

So we will have to give refrence of driver class to the DriverManager class.As we know every calss on loading creates ana object of itself and gives reference of the object to DriverManager class 
So before calling getconnection() method we will have to load required driver class to load driver call forName() static method of java.lang.class class
