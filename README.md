## **How to use**
 ### **step 1 - clone the project**
 ### **step 2 - there are 2 setup project**
     1 -setup.sh for running the application if python is installed in the client device 
     2- setup-docker.sh for running the application in the docker 
 ### **step 3 - make the script excutable, choose the commond based on the prefrence***
     1-If using `setup.sh`, the commands to be followed are:**
         `chmod +x setup.sh`
         `./setup.sh`
     2- if using `setup-docker.sh`, command to be followed 
        `chmod +x setup-docker.sh`
        `./setup-docker.sh`
### **step 4 - now project is running in the port =8000**
use the example-json file to take the json body for each api end point

### ** Api endpoints **
GET - http://127.0.0.1:8000/api/weather/daily_summary/
Get - http://127.0.0.1:8000/api/weather/name/Delhi
GET - http://127.0.0.1:8000/api/weather
