# SQL Queries to Investigate Security Incidents

### Skills Demonstrated
+ Demonstrated proficiency in writing and filtering SQL queries
+ Applied logical operators (`AND`, `OR`, `NOT`) and pattern matching with `LIKE`
+ Queried multiple tables (`log_in_attempts`, `employees`) to extract targeted insights  

---

### Task 1️⃣: Retrieve after hours failed login attempts

There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated. Following code demonstrates how I created an SQL query to retrieve records from different datasets and filter login attempts that occurred after business hours. 

```
SELECT * FROM log_in_attempts WHERE login_time > '18:00' AND success = FALSE;
```
First, I selected all data from the log_in_attempts table. Then, I used a WHERE clause with an AND operator to show only failed login attempts after 18:00. The conditions are login_time > '18:00' and success = FALSE. The resulting output is shown below. 
<img width="590" height="79" alt="Screen Shot 2025-11-03 at 3 20 33 PM" src="https://github.com/user-attachments/assets/ebcef149-4cd1-4741-83c3-8b3fea19204b" />

<br>

### Task 2️⃣: Retrieve login attempts on specific dates

A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated. The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.
```
SELECT * FROM log_in_attempts WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```
<img width="592" height="75" alt="Screen Shot 2025-11-03 at 3 39 26 PM" src="https://github.com/user-attachments/assets/8298d550-1891-4025-9d82-7d01e003198e" />


<br><br>


### Task 3️⃣: Retrieve employees in Marketing

The team wants to update the computers for certain employees in the Marketing department. The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building.
```
SELECT * FROM employees WHERE department = 'Marketing' AND office LIKE 'East%'; 
```
This query returns all employees in the Marketing department in the East building. I used LIKE with East% as the pattern to match because the data in the office column represents the East building with the specific office number. 
<img width="588" height="100" alt="Screen Shot 2025-11-03 at 3 54 37 PM" src="https://github.com/user-attachments/assets/dcbdcd31-7460-4490-862d-a633fb69583f" />

<br>

### Task 4️⃣: Retrieve employees in Finance or Sales

A different security update is needed for the machines for Finance and Sales employees as well. 
```
SELECT * FROM employees WHERE department = 'Finance' OR department = 'Sales'; 
```
<img width="593" height="101" alt="Screen Shot 2025-11-03 at 4 00 57 PM" src="https://github.com/user-attachments/assets/0d1ac196-df3d-494d-a941-449c01c33a2d" />

<br><br>


### Task 5️⃣: Retrieve all employees not in IT

Lastly, my team needs to perform a security update on employees outside of the Information Technology department. To make the update, I first have to get information on these employees.
```
SELECT * FROM employees WHERE NOT department = 'Information Technology';
```
<img width="592" height="91" alt="Screen Shot 2025-11-03 at 4 02 50 PM" src="https://github.com/user-attachments/assets/52c806f2-78d4-4d06-8adf-8218c78525e4" />


---
## Summary
As a cybersecurity analyst, SQL is important because it allows me to efficiently query and analyze data from logs, user activity, and system records. By using SQL, I can identify suspicious patterns, track unauthorized access, and uncover insights that support security investigations.
