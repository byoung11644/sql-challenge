# SQL Challenge - Employee Database: A Mystery in Two Parts

![sql.png](sql.png)

## Background

It is a beautiful spring day, and it is two weeks since being hired as a new data engineer at Pewlett Hackard. The first major task is a research project on employees of the corporation from the 1980s and 1990s. All that remain of the database of employees from that period are six CSV files.

In this assignment, we will design the tables to hold data in the CSVs, import the CSVs into a SQL database, and answer questions about the data. In other words, we will perform:

1. Data Engineering

3. Data Analysis

Note: You may hear the term "Data Modeling" in place of "Data Engineering," but they are the same terms. Data Engineering is the more modern wording instead of Data Modeling.



## Instructions

#### Data Modeling

Inspect the CSVs and sketch out an ERD of the tables. Feel free to use a tool like [http://www.quickdatabasediagrams.com](http://www.quickdatabasediagrams.com).

#### Data Engineering

* Use the information to create a table schema for each of the six CSV files. Remember to specify data types, primary keys, foreign keys, and other constraints.

  * For primary keys, we check to see if the column is unique, otherwise we create a [composite key](https://en.wikipedia.org/wiki/Compound_key).
  * Be sure to create tables in the correct order to handle foreign keys.

* Import each CSV file into the corresponding SQL table.

#### Data Analysis

Once we have a complete database, we will do the following:

1. List the following details of each employee: employee number, last name, first name, sex, and salary.

2. List first name, last name, and hire date for employees who were hired in 1986.

3. List the manager of each department with the following information: department number, department name, the manager's employee number, last name, first name.

4. List the department of each employee with the following information: employee number, last name, first name, and department name.

5. List first name, last name, and sex for employees whose first name is "Hercules" and last names begin with "B."

6. List all employees in the Sales department, including their employee number, last name, first name, and department name.

7. List all employees in the Sales and Development departments, including their employee number, last name, first name, and department name.

8. In descending order, list the frequency count of employee last names, i.e., how many employees share each last name.

## Bonus (Optional)

As we examine the data, we are overcome with a creeping suspicion that the dataset is fake. We surmise that your boss handed you spurious data in order to test the data engineering skills of a new employee. To confirm the hunch, we decide to take the following steps to generate a visualization of the data:

1. Import the SQL database into Pandas using SQLAlchemy

   ```sql
   from sqlalchemy import create_engine
   engine = create_engine('postgresql://localhost:5432/<your_db_name>')
   connection = engine.connect()
   ```

* Consult [SQLAlchemy documentation](https://docs.sqlalchemy.org/en/latest/core/engines.html#postgresql) for more information.

2. Create a histogram to visualize the most common salary ranges for employees.

3. Create a bar chart of average salary by title.

## Epilogue

The boss thanks us for the work. On the way out of the office, you hear the words, "Search your ID number." You look down at your badge to see that your employee ID number is 499942.


### Copyright

Trilogy Education Services © 2019. All Rights Reserved.
