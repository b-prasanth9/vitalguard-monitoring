# VitalGuard — Vitals-Driven Monitoring System

A Spring Boot prototype for recording patient vital signs, applying transparent rule-based thresholds, persisting readings in MySQL, and displaying alert history.

## Stack
Java 17 · Spring Boot · Spring Data JPA · MySQL · HTML/CSS/JavaScript · Maven

## Architecture
Vitals source/simulator → Spring Boot REST API → Rule Engine → Risk/Alert → MySQL → Dashboard

The current version deliberately uses a transparent rule engine. It does not pretend that a medical ML model has been trained. A future Python service can consume the vitals payload and return a model-generated risk score.

## APIs
- POST `/api/vitals`
- GET `/api/vitals`
- GET `/api/vitals/alerts`

## Run
1. Use MySQL and update credentials in `src/main/resources/application.properties`.
2. Run `mvn spring-boot:run`.
3. Open `http://localhost:8081`.

This is a software prototype, not a medical diagnostic system; the thresholds are demo values.