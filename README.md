## **How to use**
 ### **step 1 - clone the project**
     git clone https://github.com/saikatM333/WeatherReport.git
 ### **step 2 - there are 2 setup project**
     1 -setup.sh for running the application if python is installed in the client device
     2- setupDocker.sh for running the application in the docker
 ## choose based on your prefrence 3.1 or 3.2 ##    
 ### **step 3.1 - If using `setup.sh`, the commands to be followed are:***
   
         chmod +x setup.sh
         ./setup.sh
     
  ### **step 3.2 - if using `setupDocker.sh`, command to be followed***
    
        chmod +x setupDocker.sh
        ./setupDocker.sh      
  ### ** Note : step 4 - it will ask secret Key and api key ** ###
     for secret key just press the enter key it will automaticaly genearate it 
     for api key use your open wether api key 
### **step 5 - now project is running in the port =8000**


### ** Api endpoints **
GET - http://127.0.0.1:8000/api/weather/daily_summary/
Get - http://127.0.0.1:8000/api/weather/name/Delhi
GET - http://127.0.0.1:8000/api/weather

### ** cities included ** ###
  "Delhi", "Mumbai", "Chennai", "Bangalore", "Kolkata", "Hyderabad"

## Design Choices ##
### **1 . Modular Architecture**
Django Structure: The project follows Django’s modular architecture, where functionalities are organized into apps. This makes the application easier to manage, maintain, and extend.
### ** 2. Dockerization ** ###
Containerization: The application is containerized using Docker, providing an isolated environment for running the Django app. This ensures consistency across development, testing, and production environments.
Docker Compose: Using Docker Compose allows multiple services (like web servers, databases, etc.) to be defined and run together easily, managing dependencies and configurations.
### ** 3. Environment Configuration ** ###
.env Files: The use of environment variable files (.env) to store configuration settings (like database credentials, API keys) keeps sensitive information secure and configurable without hardcoding values in the source code.
PYTHONUNBUFFERED=1: This environment variable ensures that output from print statements is immediately flushed to the console, making debugging easier by providing real-time logs.
###  ** 4. Development Best Practices ** ###
Unbuffered Output: The unbuffered output option (-u) in the Python command ensures that logs and print statements are immediately displayed, aiding in debugging and monitoring.
Volume Mapping: The application code is mounted as a volume in the Docker container (.:/app), allowing for live code updates without needing to rebuild the Docker image during development.
### ** 5. API Design ** ###
RESTful API Endpoints: The application exposes RESTful API endpoints for fetching weather data (e.g., /api/weather/, /api/weather/daily_summary/). This design choice makes it easy for front-end applications or other services to interact with the back end.
Clear URL Routing: The endpoints are clearly defined, enhancing usability and making it easier for developers to understand how to interact with the service.
### ** 6. Dependency Management ** ###
requirements.txt: The application uses a requirements.txt file to manage Python package dependencies. This file is essential for building the Docker image, ensuring that all necessary packages are installed.
### **7. Logging and Monitoring** ###
Print Statements for Logging: The use of print statements for debugging and monitoring output is a straightforward method to keep track of application behavior during development. This is especially helpful in a Dockerized environment where traditional logging mechanisms may be less accessible.

### **Model-View-Template (MVT) Architecture ** ###
MVT Pattern: Django follows the MVT architectural pattern, which is a variant of the Model-View-Controller (MVC) pattern. Here’s how it fits into your application:
Model: Represents the data structure, where the application's data models define the structure of the weather data you are handling. In Django, this is typically done using Django’s ORM (Object-Relational Mapping).
View: Contains the business logic of the application, processing requests, and returning responses. In your case, views would handle API requests related to weather data (e.g., fetching weather information, handling queries).
Template: Manages the presentation layer, defining how data is presented to users. While your application appears to be an API, if there were any HTML pages, this layer would manage their rendering.
### ** Separation of Concerns ** ###
Organized Code Structure: The application likely separates different functionalities into distinct files and directories (e.g., models, views, URLs), enhancing maintainability and readability. This follows the principle of separation of concerns, ensuring that each part of the application has a single responsibility.

### ** Event-Driven Architecture ** ###
Asynchronous Processing: If your application were to implement features such as background tasks or notifications (e.g., APScheduler for asynchronous tasks), it would lean towards an event-driven architecture, where components react to events rather than direct calls.
