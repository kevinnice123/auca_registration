# AUCA Registration System

A simple Java web application built with Servlets for user authentication and search functionality.

## Project Overview

This is a Maven-based web application that demonstrates basic servlet functionality including login validation and search redirection.

## Features

- **User Login**: Login form with password strength validation
  - Warns users if password is less than 8 characters
  - Displays welcome message on successful login
  
- **Search Functionality**: Google search integration
  - Redirects user queries to Google search
  - Clean, Google-inspired UI design

## Technology Stack

- **Java**: Version 1.8
- **Build Tool**: Maven
- **Server**: Apache Tomcat 7
- **Framework**: Java Servlets (javax.servlet-api 4.0.1)
- **Testing**: JUnit 4.11

## Project Structure

```
auca_registration/
├── src/
│   └── main/
│       ├── java/
│       │   ├── LoginServlet.java      # Handles login authentication
│       │   └── RedirectServlet.java   # Redirects search queries to Google
│       └── webapp/
│           ├── index.html             # Basic login page
│           ├── login.html             # Styled login page (welcome page)
│           ├── search.html            # Search interface
│           └── WEB-INF/
│               └── web.xml            # Web app configuration
├── target/                            # Compiled files
└── pom.xml                            # Maven configuration
```

## How It Works

1. **Login Flow**:
   - User enters username and password
   - `LoginServlet` validates password length
   - User sees warning if password < 8 characters or welcome message if valid
   - Redirected to search page

2. **Search Flow**:
   - User enters search query
   - `RedirectServlet` redirects to Google with the search term

## Setup & Deployment

1. **Prerequisites**:
   - Java 8 or higher
   - Maven
   - Apache Tomcat server

2. **Build the project**:
   ```bash
   mvn clean install
   ```

3. **Deploy**:
   - Deploy the generated WAR file (`target/auca_registration.war`) to Tomcat
   - Or use Maven Tomcat plugin:
   ```bash
   mvn tomcat7:deploy
   ```

4. **Access**:
   - Navigate to: `http://localhost:8080/auca_registration/`

## Configuration

- **Server**: Configured in `pom.xml` for Tomcat deployment
- **Context Path**: `/auca_registration`
- **Welcome File**: `login.html`

## Author

AUCA (Adventist University of Central Africa)
