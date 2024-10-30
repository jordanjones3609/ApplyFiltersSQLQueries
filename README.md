<h1>Apply Filters To SQL Queries</h1>


<h2>Description</h2>
In this project, I am a security professional at a large organization, and part of my job is to investigate security issues to keep our systems secure. Recently, I discovered some potential security concerns involving login attempts and employee machines.
<br />
<br />
My task is to examine the organization’s data in the <mark>employees</mark> and <mark>log_in_attempts</mark> tables. I’ll need to use SQL filters to retrieve records from these datasets and investigate the potential security issues.


<h2>Languages and Utilities Used</h2>

- <b>SQL</b> 


<h2>Program walk-through:</h2>
<h3 align="center">Retrieve after hours failed login attempts</h3>

<p align="center">
I recently discovered a potential security incident that occurred after business hours. To investigate this, I need to query the <mark>log_in_attempts</mark> table and review after-hours login activity. I’ll use SQL filters to create a query that identifies all failed login attempts that occurred after 18:00. The time of the login attempt is found in the <mark>login_time</mark> column, and the <mark>success</mark> column contains a value of 0 when a login attempt failed. I can use either a value of 0 or FALSE in my query to identify failed login attempts, I used 0. I needed to use the <mark>AND</mark> operator to filter on multiple conditions to search login attempts that failed after 18:00. <br/>
<br />
<img src="https://imgur.com/Mp8ol2s.png" height="80%" width="80%" alt="SQL Filter Steps"/>
</p>
<br />
<br />

<h3 align="center">Retrieve login attempts on specific dates</h3>

<p align="center">
A suspicious event occurred on 2022-05-09. To investigate this, I want to review all login attempts that happened on this day and the day before. I’ll use SQL filters to create a query that identifies all login attempts that occurred on 2022-05-09 or 2022-05-08. The date of the login attempt is found in the <mark>login_date</mark> column. In order to do so, I use the operator <mark>OR</mark> to output login attempts on either the 8th or the 9th, because it allows me to specify that either condition can be met.
<br/>
<br />
<img src="https://imgur.com/NkY4o8B.png" height="80%" width="80%" alt="SQL Filter Steps"/>
</p>
<br />
<br />

<h3 align="center">Retrieve login attempts outside of Mexico</h3>

<p align="center">
There’s been suspicious activity with login attempts, but the team has determined that this activity didn’t originate in Mexico. Now, I need to investigate login attempts that occurred outside of Mexico. I’ll use SQL filters to create a query that identifies all login attempts that occurred outside of Mexico. When referring to Mexico, the <mark>country</mark> column contains values of both <mark>MEX</mark> and <mark>MEXICO</mark>, so I’ll use the <mark>LIKE</mark> keyword with <mark>%</mark> to ensure my query reflects this. The reason for the <mark>%</mark> is to look for unspecified characters after <mark>MEX</mark>, while <mark>LIKE</mark> is used to search for patterns, which allows me to search for <mark>MEX</mark> and <mark>MEXICO</mark>. The <mark>NOT</mark> operator negates the condition to search all countries except for MEX/MEXICO.
<br/>
<br />
<img src="https://imgur.com/mDP4KIc.png" height="80%" width="80%" alt="SQL Filter Steps"/>
</p>
<br />
<br />

<h3 align="center">Retrieve employees in Marketing</h3>

<p align="center">
My team wants to perform security updates on specific employee machines in the Marketing department. I’m responsible for gathering information on these employee machines and will need to query the <mark>employees</mark> table. I’ll use SQL filters to create a query that identifies all employees in the Marketing department for all offices in the East building.
The department of the employee is found in the <mark>department</mark> column, which contains values that include Marketing. The office is found in the <mark>office</mark> column. Some examples of values in this column are <mark>East-170</mark>, <mark>East-320</mark>, and <mark>North-434</mark>. I’ll need to use the <mark>LIKE</mark> keyword with <mark>%</mark> to filter for the East building.

<br/>
<br />
<img src="https://imgur.com/OU53Rp8.png" height="80%" width="80%" alt="SQL Filter Steps"/>
</p>
<br />
<br />

<h3 align="center">Retrieve employees in Finance or Sales</h3>

<p align="center">
My team now needs to perform a different security update on machines for employees in the Sales and Finance departments. I’ll use SQL filters to create a query that identifies all employees in the Sales or Finance departments. The department of the employee is found in the <mark>department</mark> column, which contains values that include <mark>Sales</mark> and <mark>Finance</mark>. I use the <mark>OR</mark> operator because it specifies that either condition can be met.
<br/>
<br />
<img src="https://imgur.com/i9tkG6X.png" height="80%" width="80%" alt="SQL Filter Steps"/>
</p>
<br />
<br />

<h3 align="center">Retrieve all employees not in IT</h3>

<p align="center">
My team needs to make one more update to employee machines. The employees in the Information Technology department have already received this update, but employees in all other departments still need it. I’ll use SQL filters to create a query that identifies all employees not in the IT department. The department of the employee is found in the <mark>department</mark> column, which contains values that include <mark>Information Technology</mark>. I create a simple query by using the <mark>NOT</mark> operator to search all employees outside of the Information Technology department to update their machines.
<br/>
<br />
<img src="https://imgur.com/H6rvmyR.png" height="80%" width="80%" alt="SQL Filter Steps"/>
</p>
<br />
<br />

<h3 align="center">Summary</h3>

<p align="center">
Recently, I used SQL filters to retrieve records and I performed several security related tasks to investigate potential issues. These included retrieving after hours failed login attempts, identifying login attempts on specific dates, and filtering login attempts that occurred outside of Mexico. Additionally, I retrieved information on employees in the Marketing department, employees in the Finance or Sales departments, and all employees not in the IT department.
<br/>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
