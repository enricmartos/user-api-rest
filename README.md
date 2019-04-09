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
- H2

*Dependency management tool*
- Gradle

*IDE*
- IntellIJ Idea

## Build setup

- Clone this repo to your local machine. If you use Spring Tool Suite as IDE, open this project there:

```
# Import the project to STS

File -> Import -> Git -> Projects from Git -> Existing local repository -> Add ${Directory where you have cloned the repo} -> Import existing Eclipse projects
```

- Run the project as Spring Boot App

- Postman or any other API tester must be already installed in your machine. Otherwise, you will have to install them. You can perform the requests below in order to test the application:

| Action | HTTP request method | Endpoint | Body example |
| ------------- | ------------- | ------------- | ------------- |
| Create new user | POST  | **/api/user**  | {"fname": "Steven", "lname": "Adams"} |
| Read all users | GET  | **/api/users** | |
| Read user | GET  | **/api/user**/3 | |
| Update user | PUT  | **/api/user** | {"id": "3", "fname": "Anthony", "lname": "Davis"}|
| Delete user | DELETE  | **/api/user**/3 | |


## References

I have accomplished the aforementioned goals thanks to the following course:

- [Angular-4 with Spring boot Rest CRUD operations](https://www.youtube.com/watch?v=ioYJx-rNNoI&list=PLF0fAweo0Kogzy5I6LxEaIlJAxVORXZm-&index=1)

