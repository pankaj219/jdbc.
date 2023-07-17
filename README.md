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

getconnection method
====================
It is an overloaded static method of DriverManger class Return type of this method is java.sql.Connection interface .
It returns an object of Connection interface to the caller method 
Remember connect() method of loaded driver class creates and return object of Connection interface to the getConnection() method .
