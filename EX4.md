# Ex. No: 4 Creating Procedures using PL/SQL

## DATE:1.9.23

### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
Developed by:MELVIN S
Register no:212222040098
```
```
> create table vacancy1(empid number,empname varchar (15),dept varchar (15),salary number);

Table created.

SQL> create or replace procedure insert_vacancy1_data as
  2  begin
  3  insert into vacancy1 (empid, empname, dept, salary) values (01,'Luffy', 'Architect', 82000);
  4  insert into vacancy1 (empid, empname, dept, salary) values (02,'Garp', 'Interpreter', 80700);
  5  insert into vacancy1 (empid, empname, dept, salary) values (03,'Zoro', 'Geologist', 60100);
  6  insert into vacancy1 (empid, empname, dept, salary) values (04,'Ace', 'Meteorologist', 65200);
  7  commit;
  8  for emp_rec IN (select * from vacancy1) LOOP
  9  dbms_output.put_line('Employee ID: ' || emp_rec.empid || ',Employee Name: ' || emp_rec.empname || ',Department: ' || emp_rec.dept || ',Salary:' || emp_rec.salary);
 10   end loop;
 11  end;
 12  /

Procedure created.

SQL> begin
  2   insert_vacancy1_data;
  3   end;
  4    /

PL/SQL procedure successfully completed.

SQL> select *from vacancy1;
```
### Output:
![Screenshot 2023-10-08 114306](https://github.com/Melvin14112004/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/129204995/5c3c6c73-5a3c-483e-8d2d-cc8256623b5a)


### Result:
Hence the procedure using pl/sql is created successfully.
