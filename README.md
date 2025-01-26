# POWERSN_IIITM_PRODUCT_DEVELOPMENT
TEAM K-TECH Sree Kanna 




# INTRODUCTION  
- The development of IoT-based smart energy meters marks a significant step forward in energy management technology. These devices utilize the Internet of Things (IoT) to enable real-time monitoring, precise data collection, and user-friendly interfaces, addressing key challenges faced by both consumers and power companies. They promote energy awareness and encourage responsible usage.

- Smart energy meters provide several benefits, including cost savings, operational efficiency, and environmental sustainability. By offering detailed insights into energy consumption patterns, they empower consumers to make informed decisions, reduce energy bills, and adopt sustainable practices. For power companies, they improve demand management, minimize energy losses, and enhance the reliability of power distribution.

- This project aims to develop a low-cost IoT-based smart energy meter to address these challenges. The proposed meter will enable real-time monitoring and accurate energy consumption tracking, ensuring both efficiency and affordability.


# OVER VIEW OF PROJECT  

- The IoT Smart Energy Meter project aims to deliver a low-cost, efficient solution for monitoring energy consumption by utilizing the VSD Squadron Mini Board with an LCD display and a relay module. This system measures real-time energy usage and presents the data on the LCD screen, ensuring immediate and local monitoring.

- To enable cloud-based communication, the project incorporates an ESP module, which facilitates TX and RX communication for transmitting data to an IoT platform. This integration allows users to remotely track and analyze energy consumption patterns, making the solution suitable for a wide range of applications, from smart homes to industrial settings.

- By combining the advanced features of the VSD Squadron Mini Board and IoT connectivity, the project aims to enhance energy

# OPERATAION OF THE SYSTEM  

- The smart energy meter solution combines hardware and software to monitor energy consumption and calculate costs in real time. The system begins with a traditional energy meter that generates pulses corresponding to the consumed energy. To ensure safety, these pulses are isolated from the microcontroller using an optocoupler with lm393 comparator.

 - The pulses are processed using the VSD Squadron Mini Board, which counts them to calculate energy usage. The board also computes the cost of consumed energy based on a predefined cost per unit. This data, including energy usage and cost, is displayed on the connected LCD screen for local, real-time monitoring. A relay module enables integration with external devices for further control or automation, while a reset button allows users to clear the data after payment, starting a new billing cycle.

- For cloud communication, the system incorporates an ESP module, which handles TX and RX communication to transmit processed data to an IoT platform. Users can remotely access and analyze energy usage and cost data through the cloud, leveraging platforms such as the Arduino IoT Cloud or similar services. A user-friendly interface is available via IoT remote apps, allowing users to monitor consumption, costs, and reset data conveniently.

 - The entire system is developed using the Arduino IDE, providing a robust environment for coding and deploying the firmware necessary for data processing, communication, and control. This integration of the VSD Squadron Mini Board with IoT capabilities offers a reliable, scalable, and user-friendly solution for efficient energy and cost management.

# Table of Components required for the prototype
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

# Pin Out table:

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


