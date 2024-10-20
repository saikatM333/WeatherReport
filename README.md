## **How to use**
 ### **step 1 - clone the project**
     git clone https://github.com/saikatM333/WeatherReport.git
 ### **step 2 - there are 2 setup project**
     1 -setup.sh for running the application if python is installed in the client device 
     2- setup-docker.sh for running the application in the docker 
 ## choose based on ypur prefrence 3.1 or 3.2 ##    
 ### **step 3.1 - If using `setup.sh`, the commands to be followed are:***
   
         chmod +x setup.sh
         ./setup.sh
     
  ### **step 3.2 - if using `setupDocker.sh`, command to be followed***
    
        chmod +x setupDocker.sh
        ./setupDocker.sh      
### **step 4 - now project is running in the port =8000**


### ** Api endpoints **
GET - http://127.0.0.1:8000/api/weather/daily_summary/
Get - http://127.0.0.1:8000/api/weather/name/Delhi
GET - http://127.0.0.1:8000/api/weather

### ** cities included ** ###
  "Delhi", "Mumbai", "Chennai", "Bangalore", "Kolkata", "Hyderabad"
