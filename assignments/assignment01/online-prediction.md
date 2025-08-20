# Online Prediction

<!-- Online Prection ทำงานอย่างไร  -->
Online Prediction คือการทำนายผลแบบ เรียลไทม์ โดยเมื่อมีข้อมูลใหม่เข้ามา (เช่น จาก Kafka หรือ MQTT) โมเดล ML จะประมวลผลและส่งผลลัพธ์ออกทันที ต่างจาก Batch ML ที่ต้องรอรวบรวมข้อมูลก่อนแล้วค่อยทำนายทีหลัง

## ปิดการใช้งานของ Batch ML ดังนี้

1. Iot-class-2025-kafka-to-jsonl
2. Iot-class-2025-predict-then-influxdb
3. Iot-class-2025-train-from-data


## เริ่มใช้งาน Online ML ดังนี้

1. Iot-class-2025-server
2. Iot-class-2025-mqtt-bridge-kafka
3. Iot-class-2025-data-to-influxdb

## ผลที่ได้จากการใช้ ML มีดังนี้

![alt text](image.png)
<!-- แนบรูป Grafana  พร้อมอธิบาย -->
ได้ผลการทำนาย (prediction) แบบ real-time
สามารถแสดงผลบน Grafana Dashboard
ข้อมูลจะอัปเดตต่อเนื่องทุกครั้งที่มี sensor data ใหม่