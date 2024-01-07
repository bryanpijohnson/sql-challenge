# Bryan Johnson's GWU Module 9 SQL Assignment READ ME File

## This files for this assignment can be found at the following repo:
https://github.com/bryanpijohnson/sql-challenge

## Within the repo link, you will find the following folders and files to be reviewed and graded:

- **README.md** - that is this file. :)
- **EmployeeSQL** - this is the folder where the following files/folders live
    - **data** - this folder holds all of the original CSV files that were imported into the database
    - **Database ERD Image From Website.png** - PNG file of the ERD I made on the quickdatabasediagrams.com site, along with the link to my created diagram (https://app.quickdatabasediagrams.com/#/d/wWIoBi)
    - **Database ERD Image From pgAdmin.png** - PNG file of the ERD I made via pgAdmin
    - **Database Schema and Setup.sql** - SQL file for the schema setup of the database. I used an Extension in VS Code to do all of the work, and it had an option to export the setup.
    - **EmployeeSQL ERD File.pgerd** - this is the ERD file that the 'Database ERD Image From pgAdmin.png' image was created from.
    - **SQL Queries.sql** - this is the SQL file that has all of the analysis questions/queries in it.

## Database Setup Description

I initially created the database and the corresponding tables using the built-in UI in pgAdmin. I created the tables as such:

- **departments**
    - *dept_no* as the PRIMARY KEY
- **dept_emp**
    - (*emp_no*, *dept_no*) as the composite PRIMARY KEY
    - *emp_no* as a FOREIGN KEY to the **employees** table
    - *dept_no* as a FOREIGN KEY to the **departments** table
- **dept_manager**
    - (*dept_no*, *emp_no*) as the composite PRIMARY KEY
    - *dept_no* as a FOREIGN KEY to the **departments** table
    - *emp_no* as a FOREIGN KEY to the **employees** table
- **employees**
    - *emp_no* as the PRIMARY KEY
    - *emp_title_id* as a FOREIGN KEY to the **titles** table
- **salaries**
    - *emp_no* as the PRIMARY KEY
    - *emp_no* as a FOREIGN KEY to the **employees** table
- **titles**
    - *title_id* as the PRIMARY KEY

After setting up the tables as shown above, I imported the data from the corresponding CSV files into the corresponding tables.

## Database Normalization Process

- **1NF** - The tables as they were set up were already in First Normal Form as each row contained exactly one value.
- **2NF** - Now that each table has a primary key (either singular or composite) along with the unique identifiers, the database is in Second Normal Form.
- **3NF** - AS the relationships are already simplified, as in there is nothing implied across any of the tables, the database is in Third Normal Form.

---

If you have any questions, please feel free to contact me.