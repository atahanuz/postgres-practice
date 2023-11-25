# postgres-practice
Hone your PostgreSQL skills by running queries on a sample database. Powered by Google Cloud

Postgres Practice is a website for running queries and seeing the output on an example database. The database simulates a company structure with projects and employees, and it is being used in YTU Computer Engineering classes to teach PostgreSQL.

### [--> PDF explaining the database <--](database-summary.pdf)
#### [--> SQL of the database schema <--](database-schema.sql)
#### [--> SQL to add sample to the DB <--](database-data.sql)

<br>
<span style="color:red"> You can access the tool from this link 👇</span>



## https://trainsql-usaflt4v6a-ue.a.run.app

<img src="https://i.imgur.com/9gjI5zQ.png" width="60%" height="60%">

   


# Usage

Enter any PostgreSQL query and click "Execute", the output will appear on the page. Select "Show Row Indexes" if you want indexes to be displayed on each row.<br>
Here are some example queries:

- SELECT * FROM employee
- SELECT fname,lname, dname <br>
FROM employee <br>
LEFT JOIN department ON employee.dno=department.dnumber

- SELECT e.fname, w.essn, SUM(w.hours)  <br>
FROM employee e, works_on w <br>
WHERE e.ssn = w.essn <br>
GROUP BY e.fname, w.essn <br>
HAVING SUM(w.hours)>30

    
    
    

Note that the database currently is read-only, queries such as UPDATE and DELETE are not supported. I'm working on a solution to allow users to modify the database



