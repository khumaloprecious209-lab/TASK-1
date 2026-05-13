Task 1 – Spring Boot Basic Application

Project Overview
This is a simple Spring Boot application created as part of a university assignment.
The main purpose of this project is to demonstrate the basics of Spring Boot, including:
• creating a Spring Boot project using Maven
• building a REST controller
• handling HTTP GET requests
• understanding the behavior of @RestController and @GetMapping
• testing endpoints using a browser 


Technologies Used
• Java
• Spring Boot
• Spring Web
• Maven


Project Structure
Task1/
├── src/
│ ├── main/
│ │ ├── java/
│ │ │ └── com/example/task1/
│ │ │ ├── Task1Application.java
│ │ │ └── controller/
│ │ │ └── Task1Controller.java
│ │ └── resources/
│ │ └── application.properties
├── pom.xml
└── README.mdHow to Run the Application

How to run Project
1. open the project
Import the project into your IDE (IntelliJ IDEA / Eclipse).
2. Build the project
Use Maven to build the application:
mvn clean install
3. Run the application
Run the main class:
Task1Application.java
4. Application will start on:
http://localhost:8080
API Endpoints
1. Hello Endpoint
GET /hello
URL:
http://localhost:8080/hello
Response:
Hello from Task1 Spring Boot Application!
2. Info Endpoint
GET /info
URL:
http://localhost:8080/info
Response:This is a simple Spring Boot controller using @RestController (@ResponseBody included).


How It Works (Code Explanation)
@SpringBootApplication
This annotation is used in the main class and enables:
• auto-configuration
• component scanning
• Spring Boot application startup
@RestController
This annotation defines a REST API controller.
It is a combination of:
• @Controller
• @ResponseBody
This means that all returned values from methods are sent directly as HTTP responses (not
views).
@GetMapping
Used to map HTTP GET requests to specific methods.
Example:
@GetMapping("/hello")
This means when the user visits:
/hello
This method is executed.
Response HandlingEach method returns a String, which is automatically displayed in the browser or Postman
as plain text.

Testing the Application
You can test the application using:
Browser
• http://localhost:8080/greeting?name=Vistula
