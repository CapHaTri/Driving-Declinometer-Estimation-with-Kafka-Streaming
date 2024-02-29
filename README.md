# Driving Declinometer Estimation with Kafka Streaming
## Overview
- This project aims to implement a real-time driving declinometer estimation system using Kafka Streaming. A declinometer measures the tilt or inclination of a vehicle concerning the horizontal plane. Understanding the declination of a vehicle is crucial for various applications, including navigation, stability control, and safety systems.

## Architecture:
The system architecture consists of:
- Producer: Collects sensor data from the vehicle and publishes it to Kafka topics.
- Kafka: Acts as the central message broker for streaming data processing.
- Stream Processing: Kafka Streams API processes the incoming data streams to estimate the declination.
- Consumer: Consumes the processed data and presents it for visualization and further analysis.
## Usage:
- Start a Kafka Sever:
---
    bin\windows\kafka-server-start.bat config\server.properties
    bin\windows\kafka-server-start.bat config\server.properties
---
- Create new topic
---

bin\windows\kafka-topics.bat --create --topic Driving_Declinometer_test --bootstrap-server localhost:9092

---
- Run Producer.ipynb file to start sending messages
- Run Consumer.ipynb file to Receive Messages and Predict Output
## Requirements:
- Apache Kafka
- Kafka Streams API
- Vehicle sensor data sources
