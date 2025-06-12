
# Real-Time Sensor Anomaly Detection

**Freelance Project — Anonymous Industrial Client (Manufacturing Sector)**

## Project Overview

This project was developed as part of a freelance engagement for an anonymous industrial client in the manufacturing sector.  
The client required a prototype real-time streaming pipeline to monitor IoT sensor data from factory equipment and automatically detect anomalies to prevent equipment failures.

## Tech Stack

- **Apache Kafka** → Real-time data streaming
- **Python** → Data producer, ML model, consumer
- **Machine Learning** → Isolation Forest for anomaly detection
- **InfluxDB** → Time-series database
- **Grafana** → Real-time visualization dashboards
- **Docker Compose** → Easy deployment of entire stack

## Architecture

```
Sensor Data → Kafka Producer → Kafka Topic (sensor_readings)
                             ↓
              Kafka Consumer → ML Model → Normal / Anomaly
                             ↓
       Kafka Topic (anomaly_alerts) + InfluxDB → Grafana Dashboard
```

## Sensor Data Simulated

- **Temperature** (°C)
- **Vibration** (Hz)
- **Pressure** (Pa)
- **Current Draw** (Amps)

## Features

✅ Real-time sensor data simulation  
✅ ML-based anomaly detection  
✅ Kafka-based scalable streaming architecture  
✅ Visual dashboards for operators  

## Usage

### 1️⃣ Start the stack

```bash
docker-compose up
```

### 2️⃣ Run Kafka producer

```bash
python producer.py
```

### 3️⃣ Run Kafka consumer with ML model

```bash
python consumer.py
```

### 4️⃣ Open Grafana

- URL: [http://localhost:3000](http://localhost:3000)
- Default login: **admin / admin**

## Results

The system detects anomalies in real time and visualizes both sensor trends and anomaly events in Grafana dashboards.

---

**Author:** Nima (Freelance Data Engineer / Data Scientist)  
**Project type:** Professional / Freelance Client Delivery
