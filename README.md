# UserManagementAppliction
Project Description
This User Management Application is a simple web-based application built using Java, JSP (JavaServer Pages), Servlets, and MySQL. The application provides basic CRUD (Create, Read, Update, Delete) functionalities for managing users. It is developed using Eclipse IDE.

Features
Create User: Add new user details to the database.
Read User: View details of all users from the database.
Update User: Edit existing user details.
Delete User: Remove user details from the database.
Technologies Used
Frontend: JSP, HTML, CSS
Backend: Java, Servlet
Database: MySQL
IDE: Eclipse
Prerequisites
JDK 8 or higher
Apache Tomcat server
MySQL database
Eclipse IDE
Project Setup

Database Setup
Install MySQL and create a database called user_management.
Create a table users with the following structure:

CREATE DATABASE user_management;

USE user_management;

CREATE TABLE users (
    id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    country VARCHAR(100) NOT NULL,
    PRIMARY KEY (id)
);
Eclipse Project Setup
Clone the repository:
git clone https://github.com/yourusername/user-management-application.git

Open Eclipse:
Select File > Import.

Choose Existing Projects into Workspace and select the project directory.
Configure Tomcat Server:
Right-click on the project in Eclipse.
Select Run As > Run on Server.
Choose your configured Tomcat server.

Configuration
Database Configuration:
Update the database connection details in DatabaseUtil.java (located in src/com/example/util):

public class DatabaseUtil {
    private static String jdbcURL = "jdbc:mysql://localhost:3306/user_management";
    private static String jdbcUsername = "your_mysql_username";
    private static String jdbcPassword = "your_mysql_password";
    // Other methods
}

Project Structure
src/
com.example.dao.UserDAO.java - Data Access Object for database operations.
com.example.model.User.java - User model class.
com.example.util.DatabaseUtil.java - Utility class for database connection.
com.example.web.* - Servlet classes for handling requests.
WebContent/
index.jsp - Home page displaying user list.
user-form.jsp - Form for creating and updating users.
WEB-INF/web.xml - Servlet configuration.

Usage
Start the server:
Right-click on the project.
Select Run As > Run on Server.

Access the application:
Open a web browser and navigate to http://localhost:8080/user-management-application/.

Perform CRUD operations:
Use the interface to add, view, update, or delete users.

