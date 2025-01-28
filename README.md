# POWERSN_IIITM_PRODUCT_DEVELOPMENT
 --------------------------------------------------
TEAM K-TECH Sree Kanna 
# Table of the Content

- [INTRODUCTION](#introduction)
- [OVERVIEW OF THE PRODUCT](#OVER-VIEW-OF-THE-PRODUCT)
- 
# INTRODUCTION  
- The development of IoT-based smart energy meters marks a significant step forward in energy management technology. These devices utilize the Internet of Things (IoT) to enable real-time monitoring, precise data collection, and user-friendly interfaces, addressing key challenges faced by both consumers and power companies. They promote energy awareness and encourage responsible usage.

- Smart energy meters provide several benefits, including cost savings, operational efficiency, and environmental sustainability. By offering detailed insights into energy consumption patterns, they empower consumers to make informed decisions, reduce energy bills, and adopt sustainable practices. For power companies, they improve demand management, minimize energy losses, and enhance the reliability of power distribution.

- This project aims to develop a low-cost IoT-based smart energy meter to address these challenges. The proposed meter will enable real-time monitoring and accurate energy consumption tracking, ensuring both efficiency and affordability.


# OVER VIEW OF PRODUCT  

- The IoT Smart Energy Meter project aims to deliver a low-cost, efficient solution for monitoring energy consumption by utilizing the VSD Squadron Mini Board with an LCD display and a relay module. This system measures real-time energy usage and presents the data on the LCD screen, ensuring immediate and local monitoring.

- To enable cloud-based communication, the project incorporates an ESP module, which facilitates TX and RX communication for transmitting data to an IoT platform. This integration allows users to remotely track and analyze energy consumption patterns, making the solution suitable for a wide range of applications, from smart homes to industrial settings.

- By combining the advanced features of the VSD Squadron Mini Board and IoT connectivity, the project aims to enhance energy

# OPERATAION OF THE SYSTEM  

- The smart energy meter solution combines hardware and software to monitor energy consumption and calculate costs in real time. The system begins with a traditional energy meter that generates pulses corresponding to the consumed energy. To ensure safety, these pulses are isolated from the microcontroller using an optocoupler with lm393 comparator.

 - The pulses are processed using the VSD Squadron Mini Board, which counts them to calculate energy usage. The board also computes the cost of consumed energy based on a predefined cost per unit. This data, including energy usage and cost, is displayed on the connected LCD screen for local, real-time monitoring. A relay module enables integration with external devices for further control or automation, while a reset button allows users to clear the data after payment, starting a new billing cycle.

- For cloud communication, the system incorporates an ESP module, which handles TX and RX communication to transmit processed data to an IoT platform. Users can remotely access and analyze energy usage and cost data through the cloud, leveraging platforms such as the Arduino IoT Cloud or similar services. A user-friendly interface is available via IoT remote apps, allowing users to monitor consumption, costs, and reset data conveniently.

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


# TABLE OF COMPONENTS REQUIRED FOR THE PRODUCT

| Item    | Quantity |
|---------|-----|
|Single phase Energy meter 240v 50Hz     | 1  | 
|  4N35 Optocoupler   | 1  | 
|VSDSquadron mini| 1|
| ESP32 MODULE | 1  |  |
| 16*2 i2cLCD display | 1 | Display |
| Connecting wires | 1Set |
|2 CH relay5V -240V|1|
|5v-voltage regulator adaptor| 1|
| Zero PCB | 1|
|Switch | 1 |
| Case box | 1|

# PIN OUT TABLE  

|Component     	|    Pin/Connection	 |     Connected To|
|----------------|--------------------|-----------------|
|Energy Meter  	|Pulse Output	   |   Optocoupler (Input)|
|Optocoupler(4N35)|	Input	Energy Meter |Pulse Output|
|                 |Output	|VSDSquadron mini GPIO Input Pin (PD2)|
|                |                  |                   |	
|VSDSquadron mini|	GPIO Pin (PD2) 	|LM393 input|
|                |GPIO Pin TX (PD5)|	GPIO Pin RX (16)|
|                | GPIO Pin RX (PD6)|	GPIO Pin TX (17)|
|                |                   |                  |
|ESP32		       |                   |                  |
|                | RX (16)        	|VSDSquadron mini TX (PD5)|
|	        |TX (17)	|VSDSquadron mini RX (PD6)|
|               |              |                          |
|Relay module	|Signal pin	|VSDSquardron mini GPIO Pin PC3|
|               |Vcc	|3.3V/5V (depending on relay)   |
|               |	GND    |	GND            |
|	        |COM	|Power Line (Common)           |
|               |	NO (Normally Open)|	Load(Device Being Controlled)|
|               |	NC (Normally Closed)|	Optional (for fail-safe connections)|
|                |                          |                                       |	
|5 volt adaptaor | 	Phase	|Phase of the energy meter                 |
|                 |	Netural |	Netural of the energy meter         |
|             |	5V	  |VSDSquadron mini|  VCC                                    |
|              |	GND	|VSDSquadron mini | GND                    |                 
|LM393 Comparator |D0      |  VSDSquadron mini   GPIO PD6                |
|                 |5V       |VSDSquadron mini 5V|
|                 |         |VSDSquadron mini GND|
|I2C LCD |	SDA|	vsdsquadron mini GPIO (PC1)|
|            |SCA|	vsdsquadron mini GPIO (PC2)|


# BLOCK DIAGRAM OF THE SYSTEM 
![Blank diagram (1)](https://github.com/user-attachments/assets/c3e824d7-7cd9-4bdf-a4bd-6e9d4d6815ec)
---------------

# CIRCUIT DIAGRAM OF THE SYSTEM 
![circuit diagram dir-v](https://github.com/user-attachments/assets/63bc4150-8d0d-4ffa-bcf4-40deb65612b2)
----------------

# INTRODUCTION TO ARDUINO IOT CLOUD 

- The Arduino IoT Cloud is an integrated platform designed to facilitate the development and deployment of IoT projects. It enables seamless connectivity and management of devices, allowing users to control and monitor the project remotely. For this project, the Arduino IoT Cloud serves as the backbone, connecting the smart energy meter to the internet and enabling real-time data visualization and remote control.

- With the Arduino IoT Cloud, We can create and manage IoT devices through an easy-to-use interface. The platform supports a variety of Arduino boards, including the popular ESP32 and MKR series, which are well-suited for IoT applications. By leveraging the Arduino IoT Cloud, we can define properties such as energy consumption, cost, and relay states, which are updated and synchronized with the cloud. This allows us to monitor the energy consumption of our smart meter in real-time and make informed decisions based on the data collected.

- The cloud platform provides robust tools for data logging, visualization, and alerting. we can create dashboards to visualize energy consumption trends and costs over time, enabling better energy management and cost-saving strategies. Additionally, the platform supports integrations with third-party services, enhancing the functionality of IoT project.

- Security is a crucial aspect of IoT deployments, and the Arduino IoT Cloud ensures secure communication between your devices and the cloud through SSL/TLS encryption. This ensures that our data remains protected from unauthorized access and tampering.

- Overall, the Arduino IoT Cloud simplifies the development process, offering a reliable and scalable solution for IoT projects. By using the Arduino IoT Cloud, this smart energy meter project can provide real-time monitoring, remote control, and data analysis, enhancing energy management and enabling smarter decision-making.

#  USER DASHBOARD OF ARDUINO IOT CLOUD IN PC 
![Screenshot (145)](https://github.com/RAJASHEKHAR-KANUKUNTLA/PROJECT-SEM-15/assets/146096356/448d21a2-a2d9-43b7-8e12-694bdace533b)


# USER DASHBOARD OF ARDUINO IOT CLOUD IN   MOBILE

![WhatsApp Image 2024-07-10 at 13 03 21](https://github.com/RAJASHEKHAR-KANUKUNTLA/PROJECT-SEM-15/assets/146096356/ab2cfe90-cf67-4e91-8f97-14a23b1bfb78)



# SOURCE CODE OF VSDSQUARDRON MINI AN ESP32 
--------

# IMAGES OF THE PROJECT
----------

# DEMONSTRATION VIDEO OF THE PRODUCT Demonstration  
--------


# ABOUT 

# CONCLUSION  
The smart energy meter project effectively integrates hardware and software components to deliver a reliable and user-friendly solution for real-time energy monitoring and cost management. By utilizing the VSD Squadron Mini Board, optocoupler, LCD display, relay module, and ESP module, the system ensures precise energy consumption tracking, cost calculation, and seamless cloud-based data access.
Users benefit from real-time feedback displayed on the LCD screen, remote monitoring through IoT platforms, and easy interaction via IoT apps, making energy management more efficient and transparent. This versatile solution is adaptable for use in homes, EV charging stations, and industrial settings, offering scalable energy monitoring and control across various applications.
 
