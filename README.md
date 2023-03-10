# cinema-app

Simple cinema service app that supports authentication, registration and CRUD operations.

### Functionality

When a person logs in they have one of two roles (ADMIN or USER), which restricts access to certain functionality of the program.

ADMIN can:
- Get/add cinema halls and movies.
- Get available movie sessions and add/update/delete other ones.
- Get users by their emails.

USER can:
- Get cinema halls, movies and available movie sessions.
- Get all orders and complete any of them.
- Get a shopping cart and add tickets for movie sessions to it.

Also, there is a registration page which is available to everyone.

All endpoints and roles that have access to them are presented in [`cinema/config/SecurityConfig.java`](https://github.com/Iryna-a/cinema-app/tree/main/src/main/java/cinema/config/SecurityConfig.java).

### Project structure

The project is built by the N-tire architecture principle. It has 3 layers:
- Presentation (controllers in [`cinema/controller`](https://github.com/Iryna-a/cinema-app/tree/main/src/main/java/cinema/controller))
- Service ([`cinema/service`](https://github.com/Iryna-a/cinema-app/tree/main/src/main/java/cinema/service))
- Data access ([`cinema/dao`](https://github.com/Iryna-a/cinema-app/tree/main/src/main/java/cinema/dao))

![diagram](Cinema_Uml.png)

### Technologies

- JDK 17
- Maven 3.8.6
- Tomcat 9.0.50
- MySQL 8.0.22
- Hibernate 5.6.14
- Spring (Spring Core, Spring Web, Spring Security) 5.6.10

### How to run the application

- Clone this project.
- Make sure you have Tomcat 9.0.50 installed.
- Make sure you use MySQL as a database otherwise you need to change a dependency in pom.xml.
- Edit URL, username, password and JDBC driver in [`resources/db.properties`](https://github.com/Iryna-a/cinema-app/blob/main/src/main/resources/db.properties).
- Edit Tomcat configuration.
- Run `mvn clean package` in terminal.
- Run the application (the first user with ADMIN role will be created automatically: email - admin@i.ua, password - admin123).
