# Creating a Fullstack Application from Scratch with Java Spring and React

Welcome to the tutorial "Creating a Fullstack Application from Scratch with Java Spring and React". This is **Part 1** of the series, where we will cover backend development using **Java Spring Boot** and **PostgreSQL**.

## Overview

In this tutorial, we will build the backend of a fullstack application using Java Spring Boot. The application will be a RESTful API that provides data for the frontend, which will be developed in Part 2 using React.

## Objectives

- Set up a Spring Boot project with PostgreSQL.
- Create a RESTful API with basic endpoints.
- Integrate Spring Data JPA for data persistence.
- Test the application using tools like Postman.

## Prerequisites

Before you start, you should have:

- [Java JDK 17+](https://www.oracle.com/java/technologies/javase-downloads.html)
- [Maven](https://maven.apache.org/download.cgi) (or [Gradle](https://gradle.org/install/), if preferred)
- [PostgreSQL](https://www.postgresql.org/download/) (installed and running)
- [Postman](https://www.postman.com/downloads/) (to test the API)

## Project Setup

1. **Create a New Spring Boot Project**

   Use the [Spring Initializr](https://start.spring.io/) to create a new Spring Boot project with the following options:

   - Project: Maven Project (or Gradle Project)
   - Language: Java
   - Spring Boot: [Latest stable version]
   - Dependencies: Spring Web, Spring Data JPA, PostgreSQL Driver

   Click "Generate" to download the project.

2. **Import the Project**

   Unzip the downloaded file and import it into your preferred IDE (e.g., IntelliJ IDEA or Eclipse).

3. **Configure the Database**

   Open the `src/main/resources/application.properties` file and configure the connection to PostgreSQL:

   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/your_database
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.show-sql=true
   spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
