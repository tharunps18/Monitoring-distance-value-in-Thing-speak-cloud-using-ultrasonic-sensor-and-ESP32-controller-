# NAME: THARUN P S
# REF NO: 24900117
# EX.NO: 6 Monitoring-distance-value-in-Thing-speak-cloud-using-ultrasonic-sensor-and-ESP32

# Uploading ultrasonic sensor data in Thing Speak cloud

# AIM:
To monitor the distance of the obstacle in the Thing speak cloud using ultrasonic sensor and ESP32 controller.
# Apparatus required:
ESP32 Controller,<br>
Ultrasonic Sensor,<br>
Power supply,<br>
Connecting wires,<br>
Bread board<br>
# PROCEDURE:
## Arduino IDE
Step1:Open the Arduino IDE<br>
Step2: Go to sketch- include library – manage libraries file and install esp32 and thing speak library file<br>
Step3:Go to file and select new file option<br>
Step4:Type the program and update the thing speak channel ID, API key, wifi password and ID<br>
Step5:Go to file and select save option to save the program<br>
Step6:Go to sketch and select verify or compile options<br>
Step7:If no error Hex file will be generated in the temporary folder<br>
Step8: Connect all the components as per the circuit diagram<br>
Step9: Connect the programming cable with esp32 and PC.<br>
Step10: Check the jumper position and connect 4 & 5 of P4.<br>
Step11. Upload the program in the esp32.<br>
Step12 Press the boot button in ESP32 and then press and release the reset button after release the boot button<br>
Step13 Check the output in the cloud<br>
## Thingspeak
Step1 Create a ThingSpeak Account<br>
Step2 Log in to your ThingSpeak account<br>
Step3 Create a new channel by navigating to "Channels" and clicking on "New Channel."<br>
Step4 Configure your channel settings, such as Field labels and Channel name<br>
Step5 Copy the Channel ID and API key in the thingspeak and update in the program<br>
Step6 Execute your program to send the sensor value to ThingSpeak<br>
Step7 Check your ThingSpeak channel to verify that the sensor value has been updated<br>
# THEORY:
## Ultrasonic sensor:
The HC-SR04 is a type of ultrasonic sensor which uses sonar to find out the distance of the object from the sensor. It provides an outstanding range of non-contact detection with high accuracy & stable readings. It includes two modules like ultrasonic transmitter & receiver. This sensor is used in a variety of applications like measurement of direction and speed, burglar alarms, medical, sonar, humidifiers, wireless charging, non-destructive testing, and ultrasonography.
### HC-SR04 Ultrasonic Sensor Pin Configuration
This sensor includes four pins and the pin configuration of this sensor is discussed below.

![image](https://github.com/user-attachments/assets/19050fb2-5138-4a32-85d8-f781f705a0df)


•	Pin1 (Vcc): This pin provides a +5V power supply to the sensor.<br>
•	Pin2 (Trigger): This is an input pin, used to initialize measurement by transmitting ultrasonic waves by keeping this pin high for 10us.<br>
•	Pin3 (Echo): This is an output pin, which goes high for a specific time period and it will be equivalent to the duration of the time for the wave to return back to the sensor.<br>
•	Pin4 (Ground): This is a GND pin used to connect to the GND of the system.<br>
### Features
The features of the HC-SR04 sensor include the following
•	The power supply used for this sensor is +5V DC<br>
•	Dimension is 45mm x 20mm x 15mm<br>
•	Quiescent current used for this sensor is <2mA<br>
•	The input pulse width of trigger is10uS<br>
•	Operating current is 15mA<br>
•	Measuring angle is 30 degrees<br>
•	The distance range is 2cm to 800 cm<br>
•	Resolution is 0.3 cm<br>
•	Effectual Angle is <15°<br>
•	Operating frequency range is 40Hz<br>
•	Accuracy is 3mm<br>
### HC-SR04 Ultrasonic Sensor Working
The HC-SR04 Ultrasonic sensor comes with four pins namely Vcc pin, Trigger pin, Echo pin, & Ground pin. This sensor is used to measure the accurate distance between the target and the sensor. This sensor mostly works on the sound waves.
When the power supply is given to this module, it generates the sound waves to travel throughout the air to hit the necessary object. These waves strike and come back from the object, then collects by the receiver module.
Here both the distance as well as time has taken is directly proportional because the time taken for more distance is high. If the trigger pin is kept high for 10 µs, then the ultrasonic waves will be generated which will travel at the sound speed. So it creates eight cycles of sonic burst that will be gathered within the Echo pin. This ultrasonic sensor is interfaced with Arduino to gauge the necessary distance between sensor & object. The distance can be calculated using the following formula.
S = (V x t)/2 <br>
Where the ‘S’ is the required distance<br>
‘V’ is the sound’s speed <br>
‘t’ is the time taken for sound waves to return back after striking the object.<br>
The actual distance can be calculated by dividing its value with 2 as the time will be twice once the waves travel and get back from the sensor.
## What is IoT?
Internet of Things (IoT) describes an emerging trend where a large number of embedded devices (things) are connected to the Internet. These connected devices communicate with people and other things and often provide sensor data to cloud storage and cloud computing resources where the data is processed and analyzed to gain important insights. Cheap cloud computing power and increased device connectivity is enabling this trend.IoT solutions are built for many vertical applications such as environmental monitoring and control, health monitoring, vehicle fleet monitoring, industrial monitoring and control, and home automation.

![image](https://github.com/user-attachments/assets/493f5a4f-9e29-44b4-8ae7-176879daf5e4)

 
Sending Data to Cloud with ESP32 and ThingSpeak
ThingSpeak is an Internet of Things (IoT) analytics platform that allows users to collect, analyze, and visualize data from sensors or devices connected to the Internet. It is a cloud-based platform that provides APIs for storing and retrieving data, as well as tools for data analysis and visualization.The Internet of Things ( or IoT) is a network of interconnected computing devices such as digital machines, automobiles with built-in sensors, or humans with unique identifiers and the ability to communicate data over a network without human intervention.Hello readers, I hope you all are doing great. In this tutorial, we will learn how to send sensor readings from ESP32 to the ThingSpeak cloud. Here we will use the ESP32’s internal sensor like hall-effect sensor and temperature sensor to observe the data and then will share that data cloud.
## What is ThingSpeak?

![image](https://github.com/user-attachments/assets/5a35cd2f-6083-47dd-9b4b-7d18a56a8a3e)

It is an open data platform for IoT (Internet of Things). ThingSpeak is a web service operated by MathWorks where we can send sensor readings/data to the cloud. We can also visualize and act on the data (calculate the data) posted by the devices to ThingSpeak. The data can be stored in either private or public channels.ThingSpeak is frequently used for internet of things prototyping and proof of concept systems that require analytics.
Features Of ThingSpeak
ThingSpeak service enables users to share analyzed data through public channels:
ThingSpeak allows professionals to prepare and analyze data for their businesses:
ThingSpeak updates various ThingSpeak channels using MQTT and REST APIs:
Easily configure devices to send data to ThingSpeak using popular IoT protocols.
Visualize your sensor data in real-time.
Aggregate data on-demand from third-party sources.
Use the power of MATLAB to make sense of your IoT data.
Run your IoT analytics automatically based on schedules or events.
Prototype and build IoT systems without setting up servers or developing web software.

![image](https://github.com/user-attachments/assets/c7746b27-dca6-4b9f-9e71-b24f3e57b6c8)

 
# PROGRAM:
~~~
#include "ThingSpeak.h"
#include <WiFi.h>

char ssid[] = "tharunps"; //SSID
char pass[] = "tharun#123"; // Password


const int trigger = 25;
const int echo = 26;
long T;
float distanceCM;
WiFiClient  client;

unsigned long myChannelField =2792164 ; // Channel ID
const int ChannelField = 1; // Which channel to write data
const char * myWriteAPIKey = "HF6JQNUBORCD8NBU"; // Your write API Key

void setup()
{
  Serial.begin(115200);
  pinMode(trigger, OUTPUT);
  pinMode(echo, INPUT);
  WiFi.mode(WIFI_STA);
  ThingSpeak.begin(client);
}
void loop()
{
  if (WiFi.status() != WL_CONNECTED)
  {
    Serial.print("Attempting to connect to SSID: ");
    Serial.println(ssid);
    while (WiFi.status() != WL_CONNECTED)
    {
      WiFi.begin(ssid, pass);
      Serial.print(".");
      delay(5000);
    }
    Serial.println("\nConnected.");
  }
  digitalWrite(trigger, LOW);
  delay(1);
  digitalWrite(trigger, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigger, LOW);
  T = pulseIn(echo, HIGH);
  distanceCM = T * 0.034;
  distanceCM = distanceCM / 2;
  Serial.print("Distance in cm: ");
  Serial.println(distanceCM);
  ThingSpeak.writeField(myChannelField, ChannelField, distanceCM, myWriteAPIKey);
  delay(1000);
}
~~~
# CIRCUIT DIAGRAM:
![image](https://github.com/user-attachments/assets/2ffd548e-7ff6-4303-a4bf-496857d22945)

# OUTPUT:
![398443177-ecc19feb-a8c7-43a4-8151-f8fe282b5c64](https://github.com/user-attachments/assets/eeffdc78-6a9f-41c2-8a78-69834716ced1)

# RESULT:
Thus the distance values are updated in the Thing speak cloud using ESP32 controller.

