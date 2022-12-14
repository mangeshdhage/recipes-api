**Recipe application** allows users to manage their favourite recipes which involves adding, updating, removing and fetching recipes.
It allows user to filter the recipes based on category, number of servings, ingredients(Include/Exclude) and instructions.

**Documentation about the architectural choices of Recipe application** 

The application has been implemented on the basis of Spring Boot architecture which is similar to Spring MVC. 
It is a REST application implemented using Java 8.
The workflow goes like:
1) The user makes the HTTP request through swagger.
2) This request goes to the controller, and the controller maps and handles it.
3) The request is then passed on to the service layer where all the business logic is implemented on the data that is mapped to JPA with entity classes.

REST API has been documented using **OpenAPI Specification (OAS)** Version 3.0.3.

Unit tests and Integration tests have been implemented for Context load, Controller and Business logic.

The Recipe application is connected to MySQL database to persist data using JPA repository. I have used **Azure Database for MySQL servers**. 
The db details are present in appication.yml file.

**Microsoft Azure environment details** :

The application has been hosted on **Microsoft Azure** and can be accessed using URL - **https://recipes-application.azurewebsites.net/swagger-ui/index.html#/**

I have enabled all the actuator endpoints which can be accessed using - https://recipes-application.azurewebsites.net/actuator

**SonarCloud link** : https://sonarcloud.io/summary/new_code?id=mangeshdhage_recipes-api&branch=main to assess code quality.

**Local environment details**

Swagger link : http://localhost:8082/swagger-ui/index.html#/Recipes

Actuator- http://localhost:8082/actuator/

Basic authentication and authorization have been implemented. Below are the credentials to login to Swagger link to access the endpoints.

**User name** : **test_user**

**Password** : **test_pwd**