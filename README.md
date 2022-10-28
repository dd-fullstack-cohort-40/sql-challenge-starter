# SQL  Challenge
## Part1 

### Getting Started

In order to complete this assignment, you must use Docker to run a sql database container. The necessary configuration files are provided for you in this repository. and below are instructions for getting started.

1. Create a new file called `/project.env` based on `/example.env` and update the placeholders with your information.
2. Create a deployment on the digital ocean droplet provided for you and perform a mass upload.
3. Gain access to your droplet using putty(windows) or the ssh command(MacOS)
4. cd into the project then run `docker-compose up -d`

For instructions on how to run sql files, see the lecture notes for the sql Commands lecture

### Marching Orders

#### Part 1.1
Using the conceptual model below create a DDL file named `asana.sql` and execute it. Pay close attention to the data types for attributes. 

##### Conceptual Model
**Profile** \
profile_id (PK) \
profile_about_me \
profile_email \
profile_hash \
profile_name 
    
 **Project** \
project_id (PK) \
project_profile_id (FK) \
project_due_date \
project_description \
project_name 
    
 **Ticket** \
 ticket_id (PK) \
 ticket_profile_id (FK) \
 ticket_project_id (FK) \
 ticket_description \
 ticket_due_date \
 ticket_name

 **Status** \
status_id (PK) \
status_value \
status_color 

 **TicketStatus** \
ticket_status_status_id \
ticket_status_ticket_id 
ticket_status_date 
    
**Relationships** \
One profile can own many projects \
One profile be assigned to many tickets \
many tickets can have many statuses 
    
#### Part 1.2
Write all of these in a second file called statements.sql and run them. You should be able to see the data show up in the database browse.

1. Write and execute three insert statements on a strong entity table based on the DDL from question 1. Reminder: Strong Entities have no foreign keys.

2. Write and execute an update statement on a row created in question 2

3. Write and execute a delete statement on a row created in question 2

4. Write and execute an insert statement on a table with a foreign key that references the original table in question 2.

5. Write and execute a select statement for a row using its primary key as the selector.

6. Write and execute a select statement that incorporates both a where clause and an inner-join.
 

