# user-rest-api

## Description

This REST API application is a user management tool which allows you to see, edit and delete all user entries. You can add new users as well.

## Personal goals

- To implement a REST API using Spring MVC
- To build the data layer using Spring Data JPA
- To understand configuration, deployment and execution of Spring applications

## Core technologies

*Back-end*
- Spring Boot
- Hibernate (as a JPA framework)

*Database*
- MySQL

*Dependency management tool*
- Gradle

*IDE*
- IntellIJ Idea

*Containerization*
- Docker-compose

## Build setup

### With Docker

- Clone this repo to your local machine. Docker-compose version must above 1.18 (Upgrade docker-compose to the latest version)[https://stackoverflow.com/questions/49839028/how-to-upgrade-docker-compose-to-latest-version]. Don't forget to restart your shell after performing all the steps.
```
# Start docker-compose

$ docker-compose up
```

This command creates the three docker containers detailed below:

- _user-rest-api_app_1_: Main container of the Spring Boot application

- _user-rest-api_mysql_1_: DB container

- _user-rest-api-adminer_1_: DB management tool to interact with the MySQL DB

Adminer's credentials are the ones defined in .env file.

### Without Docker

- Clone this repo to your local machine. If you use IntelliJ as IDE, open this project there.

- MySQL (and MySQL Workbench, optionally) must be already installed in your machine. Otherwise, you will have to install them. Please notice that the default parameters (port, username and password) to enable the MySQL connection are defined on application.properties file. So, feel free to edit them in order to match one of your MySQL connections.

```
# Create the db

CREATE SCHEMA `user_db` ;
```

- Run the project as Spring Boot App

## Usage

- Postman or any other API tester must be already installed in your machine. Otherwise, you will have to install them. You can perform the requests below in order to test the application. They belong to *User management API* collection, which can be easly imported to Postman with [this](https://www.getpostman.com/collections/f4b461a677e6d06ae204) shareable link. 

| Action | HTTP request method | Endpoint | Body example |
| ------------- | ------------- | ------------- | ------------- |
| Create new user | POST  | **/api/user**  | {"fname": "Steven", "lname": "Adams"} |
| Read all users | GET  | **/api/users** | |
| Read user | GET  | **/api/user**/3 | |
| Update user | PUT  | **/api/user** | {"id": "3", "fname": "Anthony", "lname": "Davis"}|
| Delete user | DELETE  | **/api/user**/3 | |


## References

I have accomplished the aforementioned goals thanks to the following courses:

- [Angular-4 with Spring boot Rest CRUD operations](https://www.youtube.com/watch?v=ioYJx-rNNoI&list=PLF0fAweo0Kogzy5I6LxEaIlJAxVORXZm-&index=1)
- [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)


