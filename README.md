`                                          `**JAVA Backend and REST API**

**Table of Content:**

- Introduction
- Abstract
- Technologies & Tools Used
- Model Architecture
- Task Structure
- Project Setup
- Results
- Methodology
- Future Enhancements
- Author

**Introduction:**
**\
`       `This is a Java-based Spring Boot application that provides a RESTful API to manage and execute "Task" objects representing shell commands. It supports creating, retrieving, deleting, and running tasks, with execution metadata stored in MongoDB. The API is tested using Postman and is suitable for backend task orchestration and automation.

**Abstract:**
**\
`    `This project is a Spring Boot-based RESTful application designed to manage and execute shell command tasks through a clean API interface. Each task consists of metadata such as ID, name, owner, command, and a list of execution records. The application supports creating, retrieving (by ID or name), deleting tasks, and executing commands securely while logging output and execution times. All task data is persistently stored in a MongoDB database. Command execution is carefully validated to prevent unsafe or malicious input. The system is ideal for use cases involving task automation, remote command execution, or backend job orchestration. Built using Java JDK 20, Spring Boot, MongoDB, and tested via Postman, this project showcases REST API development, NoSQL integration, and safe system-level command execution.

` `Keyword: REST API, Task Execution, MongoDB

**Technologies & Tools Used:**

- Java JDK
- IntelliJ IDEA
- MongoDB
- Postman
- Spring Web
- Spring Data MongoDB
- Validation API

**Model Architecture:**

- Spring Boot Framework to create a robust, scalable, and production-ready Java backend REST API.
- MongoDB for NoSQL storage of Task and TaskExecution objects, enabling efficient document-based querying and persistence.
- Spring Data MongoDB for seamless integration between Spring and MongoDB using repository interfaces.
- RESTful Controllers to define endpoints for task creation, retrieval, deletion, search, and execution via clean HTTP methods (GET, PUT, DELETE).
- Service Layer for business logic separation, handling command validation, execution tracking, and response formatting.
- Shell Command Execution via Java's ProcessBuilder, ensuring proper handling and sanitization of user-supplied commands.
- Validation Layer using javax.validation annotations to ensure task input fields meet safety and structural requirements.
- Postman / curl used for testing all REST endpoints with request/response visual verification.

**Task Structure:**
**\
`      `“id”: “123”, 

`      `“name”: ”Print Hello”, 

`      `“owner”:”John Smith”, 

`      `“command”: “echo Hello World again!” 
## <a name="_rt7c4lw5dtxd"></a>**Project Setup:**
- Group ID: com.example
- Artifact ID: task-manager
- Base package: com.example.taskmanager

**Project Structure:**
**\
`              `task-manager/

├── src/

│   ├── main/

│   │   ├── java/

│   │   │   └── com/

│   │   │       └── example/

│   │   │           └── taskmanager/

│   │   │               ├── TaskManagerApplication.java

│   │   │               ├── controller/

│   │   │               │   └── TaskController.java

│   │   │               ├── model/

│   │   │               │   ├── Task.java

│   │   │               │   └── TaskExecution.java

│   │   │               ├── repository/

│   │   │               │   └── TaskRepository.java

│   │   │               └── service/

│   │   │                   ├── CommandExecutorService.java

│   │   │                   ├── CommandValidator.java

│   │   │                   └── TaskService.java

│   │   └── resources/

│   │       └── application.properties

│   └── test/

├── build.gradle

└── settings.gradle


**Result:**

`  `###IntelIJ IDEA- Task Manager Application 

`        `![Task Application](images/1\_task\_application.png)

`  `###Mongodb- Running in CommandPrompt

`        `![Mongodb](images/2\_mongodb\_output.png)

` `###Postman Window- (Get,Put,Post,Delete)

`        `![Postman Window](images/3\_postman\_window.png)

` `###Mongodb Compass- Final Backend Output 

`        `![Backend Output](images/4\_final\_backend\_output\_mongodb.png)



**Methodology:**

- Designed a layered Spring Boot application structure with controller, service, model, repository, and configuration packages.
- Defined Task and TaskExecution entities with appropriate fields (ID, name, owner, command, timestamps, and output).
- Connected to MongoDB using Spring Data MongoDB for persistent storage and easy CRUD operations.
- Implemented RESTful endpoints for task creation, retrieval (by ID and name), deletion, and command execution.
- Validated user input using Java Bean Validation (@Valid, @NotNull, etc.) to prevent malformed requests.
- Executed shell commands securely using ProcessBuilder while capturing output and execution time.
- Appended each command execution result to the corresponding task’s taskExecutions list.
- Tested all endpoints using Postman to verify functionality, data persistence, and output integrity.
- Logged application behavior for debugging and monitoring purposes.

**How to Run:**
- **\
  `  `Clone the repository\
\
  **https://github.com/[[SoniaPugalendran/Java-Backend-and-REST-API](https://github.com/SoniaPugalendran/Java-Backend-and-REST-API)]/task-manager.git**  

`          `**cd task-manager**

- Open the project in IntelliJ IDEA 
- Ensure MongoDB is running
- Default URI: mongodb://localhost:27017
- Database name: taskdb (or update in application.properties)
- Run the application\
  `       `Navigate to TaskManagerApplication.java\
  `       `Click Run \
  `       `Test the REST API using Postman or curl
- Create, fetch, delete, search, and execute tasks\
  `       `POST http://localhost:8080/tasks
- `  `View Results
- Outputs include command execution start/end time and shell output
- Task data is persisted in MongoDB and can be verified using tools like MongoDB Compass.
### <a name="_hveffotnc24p"></a>**Future Enhancements:**
- Integration with a Kubernetes cluster to execute shell commands directly within pods for real-world task orchestration.
- Addition of a frontend UI using React or Angular for visualizing tasks, executions, and outputs interactively.
- Storage of execution logs and outputs in cloud storage or centralized log systems (e.g., AWS S3, ELK Stack) for analysis and auditing.
- Integration with WebSockets for real-time updates on task execution status.

Author

SoniaPugalendran

[SoniaPugalendran/](https://github.com/SoniaPugalendran/Network-Intrusion-Detection-System-Using-DeepLearning)Java-Backend-and-REST-API

Date:11/06/2025

