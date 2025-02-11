# POWERSN SMART ENERGY METER IITM PRODUCT DEVELOPMENT
 --------------------------------------------------
TEAM K-TECH Sree Kanna 
# Table of the Content

- [INTRODUCTION](#introduction)
- [OVER VIEW OF PRODUCT](#OVER-VIEW-OF-PRODUCT)
- [OPERATAION OF THE SYSTEM](#OPERATAION-OF-THE-SYSTEM)
- [FEATURES AND BENEFITES OF THE PRODUCT](#FEATURES-AND-BENEFITES-OF-THE-PRODUCT)
- [ADVANTAGES OF THE PRODUCT](#ADVANTAGES-OF-THE-PRODUCT)
- [TABLE OF COMPONENTS REQUIRED & COST FOR THE PRODUCT](#TABLE OF COMPONENTS REQUIRED & COST FOR THE PRODUCT)
- [PIN OUT TABLE](#PIN-OUT-TABLE)
- [BLOCK DIAGRAM OF THE SYSTEM](#BLOCK-DIAGRAM-OF-THE-SYSTEM)
- [CIRCUIT DIAGRAM OF THE SYSTEM](#CIRCUIT-DIAGRAM-OF-THE-SYSTEM)
- [INTRODUCTION TO ARDUINO IOT CLOUD](#INTRODUCTION-TO-ARDUINO-IOT-CLOUD)
- [USER DASHBOARD OF ARDUINO IOT CLOUD IN PC](#USER-DASHBOARD-OF-ARDUINO-IOT-CLOUD-IN-PC)
- [SOURCE CODE OF VSDSQUARDRON MINI AND ESP32](#SOURCE-CODE-OF-VSDSQUARDRON-MINI-AND-ESP32)
- [IMAGES OF THE PROJECT](#IMAGES-OF-THE-PROJECT)
- [DEMONSTRATION VIDEO OF THE PRODUCT](#DEMONSTRATION-VIDEO-OF-WORKING )
- [DEMONSTRATION VIDEO OF FINAL PRODUCT](#DEMONSTRATION-VIDEO-OF-FINAL-PRODUCT)
- [ABOUT](#ABOUT)
- [CONCLUSION](#Conclusion)

  
# INTRODUCTION  
- The development of IoT-based smart energy meters marks a significant step forward in energy management technology. These devices utilize the Internet of Things (IoT) to enable real-time monitoring, precise data collection, and user-friendly interfaces, addressing key challenges faced by both consumers and power companies. They promote energy awareness and encourage responsible usage.

- Smart energy meters provide several benefits, including cost savings, operational efficiency, and environmental sustainability. By offering detailed insights into energy consumption patterns, they empower consumers to make informed decisions, reduce energy bills, and adopt sustainable practices. For power companies, they improve demand management, minimize energy losses, and enhance the reliability of power distribution.

- This project aims to develop a low-cost IoT-based smart energy meter to address these challenges. The proposed meter will enable real-time monitoring and accurate energy consumption tracking, ensuring both efficiency and affordability.


# OVER VIEW OF PRODUCT  

- The IoT Smart Energy Meter project aims to deliver a low-cost, efficient solution for monitoring energy consumption by utilizing the VSD Squadron Mini Board with an LCD display and a relay module. This system measures real-time energy usage and presents the data on the LCD screen, ensuring immediate and local monitoring.

- To enable cloud-based communication, the project incorporates an ESP module, which facilitates wifi communication for transmitting data to an IoT platform. This integration allows users to remotely track and analyze energy consumption patterns, making the solution suitable for a wide range of applications, from smart homes to industrial settings.

- By combining the advanced features of the VSD Squadron Mini Board and IoT connectivity, the project aims to enhance energy

# OPERATAION OF THE SYSTEM  

- The smart energy meter solution combines hardware and software to monitor energy consumption and calculate costs in real time. The system begins with a traditional energy meter that generates pulses corresponding to the consumed energy. To ensure safety, these pulses are isolated from the microcontroller using an optocoupler with lm393 comparator.

 - The pulses are processed using the VSD Squadron Mini Board, which counts them to calculate energy usage. The board also computes the cost of consumed energy based on a predefined cost per unit. This data, including energy usage and cost, is displayed on the connected LCD screen for local, real-time monitoring. A relay module enables integration with external devices for further control or automation, while a reset button allows users to clear the data after payment, starting a new billing cycle.

- For cloud communication, the system incorporates an ESP module, which handles wifi communication to transmit processed data to an IoT platform. Users can remotely access and analyze energy usage and cost data through the cloud, leveraging platforms such as the Arduino IoT Cloud or similar services. A user-friendly interface is available via IoT remote apps, allowing users to monitor consumption, costs, and reset data conveniently.

 - The entire system is developed using the Arduino IDE, providing a robust environment for coding and deploying the firmware necessary for data processing, communication, and control. This integration of the VSD Squadron Mini Board with IoT capabilities offers a reliable, scalable, and user-friendly solution for efficient energy and cost management.


# FEATURES AND BENEFITES OF THE PRODUCT 

 **1.	Real-Time Monitoring:** The smart meter will provide real-time data on energy consumption, allowing users to track their usage and make informed decisions to reduce power consumption.
 
**2.	Accurate Area-Wide Data Collection:** By aggregating data from all connected meters, substations can have precise information on the total energy consumption in their areas, enabling better management and planning.

**3.	Reduced Power Loss Discrepancies:** Accurate and real-time data collection will help identify and address discrepancies between area consumption and substation records, reducing unrecorded consumption and potential energy theft.

**4.	Data Backup and Retrieval:** The IoT-based system will ensure that energy consumption data is backed up in the cloud. In case of meter failure or damage, the data can be retrieved, preventing losses for power companies.

**5.	Cost-Effectiveness:** The solution aims to be low-cost, making it affordable for widespread adoption in both household and industrial settings.

**6.	Enhanced Transparency:** Users will have access to their consumption data, fostering transparency and trust between consumers and power companies.

The development and deployment of a low-cost IoT-based smart energy meter will address the shortcomings of current energy meters. It will provide real-time monitoring, accurate data collection, and efficient energy management, ultimately reducing losses and enhancing transparency between consumers and power companies.

# ADVANTAGES OF THE PRODUCT 

**1. Real-Time Monitoring:** Consumers can monitor their energy usage in real-time, helping them understand their consumption patterns and identify ways to save energy.

**2. Billing Accuracy:** With precise data, smart meters ensure accurate billing based on actual usage rather than estimates, reducing disputes between consumers and energy providers.

**3. Cost Savings:** By providing insights into energy consumption, smart meters enable consumers to adjust their habits to reduce energy usage and lower their bills.

**4. Remote Readings:** Energy providers can read meters remotely, eliminating the need for physical visits and reducing operational costs.

**5. Energy Efficiency:** The detailed data collected by smart meters can be used to develop more effective energy-saving programs and policies.

**6. Load Management:** Energy providers can better manage the demand and supply of electricity, reducing the risk of blackouts and ensuring a stable energy supply.

**7. Support for Smart Grids:** Smart meters are a critical component of smart grids, which use digital technology to manage electricity more efficiently, reliably, and sustainably.

**8.Fraud Detection:** Enhanced monitoring capabilities allow for the detection of tampering and unauthorized usage, helping to reduce energy theft.


# TABLE OF COMPONENTS REQUIRED & COST FOR THE PRODUCT

| Item                                            |             Quantity              |  COST       |
|---------                                        |            -----                  |   ------    |
|Single phase Energy meter 240v 50Hz              |                     1             |    500      |
|  4N35 Optocoupler                               |                     1             |     10      |
|VSDSquadron mini                                 |                     1             |    999      |
| ESP32 MODULE                                    |                     1             |    250      |
| 16x2 I2CLCD display                             |                     1             |    200      |
| Connecting wires                                |                     1Set          |    50       |
|2 CH relay5V -240V                               |                     1             |    100      |
|5 voltage regulator adaptor                      |                     1             |    100      |
| Zero PCB                                        |                     1             |    150      |
| Case box                                        |                     1             |    200      |
|                                                 |                                   |    2559     |

# PIN OUT TABLE  

# Smart Energy Meter with VSDSquadron Mini & ESP32

## Wiring Connections

| **Component**          | **Pin/Connection**   | **Connected To**                           |
|-----------------------|--------------------|------------------------------------------|
| **Energy Meter**       | Pulse Output       | Optocoupler (Input)                      |
| **Optocoupler (4N35)** | Input              | Energy Meter Pulse Output                |
|                        | Output             | VSDSquadron Mini GPIO Input (PD2)        |
| **VSDSquadron Mini**   | GPIO Pin (PD2)     | LM393 Input                              |
|                        | GPIO Pin (PD3)     | ESP32 (D15)                              |
| **Internal Reset**    |  ESP32 (D14)         | VSDSquadron Mini (PD4)                 |
| **Relay Module**       | Signal Pin         | ESP32 (D13)                             |
|                        | VCC                | 3.3V/5V (depending on relay)             |
|                        | GND                | GND                                      |
|                        | COM                | Power Line (Common)                      |
|                        | NO (Normally Open) | Load (Device Being Controlled)           |
|                        | NC (Normally Closed) | Optional (for fail-safe connections)     |
| **5V Adapter**        | Phase              | Phase of the Energy Meter                |
|                        | Neutral            | Neutral of the Energy Meter              |
|                        | 5V                 | VSDSquadron Mini & ESP32 VCC              |
|                        | GND                | VSDSquadron Mini & ESP32 GND              |
| **LM393 Comparator**  | D0                 | VSDSquadron Mini GPIO PD2                |
|                        | VCC                 | VSDSquadron Mini 3V                      |
|                        | GND                | VSDSquadron Mini GND                     |
| **I2C LCD**          | SDA                 | VSDSquadron Mini GPIO (PC1)              |
|                        | SCL                | VSDSquadron Mini GPIO (PC2)              |
|                        | VCC                 | VSDSquadron Mini 5V                      |
|                        | GND                | VSDSquadron Mini GND                     |
## Notes:
- The **Optocoupler (4N35)** is used to isolate the energy meter pulse output from the microcontroller.
- The **LM393 Comparator** helps in processing the pulse signals.
- The **ESP32** handles communication with the VSDSquadron Mini.
- The **Relay Module** is used to control a load (appliance) based on energy consumption monitoring.

# BLOCK DIAGRAM OF THE SYSTEM 
![Blank diagram (2)](https://github.com/user-attachments/assets/ea67b2c5-ab37-4ff1-8182-ba275ba62140)

---------------

# CIRCUIT DIAGRAM OF THE SYSTEM 
![SMART ENERGY METER](https://github.com/user-attachments/assets/8ba171aa-518e-4bb0-8243-177e08539b9a)

----------------

# INTRODUCTION TO ARDUINO IOT CLOUD 

- The Arduino IoT Cloud is an integrated platform designed to facilitate the development and deployment of IoT projects. It enables seamless connectivity and management of devices, allowing users to control and monitor the project remotely. For this project, the Arduino IoT Cloud serves as the backbone, connecting the smart energy meter to the internet and enabling real-time data visualization and remote control.

- With the Arduino IoT Cloud, We can create and manage IoT devices through an easy-to-use interface. The platform supports a variety of Arduino boards, including the popular ESP32 and MKR series, which are well-suited for IoT applications. By leveraging the Arduino IoT Cloud, we can define properties such as energy consumption, cost, and relay states, which are updated and synchronized with the cloud. This allows us to monitor the energy consumption of our smart meter in real-time and make informed decisions based on the data collected.

- The cloud platform provides robust tools for data logging, visualization, and alerting. we can create dashboards to visualize energy consumption trends and costs over time, enabling better energy management and cost-saving strategies. Additionally, the platform supports integrations with third-party services, enhancing the functionality of IoT project.

- Security is a crucial aspect of IoT deployments, and the Arduino IoT Cloud ensures secure communication between your devices and the cloud through SSL/TLS encryption. This ensures that our data remains protected from unauthorized access and tampering.

- Overall, the Arduino IoT Cloud simplifies the development process, offering a reliable and scalable solution for IoT projects. By using the Arduino IoT Cloud, this smart energy meter project can provide real-time monitoring, remote control, and data analysis, enhancing energy management and enabling smarter decision-making.

#  USER DASHBOARD OF ARDUINO IOT CLOUD IN PC 

![Screenshot (235)](https://github.com/user-attachments/assets/ef0668d3-cf12-4b06-8213-0431355d34c0)


# USER DASHBOARD OF ARDUINO IOT CLOUD IN  MOBILE
 

![WhatsApp Image 2025-02-10 at 18 05 35](https://github.com/user-attachments/assets/22b94917-1b79-4fdd-97ce-385a74237b53)


# SOURCE CODE OF VSDSQUARDRON MINI AND ESP32 

# code for VSDSquardron mini
```
#include <Arduino.h>
#include <Wire.h>
#include <LiquidCrystal_I2C.h>

volatile int pulseCount = 0;      // Variable to store pulse count
int sensorPin = PD2;                // Pin connected to the LDR sensor (Interrupt pin)
int mirrorPin = PD3;                // Pin to output mirror pulses
int resetButtonPin = PD4;           // Pin for reset button
const int pulsesPerKWH = 10;      // Number of pulses per kWh
const int costPerKWH = 3;         // Cost per kWh in Rs

// I2C LCD configuration
LiquidCrystal_I2C lcd(0x27, 16, 2); // Change 0x27 to your LCD's I2C address if needed

void countPulse() {
  pulseCount++;                 // Increment pulse count
  digitalWrite(mirrorPin, HIGH); // Output pulse to mirror pin
  delayMicroseconds(100);        // Short pulse width
  digitalWrite(mirrorPin, LOW);  // Reset mirror pin
}

void setup() {
  pinMode(sensorPin, INPUT_PULLUP);  // Configure sensor pin as input with pull-up resistor
  pinMode(mirrorPin, OUTPUT);        // Configure mirror pin as output
  pinMode(resetButtonPin, INPUT_PULLUP); // Configure reset button pin as input with pull-up resistor
  digitalWrite(mirrorPin, LOW);      // Ensure mirror pin is LOW initially

  // Attach interrupt to the sensor pin for rising edge
   attachInterrupt(
    sensorPin,                 // GPIO pin
      GPIO_Mode_IPU,             // Input mode with pull-up
      countPulse,                // Callback function
      EXTI_Mode_Interrupt,       // Interrupt mode
      EXTI_Trigger_Rising        // Trigger on rising edge
  );

  // Initialize I2C LCD
  lcd.init();
  lcd.backlight();
  lcd.setCursor(0, 0);
  lcd.print("System Initializing");
  delay(2000);
  lcd.clear();
}

void loop() {
  static unsigned long lastDisplayTime = 0;

  // Calculate kWh and cost based on pulse count
  int kWh = pulseCount / (int)pulsesPerKWH; // Convert pulse count to kWh
  int cost = kWh * costPerKWH;                // Calculate cost 

  // Check if the reset button is pressed
  if (digitalRead(resetButtonPin) == LOW) {
    pulseCount = 0; // Reset pulse count
    lcd.clear();    // Clear the LCD display
    lcd.setCursor(0, 0);
    lcd.print("Data Reset");
    delay(2000);    // Delay to show "Data Reset" message
    lcd.clear();    // Clear the LCD again for new data
  }

  // Update LCD every second
  if (millis() - lastDisplayTime >= 1000) {
    lastDisplayTime = millis();

    // Update LCD with kWh and cost
    lcd.setCursor(0, 0); // First row
    lcd.print("kWh: ");
    lcd.print(kWh); // Display kWh with 3 decimal places
    lcd.setCursor(0, 1); // Second row
    lcd.print("Cost: Rs ");
    lcd.print(cost); // Display cost with 2 decimal places
  }
}
```
# code for esp module 

```
#include <ArduinoIoTCloud.h>
#include "thingProperties.h"
#include <Arduino_ConnectionHandler.h>
#include <WiFi.h>
#include <Wire.h>
#include <EEPROM.h> // Include the EEPROM library
#include <LiquidCrystal_I2C.h> // Include the I2C LCD library

const char THING_ID[] = "7e6b9eb0-e7ef-4d26-be40-93e38d639052"; // Replace with your Thing ID

#define I2C_ADDR 0x27 // I2C address for the LCD
#define LCD_COLUMNS 16
#define LCD_ROWS 2

LiquidCrystal_I2C lcd(I2C_ADDR, LCD_COLUMNS, LCD_ROWS);

// Define the GPIO pins
const int pulsePin = 15; // Change this to the pin you are using
const int resetPin = 4;  // Pin connected to the reset button
const int relayPin0 = 13;  // Pin connected to the relay
const int relayPin1 = 12;
const int arduinoResetPin = 14;  // Pin to trigger Arduino reset (set this to a GPIO pin on ESP32)

// Number of impulses per kWh (3200 for this meter)
const int impulsesPerKWh = 10; // Change the pulses

// Variables to store pulse count and energy consumption
volatile unsigned long pulseCount = 0;
float energyConsumed = 0.0;

// EEPROM address to store energy consumed
const int eepromAddress = 0;

// Price per kWh (replace with your rate)
const float pricePerKWh = 3; // Example price

// Cloud variables
void IRAM_ATTR onPulse() {
  pulseCount++;
}

void setup() {
  // Initialize I2C LCD display
  lcd.init();
  lcd.backlight();
  lcd.setCursor(0, 0);
  lcd.print("SMART ENERGY METER");
  delay(2000);
  lcd.clear();

  // Initialize serial communication
  Serial.begin(115200);
  initProperties();

  // Set the pulse pin as input
  pinMode(pulsePin, INPUT);
  // Set the reset pin as input with internal pull-up resistor
  pinMode(resetPin, INPUT_PULLUP);
  // Set the relay pin as output
  pinMode(relayPin0, OUTPUT);
  pinMode(relayPin1, OUTPUT);
  pinMode(arduinoResetPin, OUTPUT);  // Set reset pin to output
  digitalWrite(arduinoResetPin, HIGH);

  // Attach interrupt to the pulse pin, triggered on falling edge
  attachInterrupt(digitalPinToInterrupt(pulsePin), onPulse, FALLING);

  // Initialize EEPROM
  EEPROM.begin(1024);

  // Retrieve the stored energy consumed from EEPROM
  EEPROM.get(eepromAddress, energyConsumed);

  // Calculate initial pulse count based on retrieved energy consumed
  pulseCount = energyConsumed * impulsesPerKWh;

  // Display setup information
  Serial.println("Energy meter pulse counting initialized.");

  // Initialize Arduino IoT Cloud
  ArduinoCloud.begin(ArduinoIoTPreferredConnection);
  ArduinoCloud.addProperty(resetKwh, READWRITE, ON_CHANGE, onResetKwhChange);
  ArduinoCloud.addProperty(relayState, READWRITE, ON_CHANGE, onRelayStateChange);
  ArduinoCloud.addProperty(kwhConsumed, READ, ON_CHANGE);
  ArduinoCloud.addProperty(cost, READ, ON_CHANGE);

  setDebugMessageLevel(2);
  ArduinoCloud.printDebugInfo();
}

void loop() {
  // Arduino IoT Cloud update
  ArduinoCloud.update();

  // Check if the reset button is pressed locally
  if (digitalRead(resetPin) == LOW) {
    resetEnergyConsumption();
  }

  // Calculate energy consumption in kWh
  energyConsumed = pulseCount / (float)impulsesPerKWh;
  kwhConsumed = energyConsumed; // Update cloud variable

  // Calculate the cost
  cost = energyConsumed * pricePerKWh;

  // Display energy consumption and cost on LCD
  lcd.setCursor(0, 0);
  lcd.print("Energy: ");
  lcd.print(energyConsumed, 3);
  lcd.print(" kWh");

  lcd.setCursor(0, 1);
  lcd.print("Cost: ");
  lcd.print(cost, 2);
  lcd.print(" Rs");

  // Store the current energy consumed in EEPROM
  EEPROM.put(eepromAddress, energyConsumed);
  EEPROM.commit();

  // Delay to reduce serial output rate (adjust as needed)
  delay(1000);
}

void onResetKwhChange() {
  if (resetKwh) {
    resetEnergyConsumption();
  }
}

void onRelayStateChange() {
  digitalWrite(relayPin0, relayState ? HIGH : LOW);
  digitalWrite(relayPin1, relayState ? HIGH : LOW);
}

void resetEnergyConsumption() {
  pulseCount = 0;
  energyConsumed = 0.0;
  EEPROM.put(eepromAddress, energyConsumed);
  EEPROM.commit();

  // Display reset message
  Serial.println("Energy consumption reset to 0 kWh");
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.print("Energy Reset");
  delay(1000);
  lcd.clear();

  resetKwh = false; // Reset the cloud variable

  // Trigger Arduino reset by sending two low pulses
                           // Wait for 100 ms
  digitalWrite(arduinoResetPin, LOW); // Release the reset pin
  delay(500);                          // Wait for 100 ms
  digitalWrite(arduinoResetPin, HIGH);  // Second pulse
  delay(500);  ; // Wait for 100 ms

  // After sending the pulses, the Arduino will reset
}

void onCostChange()  {
  // Add your code here to act upon Cost change
}
```

# IMAGES OF THE PROJECT
![WhatsApp Image 2025-02-10 at 2 19 44 PM](https://github.com/user-attachments/assets/06d6a0a3-83c5-4be5-a5f1-5294343d0f87)

----------





# DEMONSTRATION VIDEO OF WORKING 

https://github.com/user-attachments/assets/905f6e65-d3f0-4a9c-80a3-a6ab19f6df79


 # DEMONSTRATION VIDEO OF FINAL PRODUCT


 https://drive.google.com/file/d/1prFfpnhG7gM3UL4GvOCPkTISeyRGW-vz/view?usp=sharing
 




# ABOUT 
We are Team K-Tech Sree Kanna , Rajashekhar and Navaneeth Kumar, and we have developed a low-cost IoT-based smart energy meter designed for the DIR-V Product Development Hackathon. Our system seamlessly integrates hardware and software components to deliver an efficient and scalable energy management solution
The hardware includes an energy meter with pulse output, an optocoupler for electrical isolation, the VSD Squadron Mini Board for processing, an ESP module for wifi cloud communication, an LCD display for local data visualization, and a relay module for turning on and off the mains supply control functions.
- Users can observe their energy consumption values in real-time on their mobile devices via the Arduino IoT Remote app, which also offers the capability to turn the system on or off if the bill is not paid, adding a layer of financial management. The app further allows users to reset the data, starting a new billing cycle. This smart energy meter system can be implemented in various settings, including home energy meters, industrial applications, EV charging stations, and prepaid energy meters, offering versatile and scalable solutions for different energy management needs. The integration of these technologies offers real-time energy monitoring, cost savings, user control, enhanced safety, and cloud-based analysis. By providing comprehensive and reliable energy management, our smart energy meter solution empowers users to optimize their energy usage and reduce costs effectively.
- This smart energy meter system is versatile and can be implemented in home energy meters, industrial applications, EV charging stations, and prepaid energy metering, providing scalable solutions for different energy management needs. By integrating real-time monitoring, cost savings, user control, enhanced safety, and cloud-based analysis, our solution empowers users to optimize their energy usage and reduce costs effectively.
  
# CONCLUSION  
The smart energy meter project effectively integrates hardware and software components to deliver a reliable and user-friendly solution for real-time energy monitoring and cost management. By utilizing the VSD Squadron Mini Board, optocoupler, LCD display, relay module, and ESP module, the system ensures precise energy consumption tracking, cost calculation, and seamless cloud-based data access.
Users benefit from real-time feedback displayed on the LCD screen, remote monitoring through IoT platforms, and easy interaction via IoT apps, making energy management more efficient and transparent. This versatile solution is adaptable for use in homes, EV charging stations, and industrial settings, offering scalable energy monitoring and control across various applications.
 
