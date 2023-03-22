# **🍿cinema-app📽️**
**The project was created using Spring and Hibernate technologies. 
This project is a simple Java backend part of the application 
that allows you to  send HTTP requests by endpoints(GET, POST, PUT, DELETE) depending on their role.
You can use this application by sending requests through Postman**

## **⚡️Functionality**
### 🔐Authorisation
* POST: /login - log in as a user/admin
* GET: /logout - log out
### 🛃Ordering (user access level)
* PUT: /shopping-carts/movie-sessions?movieSessionId - add a new ticket to user's shopping cart
* GET: /shopping-carts/by-user - display current user's shopping cart
* POST: /orders/complete - create a new order based on user's shopping cart contents
* GET: /orders - display current user's order history
### 📫Info center (user/admin access level)
* GET: /movies - display info about all movies
* GET: /movie-sessions/available?movieId&date - display available movie sessions for specified movie and date
* GET: /cinema-halls - display all cinema halls
### 🗳️Managing (admin access level)
* GET: /users/by-email?email - display info about some user by his email
* POST: /movies - add a new movie (requested params: title and (optional) description)
* POST: /cinema-halls - add a new cinema hall (requested params: capacity and (optional) description)
* POST: /movie-sessions - add a new movie session (requested params: movieId, cinemaHallId and showTime)
* PUT: /movie-sessions/{id} - update info about some movie session by its id
* DELETE: /movie-sessions/{id} - delete some movie session by its id

##   Instructions for run the project🦾
1. Download the code from [GitHub](https://github.com/diana-lomei/cinema-app) and save it to your computer.
2. Install [JDK](https://www.oracle.com/cis/java/technologies/downloads/)
3. Install [MySQL](https://dev.mysql.com/downloads/installer/)
4. Open MySql Workbench and create a new database.
5. Open the db.properties in package resources and fill in the appropriate fields(URL, USERNAME, PASSWORD, JDBC_DRIVER).
6. Download [Tomcat](https://tomcat.apache.org/download-90.cgi) (v.9.0.73)
7. Set up your Tomcat
*   at the top near to the "run" button, click "Edit Configurations"
* then click "Add new Configuration"(it's "+") in the upper left corner
* select "Tomcat Server - local"
* click "Fix" and select "web-security:war exploded"
* and delete any new link that appeared after the "/"
* This is what your link should look like http://localhost:8080/
8. Press the Run button or the Shift + F10 hotkey combination.🧑🏼‍💻
9. You can use email "alice@i.ua" and password "1234" fot authentication or register new user.
10. You can test endpoints in Postman.🕹️

##     🛠️Used technologies🛠️
* Java
* MySQL
* TomCat
* Hibernate Core
* Hibernate Validator
* Spring
* Apache Maven
* JavaServlet API
* Dependency Injection With Field Injection (Injector)

#   📻️Structure
### 🤳🏻Config
* package contains main configuration classes required by Spring, Hibernate.
### 🤖Controller
* package contains controllers for processing requests, accepts requests from clients and send responses.
### ⚙️Dao
* all the work with the database takes place at this package.
### 📮Dto
* package contains classes for providing information in http requests and responses.
### ❗️Exception
* package contains custom exception - DataProcessingException.
### 📇Lib
* package contains custom annotations and validators for email and password confirmation.
### 🔗Model
* package contains the main classes: CinemaHall, Movie, MovieSession, Order, Role, ShoppingCart, Ticket, User.
### 🔒Security
* package contains class CustomUserDetailsService for providing session-term authorisation.
### 🔧️Service
* package contains all business logic and providing connection between controller and dao levels.
### 🗓️Util
* package for working with date type data.
### ⛓️Resources
* database connection package.
![img](https://user-images.githubusercontent.com/116308273/226889944-6999c9da-46be-4e91-b484-72a2de016419.png)


