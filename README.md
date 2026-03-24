# Project: Login Web Application(Servlet + MySQL + Tomcat)
  
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
    Username: admin
    Password: 12345


## IF run by Docker make Dockerfile then
## Build Docker Image
    docker build -t login-app:v1 .
    docker run -d -p 8080:8080 login-app:v1


## Deploy in Kubernetes
    kubectl apply -f deployment.yml
    kubectl apply -f service.yml

## Access:
    http://<NodeIP>:30007/LoginApp






