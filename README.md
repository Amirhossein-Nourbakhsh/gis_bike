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
#### Summary of the APIs. Note that all the APIs are implemented by using MEAN-Stack.   
|IP and Port|Name|Input|Output|
|----------|-------------|------|------|
| (http://212.90.102.16:4242) |   getWeathermap |  (lat,long) |  Json Object |
| (http://212.90.102.16:4242) |   getTrafficLs |  (lattop, lontop, latbtm, lonbtm) | Json Object  |
| (http://212.90.102.16:4242) | fuzzyReasoning  | (speed, tr, col, weather)  | String |
| (http://212.90.102.16:4242) |   sendNotification |  (firebaseId, txtAlarm) |  String |

#### Here are two examples of getting results:
* In order to get weather condition in an area the "getWeathermap" API will be used as follow:
  * /getweathermap?lat&long
  * Intead of "lat" & "long" put the latitude and longitude of a specific area:
  * http://212.90.102.16:4242/amir/getweathermap?lat=43.77&long=-79.492749
  * The results should be similar to the following image:
   ![Architecture](/Img/16weather.PNG)
* In order to test the Fuzzy Reasoning API, the third API in the table will be used as follow:
   * /fuzzyreasoning?speed={speed}&tr={traffic-flow}&col={collisions}&weather={weather condition}
   * Instead of {speed}, {traffic-flow}, {collisions}, and {weather condition} put the actual values and test the results, for example:
   * http://212.90.102.16:4242/amir/fuzzyreasoning?speed=13&tr=2&col=20&weather=rainy
