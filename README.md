# Final-year-Project
Status: Ongoing

# Ambulance Green Corridor System Using GPS And Traffic Signal Control

## Project Overview

The **Ambulance Green Corridor System** is an IoT-based smart traffic management project designed to provide priority passage for ambulances during emergencies.

The system uses GPS technology to track an ambulance's location, ESP32 microcontrollers for processing and communication, and Firebase for real-time data exchange. By calculating the distance between the ambulance and a traffic signal, the system can automatically control a traffic signal prototype to provide a green signal when the ambulance approaches.

A web dashboard is also used to monitor location information and traffic signal status.

The main goal is to reduce delays at traffic intersections and support faster emergency medical transportation.

## Objectives

* Track ambulance location using GPS.
* Transmit location data in real time.
* Use ESP32 for communication and traffic signal control.
* Calculate the distance between the ambulance and a traffic signal.
* Automatically change traffic signals based on the ambulance's proximity.
* Monitor ambulance location and signal status through a web dashboard.
* Explore a cost-effective solution for emergency traffic management.

## Technologies Used

* **ESP32** — Microcontroller for processing and communication.
* **NEO-6M GPS Module** — Obtaining ambulance location coordinates.
* **Arduino IDE** — Programming the ESP32.
* **Embedded C/C++** — Microcontroller programming.
* **Firebase** — Real-time data storage and communication.
* **HTML, CSS, and JavaScript** — Web dashboard, if used in the implementation.
* **Red, Yellow, and Green LEDs** — Traffic signal prototype.

## System Architecture

The system consists of three main components:

### 1. Ambulance Unit

The GPS module obtains the ambulance's latitude and longitude. The ESP32 connects to Wi-Fi and uploads the location data to Firebase.

### 2. Traffic Signal Unit

A second ESP32 retrieves the ambulance's location data and calculates the distance between the ambulance and the traffic signal.

### 3. Web Dashboard

The dashboard retrieves data from Firebase and displays the ambulance's location information and traffic signal status.

##  Working Methodology

1. The ESP32 connects to Wi-Fi.
2. The GPS module obtains the ambulance's latitude and longitude.
3. The ambulance's coordinates are uploaded to Firebase.
4. The traffic signal ESP32 retrieves the coordinates.
5. The system calculates the distance between the ambulance and the traffic signal using the Haversine formula.
6. When the ambulance is within the configured distance threshold of 50 metres, the prototype signal turns green.
7. When the ambulance moves beyond the threshold, the signal returns to red.
8. The system continuously monitors the ambulance's location and updates the signal status.
9. The web dashboard displays the available location and signal information.

## Distance Calculation

The system uses the **Haversine formula** to calculate the straight-line distance between two geographical coordinates.

The formula accounts for the Earth's curvature and returns the distance in metres.

The calculated distance is used to determine whether the ambulance is within the configured signal activation threshold.

### Signal Control Logic

* **Distance ≤ 50 metres:** Activate the green signal.
* **Distance > 50 metres:** Activate the red signal.

The distance is checked repeatedly so that the signal can respond as the ambulance approaches or moves away.

## Testing and Results

The following functions are included in the project's testing and results:

* **Wi-Fi Connection:** ESP32 successfully connected to Wi-Fi.
* **GPS Tracking:** GPS coordinates received.
* **Firebase Communication:** Ambulance location uploaded successfully.
* **Distance Calculation:** Distance calculated between the ambulance and traffic signal.
* **Signal Activation:** Green signal activated when the ambulance approached within 50 metres.
* **Signal Reset:** Red signal activated when the ambulance moved beyond the threshold.
* **Dashboard Monitoring:** Location and signal status displayed on the web dashboard.
* **Continuous Monitoring:** Ambulance location and signal status updated continuously.

## Key Features

* GPS-based ambulance tracking.
* Real-time data exchange through Firebase.
* ESP32-based traffic signal control.
* Distance-based signal activation.
* Automatic signal state updates.
* Web dashboard for monitoring.
* Low-cost hardware prototype.

## Advantages

* Helps demonstrate how ambulance delays at traffic signals can be reduced.
* Provides automated traffic signal priority in a prototype environment.
* Supports real-time monitoring of ambulance location.
* Combines embedded systems, IoT, GPS, and cloud technology.
* Offers a foundation for future smart-city traffic management solutions.

## Future Scope

* Coordination of multiple traffic signals along an ambulance's route.
* Authentication of emergency vehicles.
* AI-based traffic detection.
* Dynamic route optimization.
* Integration with real-world traffic management infrastructure.

## Project Information

* **Project Title:** Ambulance Green Corridor System Using GPS And Traffic Signal Control
* **Project Type:** Final-Year Engineering Project
* **Department:** Information Science and Engineering
* **Institution:** Cambridge Institute of Technology, Bengaluru
* **Domain:** Internet of Things (IoT), Embedded Systems, and Smart Traffic Management
* **Programming Language:** Embedded C/C++
* **Microcontroller:** ESP32
* **Cloud Platform:** Firebase

## 🚧 Project Status

**Project Review and Development**

This project demonstrates GPS-based ambulance tracking and distance-based traffic signal control using ESP32 and Firebase.

## References

1. P. Prem Swaroop, P. Sree Gopal, and U. Vijay Teja, *Development of a Machine Learning-Based Model for an Intelligent Ambulance Detection System Using CNN*, IEEE Access, 2025.
2. *Enhancing Traffic Management with YOLOv5-Based Ambulance Tracking System*, IEEE Access, 2023.
3. R. Sundar, S. Hebbar, and V. Golla, *Implementing Intelligent Traffic Control System for Congestion Control, Ambulance Clearance, and Stolen Vehicle Detection*, IEEE Sensors Journal, 2015.
4. T. Sarapirom and S. Poochaya, *Detection and Classification of Incoming Ambulance Vehicle Using Artificial Intelligence Technology*, ECTI-CON, 2021.

---
 **This project explores how GPS, IoT, and automated traffic signal control can support faster ambulance movement during emergencies.**
