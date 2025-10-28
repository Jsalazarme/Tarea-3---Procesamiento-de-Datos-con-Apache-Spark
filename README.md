# 🌡️ Análisis de Sensores en Tiempo Real con Apache Kafka y Apache Spark Streaming

## 📘 Descripción del Proyecto
Este proyecto implementa una arquitectura de **procesamiento de datos en tiempo real** utilizando **Apache Kafka** como sistema de mensajería y **Apache Spark Structured Streaming** como motor de análisis.

Se simulan lecturas de sensores (temperatura y humedad) que son enviadas continuamente a Kafka, procesadas por Spark, y agregadas en ventanas de tiempo de **1 minuto** para calcular promedios por cada sensor.

---

## 🎯 Objetivo
Desarrollar un sistema que permita **procesar, analizar y visualizar flujos de datos en tiempo real**, demostrando el uso de herramientas Big Data (Kafka + Spark) para análisis de IoT (Internet of Things).

---

## 🧩 Arquitectura General

```mermaid
flowchart LR
  A[Sensores simulados<br>(Python Producer)] -->|JSON| B[(Kafka Topic: sensor_data)]
  B --> C[Spark Structured Streaming<br>(Consumidor)]
  C --> D[(Consola / Almacenamiento)]
