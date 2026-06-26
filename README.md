## Repository Description

**Agro 5G – Smart Agriculture Monitoring and Crop Recommendation System using 5G, Edge AI, and MEC**

Agro 5G is an intelligent agriculture solution that integrates IoT sensors, 5G communication, Multi-access Edge Computing (MEC), and Machine Learning to provide real-time soil monitoring, crop prediction, and fertilizer recommendations. The system collects environmental and soil nutrient data using Arduino-based sensors, transmits the data through a Raspberry Pi 5G evaluation platform to an MEC server, and utilizes AI models to recommend suitable crops and fertilizers for optimized agricultural productivity.

---

# README.md

````markdown
# Agro 5G

## Overview

Agro 5G is a smart agriculture platform that combines IoT sensing, 5G connectivity, Edge AI, and Multi-access Edge Computing (MEC) to assist farmers in making data-driven decisions. The system continuously monitors soil and environmental conditions and uses machine learning models to predict the most suitable crop and fertilizer for a given field.

The solution demonstrates how next-generation communication technologies can improve agricultural productivity by enabling real-time monitoring and intelligent decision-making.

---

## Features

- Real-time soil nutrient monitoring
- Temperature and humidity sensing
- 5G-enabled data transmission
- Edge computing using MEC architecture
- AI-based crop recommendation
- AI-based fertilizer recommendation
- Live web dashboard visualization
- Low-latency agricultural analytics
- Scalable IoT architecture

---

## System Architecture

```text
+------------------+
| Soil Sensors     |
| NPK Sensor       |
| TDS Sensor       |
| DHT11 Sensor     |
+--------+---------+
         |
         v
+------------------+
| Arduino Uno      |
| Data Collection  |
+--------+---------+
         |
         v
+------------------+
| Raspberry Pi 5   |
| 5G Evaluation    |
| Platform         |
+--------+---------+
         |
         v
+------------------+
| MEC Server       |
| AI Processing    |
+--------+---------+
         |
         v
+------------------+
| Web Dashboard    |
| Visualization    |
+------------------+
````

---

## Hardware Components

### Microcontrollers and Processing Units

* Arduino Uno
* Raspberry Pi 5 (5G Evaluation Board)

### Sensors

* NPK Soil Nutrient Sensor (RS485)
* MAX485 RS485 Communication Module
* TDS Sensor Module
* DHT11 Temperature and Humidity Sensor

### Communication

* 5G SIM Connectivity
* UDP Data Transmission

---

## Software Stack

### Programming Languages

* Python
* C/C++

### Libraries and Frameworks

* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Streamlit
* Socket Programming

### Platforms

* Raspberry Pi OS
* Linux
* MEC Edge Server

---

## Machine Learning Models

The system utilizes XGBoost models trained on agricultural datasets for:

### Crop Prediction

Input Features:

* Temperature
* Nitrogen (N)
* Phosphorus (P)
* Potassium (K)

Output:

* Recommended Crop

### Fertilizer Prediction

Input Features:

* Temperature
* Nitrogen (N)
* Phosphorus (P)
* Potassium (K)

Output:

* Recommended Fertilizer

---

## Data Flow

1. Sensors collect soil nutrient and environmental data.
2. Arduino Uno acquires and preprocesses sensor readings.
3. Data is forwarded to the Raspberry Pi 5G platform.
4. Raspberry Pi transmits data to the MEC server through the 5G network.
5. MEC server processes the incoming data.
6. XGBoost models perform crop and fertilizer prediction.
7. Results are displayed on the web dashboard.
8. Farmers receive real-time recommendations.

---

## Project Structure

```text
Agro-5G/
│
├── arduino/
│   ├── sensor_reading.ino
│
├── raspberry_pi/
│   ├── sender.py
│
├── mec_server/
│   ├── receiver.py
│   ├── predictor.py
│   ├── xgb_crop_model.pkl
│   ├── xgb_fertilizer_model.pkl
│
├── dashboard/
│   ├── app.py
│
├── dataset/
│   ├── crop_fertilizer_dataset.csv
│
├── models/
│   ├── crop_label_encoder.pkl
│   ├── fertilizer_label_encoder.pkl
│
└── README.md
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/agro-5g.git
cd agro-5g
```

### Install Dependencies

```bash
pip install pandas numpy scikit-learn xgboost streamlit
```

---

## Running the Project

### Step 1: Start MEC Server

```bash
python receiver.py
```

### Step 2: Start Prediction Service

```bash
python predictor.py
```

### Step 3: Launch Dashboard

```bash
streamlit run app.py
```

### Step 4: Run Raspberry Pi Sender

```bash
python sender.py
```

---

## Example Input

```json
{
  "temperature": 28,
  "nitrogen": 62,
  "phosphorus": 85,
  "potassium": 212
}
```

### Example Output

```json
{
  "recommended_crop": "Rice",
  "recommended_fertilizer": "Urea"
}
```

---

## Applications

* Precision Agriculture
* Smart Farming
* Sustainable Agriculture
* Remote Soil Monitoring
* Edge AI in Agriculture
* 5G-enabled Agricultural Analytics

---

## Future Enhancements

* Integration of additional soil parameters
* Real-time irrigation recommendations
* Drone-assisted field monitoring
* Federated learning support
* Cloud and edge hybrid deployment
* Mobile application integration

---

## Technologies Used

* IoT
* 5G Communication
* Multi-access Edge Computing (MEC)
* Artificial Intelligence
* Machine Learning
* Edge Computing
* Smart Agriculture

---

## Contributors

Bharath Kumar S
B.Tech Electronics and Computer Engineering
SRM Institute of Science and Technology

---

## License

This project is intended for educational, research, and demonstration purposes.

```

This README is suitable for GitHub, internships, resume project links, and project demonstrations. It presents Agro 5G as a professional IoT + 5G + Edge AI project rather than just a sensor-monitoring system.
```
