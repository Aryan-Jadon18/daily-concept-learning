Apache kafka was created by linkedin and donated to Apache foundation. It is used for even streaming. Event streaming here means variety of application.
Event -> Event created data -> data is collected -> sent to be processed -> data is analyzed -> analysis leads to biz decisions.

What is event streaming used for?
- to process payments and financial transactions in real time, such as in stock exchanges, banks and insurances.
- to track and monitor shipments, vehicles in real time, such as in logistics and  automotive industry.
- to continously capture and analyze sensor data from IoT devices or other equipment, such as in factories and wind parks.
- to collect and immediately react to customer data such as in retail, hotels etc..
- To monitor patients in hospital and predict possible treatments for timely recovery.
- to connect, store data from a company's different divisions.
- to serve as foundation for data platforms, event driven architectures and microservices.

Key -> To publish(write) and subscribe(read) to streams of events, including continous import/export of your data from other systems. -> store streams relaibly as long and you want -/. to process streams of events as they occur or retrosprectively.

# 📡 Apache Kafka – Simple Guide

## 📖 Introduction
Apache Kafka is a **distributed event streaming platform**.  
Think of it like a **post office for data**:
- Applications can **send messages** (like letters).
- Other applications can **receive those messages**.
- Kafka makes sure the messages are delivered **quickly, reliably, and in order**.

Kafka was originally built at **LinkedIn** and later open‑sourced. Today, it’s widely used for **real‑time data pipelines** and **event‑driven applications**.

---

## 🧩 Core Concepts (Explained Simply)
- **Producer** → The sender. It publishes messages (events) into Kafka.
- **Consumer** → The receiver. It subscribes to topics and reads messages.
- **Topic** → A mailbox or channel where messages are stored.
- **Broker** → A Kafka server that stores topics and messages.
- **Cluster** → A group of brokers working together.
- **Partition** → Splits a topic into smaller chunks for scalability.

👉 Example:  
Imagine an **online store**:
- Producer: Checkout system sends “Order Placed” events.
- Topic: `orders`
- Consumer: Inventory system listens to `orders` and updates stock.

---

## ⚡ Why Use Kafka?
- **Real‑time processing** → Handle millions of events per second.
- **Scalability** → Add more brokers to handle more data.
- **Durability** → Messages are stored safely until consumed.
- **Flexibility** → Works for payments, IoT sensors, logs, analytics, and more.

---

## 🚀 How to Use Kafka (Step by Step)

### 1. Install Kafka
- Download from [Apache Kafka](https://kafka.apache.org/downloads).
- Extract and start **ZooKeeper** (for older versions) and **Kafka server**:
  ```bash
  # Start ZooKeeper (if required)
  bin/zookeeper-server-start.sh config/zookeeper.properties

  # Start Kafka broker
  bin/kafka-server-start.sh config/server.properties
