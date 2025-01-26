# POWERSN_IIITM_PRODUCT_DEVELOPMENT
TEAM K-TECH Sree Kanna 




# INTRODUCTION  
- The development of IoT-based smart energy meters marks a significant step forward in energy management technology. These devices utilize the Internet of Things (IoT) to enable real-time monitoring, precise data collection, and user-friendly interfaces, addressing key challenges faced by both consumers and power companies. They promote energy awareness and encourage responsible usage.

- Smart energy meters provide several benefits, including cost savings, operational efficiency, and environmental sustainability. By offering detailed insights into energy consumption patterns, they empower consumers to make informed decisions, reduce energy bills, and adopt sustainable practices. For power companies, they improve demand management, minimize energy losses, and enhance the reliability of power distribution.

- This project aims to develop a low-cost IoT-based smart energy meter to address these challenges. The proposed meter will enable real-time monitoring and accurate energy consumption tracking, ensuring both efficiency and affordability.


# OVER VIEW OF PROJECT  

- The IoT Smart Energy Meter project aims to deliver a low-cost, efficient solution for monitoring energy consumption by utilizing the VSD Squadron Mini Board with an LCD display and a relay module. This system measures real-time energy usage and presents the data on the LCD screen, ensuring immediate and local monitoring.

- To enable cloud-based communication, the project incorporates an ESP module, which facilitates TX and RX communication for transmitting data to an IoT platform. This integration allows users to remotely track and analyze energy consumption patterns, making the solution suitable for a wide range of applications, from smart homes to industrial settings.

- By combining the advanced features of the VSD Squadron Mini Board and IoT connectivity, the project aims to enhance ene


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
|	5V	  |VSDSquadron mini|  VCC                                    |
|	GND	|VSDSquadron mini | GND                    |                 
|LM393 Comparator |D0      |  VSDSquadron mini   GPIO PD6                |
|                 |5V       |VSDSquadron mini 5V|
|                 |         |VSDSquadron mini GND|


