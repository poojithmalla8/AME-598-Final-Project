# AME-598-Final-Project- Crop Prediction System Using IoT

# Crop Prediction System Using IoT

Smart Agriculture can help in increasing the efficiency of the harvest process and also reduce production costs and production loss. So, predicting the
type of crop based on soil properties would help in reducing production loss and help in generating maximum harvest and best quality crop. The proposed system connects the agricultural field to the internet and extracts real-time farm information and uses this data in predicting the soil condition and suggesting the crop to harvest for the season. This system uses the sensor, server, and ML model to improve the quality of the harvest and make the best out of the soil.

## Table of Contents

| S.No. | Title |
|-----:|-----------|
|     1| Prerequisites|
|     2| Components    |
|     3| Deployment       |
|     4| Working    |
|     5| Results       |

### Prerequisites

What things you need to install the software and how to install them

```
Ardiono:- https://www.arduino.cc/en/software
Python:- https://www.python.org/downloads/
Data Set:- https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset
```
## Using **Arduino IDE**

1. Install the current upstream Arduino IDE at the 1.8 level or later. The current version is at the [Arduino website](http://www.arduino.cc/en/main/software).
2. Start Arduino and open Preferences window. In additional board manager add url: https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json .separating them with commas.
3. Copy or move the folder in the **lib** directory to `<C:\Users\Your User Name\Documents\Arduino\libraries>` 
4. Board select `Tools` -> `Board` -> `ESP32 Dev Module`
5. In `configuration.h`, you can select hotspots and connect to wireless WiFi, and you can change and add sensors. For details, please refer to `configuration.h` 
6. Build and Upload the sketch
7. View the obtained ip address in the serial output,  enter the ip address in the browser to view the data.

## Using **PlatformIO**

1. Install [VSCODE](https://code.visualstudio.com/) and [Python](https://www.python.org/)
2. Search for the PlatformIO plug-in in the VSCODE extension and install it.
3. After the installation is complete and the reload is completed, there will be a small house icon in the lower left corner. Click to display the Platformio IDE home page
4. Go to file - > `Open folder` - > Select the `Repo` 
5. Click the (√) symbol in the lower left corner to compile (→) for upload.



## Components
* [LilyGO-Highgrow Sensor](https://www.aliexpress.us/item/2251832629468148.html?gatewayAdapt=glo2usa4itemAdapt&_randl_shipto=US) - Sensor to get plant data
![](https://github.com/Xinyuan-LilyGO/LilyGo-HiGrow/blob/master/image/img1.jpg)

![](https://github.com/Xinyuan-LilyGO/LilyGo-HiGrow/blob/master/image/img2.jpg)* 

## Deployment
![Project_Workflow](https://user-images.githubusercontent.com/111541172/206347884-0f0be09e-f16c-44a4-89de-8a0bfdbfa9cc.png)

* Hardware Deployment: For the purpose of collecting soil data, we are using the Lily-Go
Highgrow sensor, which has an ESP 32 chip, DHT11 (Temperature and humidity sensor),
soil moisture sensor, and BH1750 (Ambient Light Sensor)
* Server Interface: Tracking live soil data using a webpage and sending this data to the
cloud server.
* ML Model: Finally we retrieve the collected data from the cloud and run it through an
ML model. This model helps us in predicting the suitable crop based on soil data
collected.

## Working
* Sensor Data and Server:- This code is written in C++ and javascript using the Platform IO library to flash the code to the
hardware. The sensor is interfaced using a UART bus and communicated using the I2C protocol.
For the webpage to check real-time sensor data, we are using the ESP DASH library, which is a
UI library for ESP 32 and ESP 8266 microcontrollers. The classroom lectures helped me in
creating the environment, understand I2C communication, and create a client/server model using
HTTP. For this model, we are using HTTP instead of the website, majorly because of the firewall
by the Windows OS while deploying the WebSocket server. I personally recommend the
WebSocket server as it provides a faster connection and faster transfer of data with minimal data
loss compared to the HTTP server.
* ML Model:- This code is written in Python, using pandas, NumPy, sklearn, and tree libraries. The code ideally
retrieves the data from the server using pandas and trains the data using the sklearn library and
provides a decision tree classification using the tree library. Finally, the code provides the crop
that can be harvested and also estimates the rate of the correctness of the prediction made. This
course helped in understanding the use of IoT and its integration with ML/AI models to refine
the result. For this project, I used the Crop Prediction Dataset which has the crop data of 2200
different soil conditions, and trained it using the sklearn library


## Results
![image](https://user-images.githubusercontent.com/111541172/206350152-3714c865-0c44-43d6-84e6-db88a0189b69.png)
Real-time Soil Data

![image](https://user-images.githubusercontent.com/111541172/206350192-cfbb2f82-bb5c-4337-8bdf-147f68b5dcad.png)
![image](https://user-images.githubusercontent.com/111541172/206350210-413f8c8e-3c29-4dfd-8103-80f8e2a1134c.png)
![image](https://user-images.githubusercontent.com/111541172/206350220-f93271ea-79b7-4c83-8067-1e4956d6b4cb.png)
![image](https://user-images.githubusercontent.com/111541172/206350236-841424e4-21bb-4d29-bfe7-3951203593e0.png)

Results after running the ML model and predicting the suitable crop based on the data taken from the data set.

## References
#### &ensp;[Installing UART Drivers](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers)
#### &ensp;[Lilygo Highgrow](https://github.com/Xinyuan-LilyGO/LilyGo-HiGrow) 
#### &ensp;[Crop Prediction](https://github.com/shan515/AI-Based_Crop-Predictor_App)


