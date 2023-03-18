# CASSANDRA_CRUD

Cassandra Query Language (CQL) CRUD Operations

Cassandra Query Language (CQL) is a language that allows users to interact with the Cassandra database. It is a SQL-like language that is used to create, update, and delete data from the Cassandra database.

This README file provides a brief guide on how to perform CRUD (Create, Read, Update, Delete) operations using CQL in Cassandra.

Creating a Table
To create a table in Cassandra, you can use the CREATE TABLE statement. The general syntax for creating a table is as follows:



                  CREATE TABLE table_name (
                    column1 datatype,
                    column2 datatype,
                    column3 datatype,
                    ...
                    PRIMARY KEY (one_or_more_columns)
                       );

In this syntax, "table_name" is the name of the table you want to create, and "column1", "column2", "column3", etc. are the names of the columns in the table, along with their respective data types.

The PRIMARY KEY clause is used to specify one or more columns that will be used as the primary key for the table. The primary key uniquely identifies each row in the table.

In the Database  two tables are created named students and faculty 
 
                  CREATE TABLE students (
                               roll_no INT PRIMARY KEY,
                               name TEXT,
                               age INT,
                               dep TEXT,
                               email TEXT,
                               phone TEXT,
                               cgpa FLOAT
                                         );
                         CREATE TABLE faculty (
                                f_id INT PRIMARY KEY,
                                 name TEXT,
                                age INT,
                                dep TEXT,
                                email TEXT,
                                phone TEXT,
                                ex_year INT
                                             );


In the "students" table, we have columns for student roll_no, name, age, dep for department of the student, email , phone  and cgpa. The primary key is set to the "roll_no" column.

In the "faculty" table, we have columns for faculty f_id, name,age,dep for department of the faculty, email ,phone and ex_year for experience of the faculty. The primary key is set to the "f_id" column.

Create Operation

To create a new row in a table in Cassandra, you can use the INSERT statement. 


                    INSERT INTO students (roll_no, name, age, dep, email, phone, cgpa) 
                    VALUES 
                    (1, 'Anbu', 20, 'IT', 'anbu@gmail.com', '9645122515',9.2) ;
                    INSERT INTO students (roll_no, name, age, dep, email, phone, cgpa) 
                    VALUES 
                    (2, 'Anto', 22, 'IT', 'anto@gmail.com', '9645122587',8.5);
                    INSERT INTO students (roll_no, name, age, dep, email, phone, cgpa) 
                    VALUES 
                   (3, ' Bala', 19,'IT', 'bala@gmail.com', '7545122515',8.9);
                   INSERT INTO students (roll_no, name, age, dep, email, phone, cgpa) 
                   VALUES 
                   (4, 'Dinesh', 19,'IT', 'dinesh@gmail.com', '9665122515',9.1);
                   INSERT INTO students (roll_no, name, age, dep, email, phone, cgpa) 
                   VALUES 
                   (5, 'Harish', 22, 'IT', 'harish@gmail.com', '9645452587',8.8);


we are inserting a new 5 rows ,for example with an roll_id of 1, a name of "Anbu ", an age of 22, department of "IT" and an email address of "anbu@gamil.com",phone no of '9645122515' and cpga of 9.2 into the " students" table.

                  INSERT INTO faculty ( f_id, name, age, dep, email, phone,ex_year) 
                  VALUES 
                  (1, 'ATHAVAN', 32, 'IT', 'athavan@gmail.com', '9645452587',8);
                  INSERT INTO faculty ( f_id, name, age, dep, email, phone,ex_year) 
                  VALUES 
                  (2, 'ARYA', 32, 'IT', 'athavan@gmail.com', '9645452587',8);
                  INSERT INTO faculty ( f_id, name, age, dep, email, phone,ex_year) 
                  VALUES 
                  (3, 'DRAVID', 35, 'IT', 'dravid@gmail.com', '7845452111',6);
                  INSERT INTO faculty ( f_id, name, age, dep, email, phone,ex_year) 
                  VALUES 
                  (4, 'MOHAN', 28, 'IT', 'mohan@gmail.com', '9255652587',2);
                 INSERT INTO faculty ( f_id, name, age, dep, email, phone,ex_year) 
                 VALUES 
                 (5, 'PRIYA', 27, 'IT', 'priya@gmail.com', '9115400251',2);

we are inserting a new 5 rows ,for example with an f_id of 1, a name of "Athavan ", an age of 32, department of "IT" and an email address of "athavan@gamil.com" ,phone of '9645452587'and experience year of 8 into the "faculty" table.


Read Operation

    To read data from a table in Cassandra, you can use the SELECT statement. Here is an example of selecting all rows from the "users" table:


              SELECT * FROM students;
              
  In this we are selecting all rows from the "students" table.
              
              SELECT * FROM faculty;
              
   In this we are selecting all rows from the "faculty " table.   
   
   
Update Operation

To update data in a table in Cassandra,  use the UPDATE statement. 

            UPDATE students SET email ='dinesh123@example.com' WHERE roll_no = 4;
            
In this  we are updating the email of the student with an roll_no of 4  in the "students" table.

             UPDATE faculty SET email ='arya@example.com' WHERE f_id = 2;
             
In this  we are updating the email of the faculty with an f_id of 2  in the "faculty" table.


Delete Operation

To delete data from a table in Cassandra,  use the DELETE statement. 

                        DELETE FROM faculty WHERE f_id = 1;
In this we are deleting the faculty with an f_id of 1 from the "faculty" table.

To delete a entire table ,use  DROP TABLE
 
                        DROP TABLE faculty;
                        
                        
Conclusion

This README file provided a brief guide on how to perform CRUD operations using CQL in Cassandra.              
