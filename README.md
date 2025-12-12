# maintenance-predective

Project Overview
This project implements a predictive maintenance system for electrical machines using IoT sensors
and Machine Learning.
The system collects real-time data from sensors, sends it over TCP/IP to a local server, analyzes it
with a trained ML model, and predicts maintenance needs to prevent machine failures.
Features- Real-time data collection from IoT sensors: Temperature, Current, Voltage/Tension, Rotation
speed- TCP/IP communication between IoT devices and local server- ML model trained on historical data to predict machine failures- Dashboard interface for monitoring status and predictions- Optional actuator control or alert triggers
Architecture
Sensors (Temp, Current, Voltage, Rotation)-> ESP8266 / ESP32 (WiFi) - TCP/IP Client-> Local Server (Python TCP/IP) - ML Processing-> Dashboard / Interface (Real-time Visualization)
Getting Started
Requirements- Python 3.12+- ESP8266 / ESP32 device- Python libraries: socket, pandas, scikit-learn, matplotlib- Arduino IDE or PlatformIO (for ESP device)
Installation

. Navigate to the project folder:
   cd predictive-maintenance
. Install Python dependencies:
   pip install -r requirements.txt
. Upload ESP client code to your ESP device.
. Run the server:
   python server.py
. Open the dashboard to monitor predictions in real time.
How It Works
1. Sensors continuously measure machine parameters.
2. ESP device sends the data via TCP/IP to the local server.
3. Server receives and parses the data.
4. ML model predicts potential failures or maintenance needs.
5. Dashboard visualizes the machine status, predictions, and alerts.
Dataset- Dataset used for training comes from Kaggle with 200 records.- Features include Temperature, Current, Voltage, and Rotation.- Located in /data folder.
Future Improvements- Integrate GSM/Email alerts for critical machine conditions- Historical data storage and trend analysis- Expand to multiple machines and IoT nodes- Enhance dashboard with live graphs and interactive charts
Authors
Nour Limem, Balkis, Hend
Mastere EEA2 - Embedded Systems & IoT
License
This project is licensed under the MIT License
