# Interview_Creation_Portal

To run this Project you have to install NodeJS (npm) and MySQL server on your machine.

To setup the web server:

Go to the project directory and run the terminal command as follows:
```
cd server
npm install
```
To setup the MySQL database:

1. Create a Database/Schema name as "Interview_Database" or run the following SQL queries.
```
CREATE DATABASE Interview_Database;
```
```
USE Interview_Database;
```
2. Add two tables "users", to hold data of the available users and "interviews", to hold the data of the upcoming interviews. Run the following SQL query.
  ```
  CREATE TABLE users (
    name VARCHAR(100) NOT NULL,
    email_id VARCHAR(100) NOT NULL,
    PRIMARY KEY (email_id)
  );
  ```
Add some random names with email addresses to the users tables. Run the following SQL query.
```
INSERT INTO users (name, email_id) VALUES ('Arpita', 'arpita@gmail.com');
INSERT INTO users (name, email_id) VALUES ('Deepshi', 'deepshisharma123@gmail.com');
INSERT INTO users (name, email_id) VALUES ('Kirti', 'kirti.godani837@gmail.com');
INSERT INTO users (name, email_id) VALUES ('Govind', 'govindmh14@gmail.com');
INSERT INTO users (name, email_id) VALUES ('Priya', 'Priya@ins.com');
```
Create the table interviews with fields id, email1, email2, startTime, endTime. Run the following SQL query.
```
CREATE TABLE interviews (
  id INT NOT NULL AUTO_INCREMENT,
  email1 VARCHAR(100) NOT NULL,
  email2 VARCHAR(100) NOT NULL,
  startTime DATETIME NOT NULL,
  endTime DATETIME NOT NULL,
  PRIMARY KEY (id)
);
```
You may or may not have any data into the interviews table. The data will be added automatically when you scedule a new interview.

Now when everything is setup. Run the server:
```
cd server
nodemon app
```
If everything is successfull you will the see the text "app is running" and "db is connected" on your terminal.
Then open go to client and open index.html. 

Here are some screenshots of the working system / frontend.
![screenshot](https://i2.paste.pics/b1932c599591aacf2098f6651ee3ec54.png)
![screenshot](https://i2.paste.pics/cb60eb361d97dc93b2023d348f27cdb3.png)