# Kubernetes Expense Tracker Monitoring

## 📌 Project Overview

This project demonstrates the deployment and monitoring of a Java Spring Boot Expense Tracker application on a K3s Kubernetes cluster.

The application is containerized using Docker and deployed on Kubernetes with MySQL as the backend database.

The project implements Kubernetes deployment, persistent storage, health monitoring, scaling, rolling updates, rollback, Prometheus monitoring, Grafana dashboards and alerting.

---

## 🏗️ Architecture

![Project Architecture](docs/01-Architecture-image.png)

---

## 🛠️ Technology Stack

- Java
- Spring Boot
- MySQL
- Docker
- Kubernetes
- K3s
- Kubernetes ConfigMap
- Kubernetes Secrets
- PersistentVolumeClaim
- NodePort
- Traefik Ingress
- Prometheus
- Micrometer
- Node Exporter
- kube-state-metrics
- Grafana
- Grafana Alerting

---

# 🚀 Application

The Expense Tracker is a Java Spring Boot web application that allows users to manage their expenses.

### Home Page

![Home Page](docs/02-home-page.png)

### Login

![Login Page](docs/03-login.png)

### Expense Added

![Expense Added](docs/04-expense-added.png)

---

# ☸️ Kubernetes Deployment

The Spring Boot application and MySQL database are deployed on a K3s Kubernetes cluster.

The deployment includes:

- Kubernetes Namespace
- ConfigMap
- Secret
- MySQL Deployment
- MySQL Service
- PersistentVolumeClaim
- Expense Tracker Deployment
- Expense Tracker Service
- Resource Requests and Limits
- Liveness Probe
- Readiness Probe
- NodePort Service
- Traefik Ingress
- Horizontal Pod Autoscaler
- Rolling Updates
- Rollback

### Kubernetes Pods

![Kubernetes Pods](docs/05-Pods-image.png.jpeg)

### Kubernetes Deployment

![Kubernetes Deployment](docs/06-deployment.png.jpeg)

---

# 🔍 Deployment Quality Check

The application deployment and Kubernetes configuration were verified using Kubernetes commands and application health checks.

![Deployment Quality Check](docs/07-quality-check.png.jpeg)

---

# 📊 Monitoring

A complete Kubernetes monitoring stack was implemented.

## Monitoring Components

- Prometheus
- Grafana
- Node Exporter
- kube-state-metrics
- Spring Boot Actuator
- Micrometer

The monitoring architecture collects application, JVM, pod and Kubernetes node metrics.

### Kubernetes Deployment and Monitoring Status

![Kubernetes Monitoring Status](docs/08-kubernetes-deployment-and-monitoring-status.png.jpeg)

---

# 🚨 Grafana Alerting

Grafana Alerting is configured to monitor the availability of the Expense Tracker application.

The alert uses the Prometheus `up` metric to detect whether the application is available.

![Grafana Alerting](docs/09-grafana-alerting.png)

---

# 📈 Grafana Dashboard

Grafana is connected to Prometheus and is used to visualize application and Kubernetes metrics.

The dashboard includes monitoring for:

- JVM CPU Usage
- JVM Memory Usage
- HTTP Request Rate
- Application Uptime
- Running Pods
- Application Availability
- Kubernetes Node CPU
- Kubernetes Node Memory

![Grafana Dashboard](docs/10-grafana-dashboard.png)

### Additional Grafana Dashboard

![Grafana Monitoring Dashboard](docs/11-grafana-dashboard.png)

---

# 🔥 Prometheus

Prometheus collects metrics from the Spring Boot application and Kubernetes monitoring components.

Spring Boot exposes application metrics through:

```text
/actuator/prometheus
