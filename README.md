# Fire Station Incident Management System

A Java web application for reporting and managing fire-related incidents, coordinating volunteers, exchanging messages, and viewing operational statistics.

## Purpose

The application was developed as an individual university database and web-programming exercise. Its goal was to connect a role-based browser interface to a relational data model and implement complete incident-management workflows with Java Servlets and MySQL.

## Features

- User and volunteer registration
- Authentication for users and administrators
- Fire-incident reporting and status updates
- Volunteer availability and assignment to incidents
- Active, submitted, and volunteer-specific incident views
- Incident details and operational statistics
- Incident-related messaging
- Profile updates and role-specific pages

## Technologies

- Java Servlets
- JDBC
- MySQL
- Maven
- HTML and CSS
- JavaScript and AJAX
- JSON and Gson
- WAR deployment

## Backend structure

The application separates request handlers by HTTP responsibility:

- `DoPostServlets` contains commands such as registration, login, incident reporting, volunteer assignment, messaging, and updates.
- `DoGetServlets` contains queries for incidents, volunteers, messages, assignments, and statistics.
- `DataBaseConnection` provides the JDBC connection to the `event_management` MySQL database.
- `MyServlet` initializes the main database tables required by the application.

## Running the original submission

The original Maven project is stored in `project_hy359_csd5097.zip`.

1. Install Java, Maven, MySQL, and a Servlet 4-compatible container such as Apache Tomcat 9.
2. Create a local MySQL database named `event_management`.
3. Extract the archive and review the connection settings in `DataBaseConnection.java`.
4. Build the WAR with `mvn package`.
5. Deploy the generated WAR to the servlet container.

## Repository status

This repository contains an archived university submission. The application currently uses local development database settings and should not be deployed publicly without moving credentials into environment-based configuration and reviewing authentication and input-validation behaviour.
