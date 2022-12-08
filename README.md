# AME-598-Final-Project- Crop Prediction System Using IoT

# Crop Prediction System Using IoT

Smart Agriculture can help in increasing the efficiency of the harvest process and also reduce production costs and production loss. So, predicting the
type of crop based on soil properties would help in reducing production loss and help in generating maximum harvest and best quality crop. The proposed system connects the agricultural field to the internet and extracts real-time farm information and uses this data in predicting the soil condition and suggesting the crop to harvest for the season. This system uses the sensor, server, and ML model to improve the quality of the harvest and make the best out of the soil.

## Table of Contents

| S.No. | Title |
|-----:|-----------|
|     1| Introduction|
|     2| Method    |
|     3| Process Flow       |
|     4| ML Model    |
|     5| Results       |

### Prerequisites

What things you need to install the software and how to install them

```
Ardiono:- https://www.arduino.cc/en/software
Python:- https://www.python.org/downloads/
Data Set:- https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset
```

## Deployment
![Project_Workflow](https://user-images.githubusercontent.com/111541172/206347884-0f0be09e-f16c-44a4-89de-8a0bfdbfa9cc.png)

● Hardware Deployment: For the purpose of collecting soil data, we are using the Lily-Go
Highgrow sensor, which has an ESP 32 chip, DHT11 (Temperature and humidity sensor),
soil moisture sensor, and BH1750 (Ambient Light Sensor)
● Server Interface: Tracking live soil data using a webpage and sending this data to the
cloud server.
● ML Model: Finally we retrieve the collected data from the cloud and run it through an
ML model. This model helps us in predicting the suitable crop based on soil data
collected.

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
