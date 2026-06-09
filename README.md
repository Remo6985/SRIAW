# 🛒 Smart Retail IoT Architecture (Whitepaper)

**Status:** Completed \
**Domain:** Internet of Things (IoT), Cloud Architecture, Retail Tech  

### 📝 Project Overview
This repository contains the architectural whitepaper and system design specifications for a **Smart Retail IoT Framework**. The project conceptualizes a scalable, four-layer IoT infrastructure designed to provide real-time, SKU-level inventory visibility and automate the checkout process using RFID technology and AWS cloud services.

The primary objective of this design is to balance high-throughput sensor telemetry with power efficiency, bridging the physical retail environment with enterprise ERP systems through an event-driven cloud pipeline.

---

### 🏗️ Architecture Design

![Architecture Diagram](images/Group%2038.png)

The system is engineered across four distinct layers:

* **1. Perception Layer (Edge):** Utilizes RFID sensors and smart shelf readers for continuous, real-time demand sensing and inventory tracking at the SKU level.
* **2. Network Layer (Hybrid Topology):** Implements a hybrid communication model. It uses **Zigbee** for low-power, lightweight sensor node transmission, and **Wi-Fi** for high-bandwidth data aggregation, optimizing the overall power footprint of the store's IoT grid.
* **3. Telemetry & Processing Layer (Cloud):** Leverages **AWS IoT Core** for secure, scalable device connectivity. High-volume continuous RFID data streams are ingested and buffered using **Amazon Kinesis** to ensure low-latency processing without data loss.
* **4. Application Layer (Integration):** An event-driven backend utilizing **AWS Lambda** translates physical sensor events into business logic, updating enterprise ERP databases in real time.

---

### 🚀 Key Features & Innovations

* **Automated "Smart Checkout":** A conceptualized physical infrastructure that allows simultaneous, multi-item scanning via clustered RFID readers. 
* **Event-Driven ERP Integration:** Eliminates batch-processing delays by using AWS Lambda to trigger instantaneous database updates the moment an item crosses the checkout threshold.
* **Power-Optimized Sensor Grid:** The strategic split between Zigbee and Wi-Fi ensures that battery-operated edge sensors maintain long lifecycles while still providing high-fidelity data to the cloud.

---

### 🛠️ Technology Stack

**Hardware & Networking**
* **RFID:** Passive tags and smart shelf reader nodes.
* **Zigbee (IEEE 802.15.4):** Low-power mesh networking for edge sensors.
* **Wi-Fi (IEEE 802.11):** High-bandwidth backhaul for data aggregators.

**Cloud & Infrastructure (AWS)**
* **AWS IoT Core:** Device registry, secure MQTT communication, and rule routing.
* **Amazon Kinesis:** High-throughput data stream ingestion.
* **AWS Lambda:** Serverless compute for event-driven ERP integration.

---

### 📄 Documentation
*For a deep dive into the network topologies, payload structures, and cloud routing rules, please read the full whitepaper included in this repository:*

* [Smart Retail IoT Architecture Whitepaper](https://drive.google.com/file/d/1gsBb6DQltiXzVeiX3Eon9e_TJsfYbITO/view?usp=sharing)
