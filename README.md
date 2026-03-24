# Project: Login Web Application (Servlet + MySQL + Tomcat)
  
## MySQL Database Setup
## Run this in MySQL:

    CREATE DATABASE login_db;
    USE login_db;

    CREATE TABLE users (
        id INT PRIMARY KEY AUTO_INCREMENT,
        username VARCHAR(50),
        password VARCHAR(50)
    );

    INSERT INTO users (username, password)
    VALUES ('admin', '12345');


## Create WAR File
## Inside project folder run:
    jar -cvf LoginApp.war *

## Deploy to Tomcat
## Copy WAR file to:
    tomcat/webapps/

## Start Tomcat:
    startup.sh

## Open browser:
    http://localhost:8080/LoginApp

## Login credentials:
```bash
Username: admin
Password: 12345
