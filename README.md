# SQL Definition
I can't describe this mini project, but I just want to refresh my knowledge about database and SQL functions by a case. Here are the guidelines you to follow:
* [Scenario](#scenario)
* [Objective](#objective)
* [Context](#context)
* [Requirements](#requirements)
* [Solving](#solving)

## Scenario
I am working in an e-commerce company and single handedly responsible with a CRM (customer relationship management) with the user management data. The user data should synchronize with user data from another system which from [`https://reqres.in/api/users?page=2`](https://reqres.in/api/users?page=2).

## Objective
I need to build a database schema for CRM service from scratch according to the requirements.

## Context
* For the MVP, the requirements of CRM service are defined below 
* The actors that can access the service are admin and super admin.
* User is the entity that manipulates or manages the services.
* Users and actors had different data structures.

## Requirements
1. Milestone 1
    * Create ERD how I want to design the database based on the configuration at milestone 2.
1. Milestone 2
    * Initiate the database schema on mySQL server.
    * Create table actors which will contain information about as follow:
        ```
        Id (bigint unsigned)
        Username (varchar)
        Password (varchar)
        Role id (int unsigned)
        Flag for actor if its verified (enum(‘true’, ‘false’)
        Flag for actor if its active (enum(‘true’, ‘false’)
        Created at (timestamp)
        Updated at (timestamp)
        ```
    * Create table for customer which will contain information about as follow:
        ```
        Id (bigint unsigned)
        First name (varchar)
        Last name (varchar)
        Email (varchar)
        Avatar (varchar)
        Created at (timestamp)
        Updated at (timestamp)
        ```
    * Create table for storing each unique actor role which are admin and super admin, the table consist:
        ```
        Id (int unsigned)
        Role name (varchar)
        ```
    * Create table register approval which will be used to get a list of admin registration that need to be approved by super admin, the data consist:
        ```
        Id (bigint unsigned)
        Admin id (bigint unsigned)
        Super admin id (bigint unsigned)
        Status (varchar)
        ```
    * Add foreign key to role id which reference table is table role.
1. Milestone 3
    * For super admin, insert one super admin to table actors.
    * For the super admin, create a mysql user that can access the database through the mysql server with the same username and password from table actors, also the host is 0.0.0.0.
    * Export the database schema into a sql file using mysqldump.

## Solving
Still processing...
