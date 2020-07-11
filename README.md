# Steps for Database Configuration
1. Install MySQL Server
2. Install MySQL WorkBench
3. Once your databse is up and running then create a connection with database using below credentials :

hostname : localhost
Port : 3306
Username: root
Password: Welcome@123

 
4. Create your database and tables as per below: 

CREATE DATABASE twiter_db;
USE twiter_db;
CREATE TABLE users ( id int, userName varchar(20) not null, password varchar(20) not null );
INSERT INTO users VALUES ( 1, 'admin', 'admin' );

5. Make below changes to your application.properties file (Already done) - Just for reference, you may change values here as per your credentials
spring.jpa.hibernate.ddl-auto=update
spring.datasource.url=jdbc:mysql://${MYSQL_HOST:localhost}:3306/twiter_db
spring.datasource.username=root
spring.datasource.password=Welcome@123

# Prerequisite softwares: 
1. Java 8
2. JDK 1.8
3. Node for frontend application from https://nodejs.org/en/
Nodejs - v12.18.1
4. Install curl for rest api calls  
   npm install curl

# Curl command for rest calls/Postman

## Post call 
curl localhost:8080/demo/add -d userName=root -d password=root

## Get call 
curl 'localhost:8080/demo/all'


# Help
For any help, visit below URL: 
https://spring.io/guides/gs/accessing-data-mysql/


  
