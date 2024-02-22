# SchoolMockaroo

SchoolMockaroo is a mock database project aimed at simulating a school management system using PostgreSQL. It provides a sample database schema and data generated with Mockaroo testing purposes.

## Features

- **Database Schema**: The project includes an Entity-Relationship (ER) diagram outlining the database schema.
- **Mock Data**: Sample data is generated using Mockaroo to populate the database tables.
- **PostgreSQL**: The database management system used for this project is PostgreSQL, ensuring compatibility and reliability.

## ER Diagram

<img width="500" alt="ER diagram for School Management" src="https://github.com/CLiz17/schoolMockaroo/assets/68838221/18c16170-9018-4653-b7b3-1ebf49cc0e67">

## Steps

### Step 1: Setup PostgreSQL and Create a Database

First, install PostgreSQL. Im using Fedora system:

```bash
sudo dnf install postgresql-server postgresql-contrib
```

Initialize the database cluster:

```bash
sudo postgresql-setup --initdb
```

Start the PostgreSQL service:

```bash
sudo systemctl start postgresql
```

Create a use or use the default user 'postgres'

```bash
CREATE ROLE username WITH LOGIN PASSWORD 'password';

# Example
CREATE ROLE liz WITH LOGIN PASSWORD 'password';
```

Create a database

```bash
sudo -u user_name createdb database_name

# Example
sudo -u liz createdb schooldb
```

### Step 2: Login to Postgres Terminal

Now, Login to the Postgres Terminal

```bash
sudo -u user_name psql
```

To view the database

```bash
\l
```

To view the users

```bash
\du
```

To switch to the database

```bash
psql -U user_name -d your_database_name

# Example
psql -U liz -d schooldb
```

### Step 3: Create Tables in the Database

Refering the ER Diagram, create tables in the database created.

```bash
CREATE TABLE student (
    id SERIAL PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    grade VARCHAR(50),
    dob DATE,
    age INTEGER
);

CREATE TABLE school (
    name VARCHAR(50),
    addr_city VARCHAR(50),
    addr_state VARCHAR(50),
    addr_pin INTEGER
);

CREATE TABLE faculty (
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    salary INTEGER,
    subject VARCHAR(50),
    phone_no VARCHAR(15)
);
```

### Step 4: Add data to the tables

COPY command can be used to import data into PostgreSQL

```bash
COPY students FROM '/home/liz/schoolMockaroo/student.csv' DELIMITER ',' CSV HEADER;
```
