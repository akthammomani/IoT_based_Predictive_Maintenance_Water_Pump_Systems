# **IoT-Based Predictive Maintenance of Water Pump Systems**
![Image](https://github.com/user-attachments/assets/6a565c67-db69-456e-baf7-efa9d27d2901)

This project is a part of the Data Analytics and Internet of Things (AAI-530) course in the Applied Artificial Intelligence Master Program at the University of San Diego (USD).

-- Project Status: COMPLETED

## **Introduction**

Water pump systems play a crucial role in industrial and municipal operations, but unexpected failures can lead to costly downtime and maintenance expenses. Predictive maintenance leverages sensor data and machine learning to detect issues early, allowing for proactive interventions.
This project focuses on predicting machine failures in water pump systems using a combination of time-series forecasting and classification models. We start by cleaning and preprocessing raw IoT sensor data to extract meaningful features. Then, we build two models:
•	LSTM for time-series prediction: Forecasts machine status changes, identifying when a pump might shift from normal to abnormal. 
•	Random Forest for failure cause classification: Diagnoses the likely reason for failure based on sensors patterns.

## **Predictive Maintenace IoT System**

The IoT-based predictive maintenance system for water pump systems integrates multiple sensors to monitor key operational parameters. 

These sensors provide real-time data to machine learning models, enabling early detection of failures and reducing unexpected downtime. The dataset used for this project, Pump Sensor Data, is publicly available on [Kaggle](https://www.kaggle.com/datasets/nphantawee/pump-sensor-data/data) This dataset consists of IoT sensor readings collected from water pump systems, helping identify anomalies and predict potential failures before they cause operational disruptions.

•	Vibration Sensors are mounted on the motor casing and pump casing. The motor casing vibration sensor has a mean value of 2.37g, a measurement range of 0 to 2.55g, and a standard deviation of 0.4g. The pump casing vibration sensor has a mean of 2.3g, ranging from 0 to 4.87g, with a standard deviation of 0.77g. Regular calibration is necessary to maintain accuracy and prevent data drift. Regular calibration is necessary to maintain accuracy and prevent data drift.
•	Temperature Sensors are installed on the pump lubrication oil supply and motor components. The pump lube oil supply temperature sensor operates within a range of 19.27°C to 547.92°C, with a mean of 36.61°C and a standard deviation of 15.61°C. These sensors are heat-resistant and shielded to prevent external thermal interference.
•	Pressure Sensors are located at the pump discharge line, measuring pressure fluctuations to detect performance degradation. The pump discharge pressure sensor has a range of 27.78 PSI to 1000 PSI, with a mean of 202.7 PSI and a standard deviation of 105.7 PSI. Periodic cleaning is required to prevent sensor fouling and ensure accurate readings.
•	Electrical Sensors are positioned on the motor power supply and phase lines, monitoring critical electrical parameters. The motor phase current sensor has a range of 0 to 45A, with a mean of 29.14A and a standard deviation of 10.11A. The motor phase voltage sensor operates in a range of 0 to 600V, with a mean of 421.13V and a standard deviation of 129.1V. These sensors help monitor electrical load variations and prevent overloading.
•	Speed Sensors are attached to the motor shaft and impeller to track rotational speeds. The motor speed sensor operates in a range of 2.8 to 800 RPM, with a mean of 590.67 RPM and a standard deviation of 144 RPM. The pump stage 1 impeller speed sensor has a similar range of 2.8 to 878.92 RPM, with a mean of 590.84 RPM and a standard deviation of 199.3 RPM. These sensors use optical or magnetic encoders for precise measurement.
The combination of these sensors enables continuous monitoring, allowing the system to detect anomalies and predict potential failures. This design ensures optimal pump performance while minimizing operational disruptions.

**IoT Gateway**: The IoT Gateway acts as the central hub between the sensors and the data processing stages. It collects data from the sensors, aggregates it, and performs basic preprocessing to reduce network load. The gateway also ensures compatibility between sensor communication protocols and cloud systems. A key limitation is that it can become a bottleneck if overloaded and relies on stable power and network connectivity. Additionally, it requires rugged housing to operate effectively in harsh refinery conditions, such as exposure to heat, dust, and humidity.
•	Connectivity Type: Zigbee (from sensors), Ethernet/Wi-Fi (to cloud)
•	Messaging Protocol: MQTT (lightweight, efficient protocol for IoT communication.       

## **Methods and Technologies Utilized**

The project incorporates the following methods & Technologies:

* Data Wrangling & Preprocessing  
  * **Library Used:** `pandas`  
  * **Steps:** Cleaning, handling missing values, feature selection, and encoding categorical variables for machine learning models.  

* Time-Series Prediction  
  * **Model Used:** `Long Short-Term Memory (LSTM)`  
  * **Purpose:** Predict machine status transitions (normal vs. abnormal) based on historical sensor readings.  

* Multi-Class Classification  
  * **Model Used:** `Random Forest Classifier`  
  * **Purpose:** Classify failure causes into multiple categories (rotational, vibration, electrical issues, etc.).  

* Data Visualization  
  * **Libraries Used:** `seaborn` and `matplotlib`  
  * **Purpose:** Visualizing sensor trends, feature importance, and model performance.  

* Interactive Dashboard  
  * **Tool Used:** `Tableau Public`  linke found [here](https://public.tableau.com/views/IoT-BasedPredictiveMaintenanceofWaterPumpSystems/IoT-BasedPredictiveMaintenanceofWaterPumpSystem?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
)
  * **Purpose:** Presenting machine status predictions and failure cause insights in an interactive, easy-to-understand format.  

## **Results** 
  * **LSTM Model:** Achieved high accuracy in predicting machine status over time.  
  * **Random Forest Model:** Delivered strong classification performance with an accuracy of **99.87%**.  
  * **Tableau Dashboard:** Provided an intuitive way to analyze sensor data and failure trends.

## **Contributing**
Contributions are welcome for future improvements after the initial development phase.

## **License**
This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.

## **Acknowledgement**
A special thanks to **Professor Kahila Mokhtari, Ph.D.**, for his invaluable guidance and support throughout this class/project.



