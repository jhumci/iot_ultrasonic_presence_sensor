# Ultrasonic presence sensor with housing to MQTT


## Description

* Ultrasonic-Sensor transmitting distance measurements to MQTT.
* Additionaly you can use MQTT->Telegraf->InfluxDB->Grafana for Visualization.
* Visualization for last 50 measurements can also be done via the django project.
* Housing for Ultrasonic-Sensor and ESP32 for easy installation on every surface.

The microcontroller sends distance measurements to the MQTT Server. 
In the python code it is possible to adjust the max_req_dist & cooldown to manage presence detection.

# Project structure:
[iot_ultrasonic_presence_sensor/](./iot_ultrasonic_presence_sensor)
  * [datasheets/](./iot_ultrasonic_presence_sensor/datasheets)
    * [HC-SR04_ultraschallmodul_beschreibung_3.pdf](./iot_ultrasonic_presence_sensor/datasheets/HC-SR04_ultraschallmodul_beschreibung_3.pdf) // Datasheet of our sensor
  * [esp32_code/](./iot_ultrasonic_presence_sensor/esp32_code)
    * [esp32_code.ino](./iot_ultrasonic_presence_sensor/esp32_code/esp32_code.ino) // Code for ESP32 Microcontroller
  * [housing/](./iot_ultrasonic_presence_sensor/housing)
    * [Base.ipt](./iot_ultrasonic_presence_sensor/housing/Base.ipt)
    * [Base.stl](./iot_ultrasonic_presence_sensor/housing/Base.stl)
    * [Upper.ipt](./iot_ultrasonic_presence_sensor/housing/Upper.ipt)
    * [Upper.stl](./iot_ultrasonic_presence_sensor/housing/Upper.stl)
  * [python_script/](./iot_ultrasonic_presence_sensor/python_script)
    * [python_script.py](./iot_ultrasonic_presence_sensor/python_script/python_script.py) // simple script to get presence status
    * [requirements.txt](./iot_ultrasonic_presence_sensor/python_script/requirements.txt) // requirements for python script & django project
    * [visualisierung/](./iot_ultrasonic_presence_sensor/python_script/visualisierung)
  * [README.md](./iot_ultrasonic_presence_sensor/README.md) // Project description (this file)




## Hardware

* ESP32
* Ultrasonic-Sensor HC-SR04
* Cable
* Power supply for ESP32 and Ultrasonic-Sensor 


## Making & Using the sensor

* Print the housing
* Adapt your SSID for internet connection and the adress for the MQTT server in the microcontroller files.
* Connect the sensor to the microcontroller via GPIO-Pins. -> Make sure to use the pins used in the code.
* Copy the software onto the microcontroller.
* Place the sensor and the microcontroller in the housing.
* Connect the microcontroller to power
* Enjoy

