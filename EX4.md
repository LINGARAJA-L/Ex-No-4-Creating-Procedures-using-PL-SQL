# Ex. No: 4 Creating Procedures using PL/SQL

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
Developed by:LINGARAJA L
Register no:212222040086
```
```
create table vacancy (
  2   empid number,
  3   empname varchar (15),
  4   dept varchar(15),
  5    salary number
  6  );

Table created.

SQL>  create or replace procedure insert_vacancy_data as
  2  begin
  3    insert into vacancy (empid, empname, dept, salary) values (001,'Lucas Warren', 'Programmer', 480000);
  4    insert into vacancy (empid, empname, dept, salary) values (002,'Melaine Bailey', 'HR', 10730);
  5    insert into vacancy (empid, empname, dept, salary) values (003,'John Cena', 'Manager', 160100);
  6  commit;
  7  for emp_rec IN (select * from vacancy) loop
  8  dbms_output.put_line('Employee ID: ' || emp_rec.empid || ',Employee Name: ' || emp_rec.empname || ',Department: ' || emp_rec.dept || ',Salary:' || emp_rec.salary);
  9  end loop;
 10  end;
 11  /

Procedure created.

SQL> begin
  2  insert_vacancy_data;
  3   end;
  4  /

PL/SQL procedure successfully completed..

SQL> select *from vacancy;
```
### Output:
![Screenshot 2023-10-06 152453](https://github.com/LINGARAJA-L/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/129825857/3ab32983-e376-4356-bf5f-4dae140c783d)

![Screenshot 2023-10-06 152534](https://github.com/LINGARAJA-L/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/129825857/e672391a-3ede-4f5d-bbc7-6b1b06386a26)

![Screenshot 2023-10-06 152630](https://github.com/LINGARAJA-L/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/129825857/f78dd6fa-9606-4bcc-91b0-3eb87dce0269)

![Screenshot 2023-10-06 152708](https://github.com/LINGARAJA-L/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/129825857/0e381b5c-14da-4f79-a383-1bd6f7297f98)


### Result:
Hence the procedure using pl/sql is created successfully.
