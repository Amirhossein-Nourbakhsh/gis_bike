# gis_bike
## Instruction of using APIs and the Android App
### The architecture of the system is shown on the image bellow.
![Architecture](/Img/architecture.PNG)
### Please download the apk app and install on your Android smartphone. 
* Click on the code button.
* Download the code as ZIP file.
* Extract the ZIP file and install the apk file on the Android smartphone.
![Architecture](/Img/test.PNG)
### Assign Firebase ID for the app
* Once the app is installed successfully, a unique ID will be assigned to the app and can be visible in the app.
* Click on the button on top of the screen (Show Token).
* Copy and Paste the code to get access to the APIs. 
![Architecture](/Img/app1.jpg)

### Get access to the APIs
   
|IP and Port|Name|Input|Output|
|----------|-------------|------|------|
| (http://195.248.241.80:4242) |   getWeathermap |  (lat,long) |  Json Object |
| (http://195.248.241.80:4242) |   getTrafficLs |  (lattop, lontop, latbtm, lonbtm) | Json Object  |
| (http://195.248.241.80:4242) | fuzzyReasoning  | (speed, tr, col, weather)  | String |
| (http://195.248.241.80:4242) |   sendNotification |  (firebaseId, txtAlarm) |  String |
