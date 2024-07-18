# Home_Automation
The Home Automation System uses microcontrollers like Arduino or ESP8266 to control home appliances such as lighting, temperature, and security. Integrating IoT devices and networking protocols, it offers a centralized interface for efficient and seamless remote management of home utilities.
# Home Automation System
- In this ESP32 project, I have explained how to make IoT-based projects using ESP32 with Google Home & Alexa. With this Internet of Things project, you can control 3 home appliances with Google Assistant, - Alexa, and manual switches. You can also control the relays from Google Home and Amazon Alexa App from anywhere in the world.

- And you don’t need any Google Nest or Amazon Echo Dot devices for this voice control home automation project.

![Home Automation System](images/home-automation-diagram.png)
- With this home automation project, you can control & monitor the real-time feedback of the relays in the Google Home and Alexa App from anywhere in the world. If the Wi-Fi is available, the ESP32 will automatically connect with the Wi-Fi.
![Home Automation System](images/home-automation-diagram.png)
- For this project, I have used all the FREE tools. So if you follow all the steps, you can easily make this Smart Home System with Google Home and Amazon Alexa to control the appliances with voice commands.

## Circuit of the ESP32 Home Automation
![Home Automation System](images/home-automation-diagram.png)
- I have used D23, D22, D21 & D19 GPIO to control the 4-channel relay module.

- And the GPIO D13, D12, D14 & D27 are connected with switches to control the relay module manually.

- I have used the INPUT_PULLUP function in Arduino IDE instead of using the pull-up resistors with each push button.

- As per the source code, when the control pins of the relay module receive a LOW signal the relay will turn on and the relay will turn off for the HIGH signal in the control pin.

- I have used a 5V 5Amp mobile charger to supply the circuit.

### Required Components for the ESP32 projects
- ESP32 DevKIT V1
- 4-channel 5V SPDT Relay Module
- Manual Switches or Pushbuttons
- Amazon Echo Dot (optional)
- Google Nest Mini (optional)
### Sinric Pro FREE account setup
- For this smart house project, I have used the Sinric Pro Free account. First, you have to add 3 devices to the Sinric Pro account.

- I have already explained, how to set up and add devices to Sinric Pro in following article.

- **Sinric Pro Account Setup**
- **Connect Sinric Pro with Alexa App**
- **Connect Sinric Pro with Google Home App**

### Program ESP32 with Arduino IDE
- 1. Update the Preferences –> Additional Boards Manager URLs: https://dl.espressif.com/dl/package_esp32_index.json, http://arduino.esp8266.com/stable/package_esp8266com_index.json
- 2. Then install the ESP32 board from the Board Manager or Click Here to download the ESP32 board.
- 3. Download the required libraries from the following links:
  - Sinric Pro by Boris Jaeger (Download Sinric Pro examples for ESP8266 & ESP32)
  - WebSockets by Markus Sattler (minimum Version 2.3.5)
  - ArduinoJson by Benoit Blanchon (minimum Version 6.12.0)

- Please download the latest version of the libraries from the given links. Then install the libraries at Arduino IDE **– Sketch – Include Library –** Add Zip Library.
- Enter the APP KEY and APP SECRET with Wi-Fi name and Wi-Fi password in the code.

- You can get the APP KEY and APP SECRET under the Credentials menu in Sinric Pro

- #define WIFI_SSID         "YOUR-WIFI-NAME"    
- #define WIFI_PASS         "YOUR-WIFI-PASSWORD"
- #define APP_KEY           "YOUR-APP-KEY"
- #define APP_SECRET        "YOUR-APP-SECRET"
- Also enter the device id in the code. You will find the Device ID from Devices menu.

- //Enter the device IDs here
- #define device_ID_1   "SWITCH_ID_NO_1_HERE"
- #define device_ID_2   "SWITCH_ID_NO_2_HERE"
- #define device_ID_3   "SWITCH_ID_NO_3_HERE"
- #define device_ID_4   "SWITCH_ID_NO_4_HERE"
- **After adding a device in Sinric Pro, a unique ID will be assigned to that device. If you create 3 devices, then there will be 3 unique device IDs.**

- As I am using a free Sinric pro account, so I have entered the 3-device IDs. (Sinric Pro gives 3 devices for FREE)


- Uncomment the following line if you use pushbuttons instead of toggle switches.

- //#define TACTILE_BUTTON 1
- After uploading the code to ESP32, please refer to the following articles for connecting the Sinric Pro Account with Amazon Alexa and Google Home App.

- **Connect Sinric Pro with Alexa App**
- **Connect Sinric Pro with Google Home App**
- After doing all these steps, now you control the appliances with Google Assistant and Alexa.

### ESP32 control Relays with Alexa App
- If the ESP32 is connected with Wi-Fi, then you can ask Alexa, to turn on the light [“Alexa, Turn ON Room Light“]. Thus, you can control the appliances like light, fan, etc with voice commands using
- Amazon Alexa App, and also monitor the current status of the switches from anywhere in the world from the Alexa App.
- ![Home Automation System](images/home-automation-diagram.png)

## ESP32 control Relays with Google Assistant
-  ![Home Automation System](images/home-automation-diagram.png)
- You can also ask Google Assistant, to control the light [“Hey Google, Turn ON the Room Light“]. Thus, you can control the appliances like light, fan, etc with voice commands using Google Assistant, and also monitor the real-time feedback and control the relays from anywhere in the world from the Google Home App.

## Control relays manually with Switches
-  ![Home Automation System](images/home-automation-diagram.png)
- You can always control the appliances manually with switches or push buttons and monitor the real-time status in Google Home and Alexa App.

## Conclusion
The Home Automation System is a comprehensive project that showcases proficiency in microcontroller programming, electronics, IoT, and networking protocols. It demonstrates the ability to create a practical and user-friendly solution for managing home utilities, providing a solid foundation for roles in embedded systems and IoT development.
