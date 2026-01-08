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

---

## 🧩 Core Concepts
- **Producer** → The sender. Publishes messages (events).
- **Consumer** → The receiver. Subscribes to topics and reads messages.
- **Topic** → A mailbox/channel where messages are stored.
- **Broker** → A Kafka server that stores topics and messages.
- **Cluster** → A group of brokers working together.
- **Partition** → Splits a topic into smaller chunks for scalability.

👉 Example:  
An **online store**:
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
Download from [Apache Kafka](https://kafka.apache.org/downloads).  
Start ZooKeeper (if required) and Kafka broker:

```bash
# Start ZooKeeper (for older versions)
bin/zookeeper-server-start.sh config/zookeeper.properties

# Start Kafka broker
bin/kafka-server-start.sh config/server.properties
```

---

### 2. Create a Topic
```bash
bin/kafka-topics.sh --create --topic test-topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
```

---

### 3. Start a Producer
The **producer** is the sender of messages.  
Run the following command to start a producer and send messages to your topic:

```bash
bin/kafka-console-producer.sh --topic test-topic --bootstrap-server localhost:9092
```

Now type any message (e.g., `Hello Kafka!`) and press Enter.  
👉 Each line you type is sent into Kafka under the topic `test-topic`.

---

### 4. Start a Consumer
The **consumer** is the receiver of messages.  
Run the following command in a new terminal:

```bash
bin/kafka-console-consumer.sh --topic test-topic --from-beginning --bootstrap-server localhost:9092
```

You’ll see the messages you typed in the producer terminal appear here in real time.

---

### 5. Interactive Example
1. Open **two terminals**:
   - Terminal 1 → Run the **producer**.
   - Terminal 2 → Run the **consumer**.
2. In the producer terminal, type:
   ```
   Order #123 placed
   Payment received
   Inventory updated
   ```
3. In the consumer terminal, watch the messages appear instantly.

---

## 📚 Use Cases
- **Finance:** Real‑time payments and fraud detection.
- **Logistics:** Track shipments and vehicles live.
- **IoT:** Stream sensor data from devices.
- **Healthcare:** Monitor patients and predict treatments.
- **Retail:** React to customer actions instantly.

---

## 🤝 Contribution Guidelines
- Use **simple language** in notes and examples.
- Add **clear comments** in code snippets.
- Provide **step‑by‑step instructions** for new learners.
- Test your commands before submitting a PR.

---

## ⭐ Key Takeaway
Apache Kafka is like a **high‑speed data highway**.  
It helps applications **talk to each other in real time**, making it essential for modern systems.

---

## 📚 Resources
- [Apache Kafka Official Documentation](https://kafka.apache.org/documentation/)
- [Confluent Developer – Intro to Kafka](https://developer.confluent.io/what-is-apache-kafka/)
- [System Design Primer – Kafka Section](https://github.com/donnemartin/system-design-primer)
```
