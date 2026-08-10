# Kubernetes Expense Tracker Monitoring

A production-style DevOps project demonstrating the deployment, scaling, monitoring and alerting of a Java Spring Boot Expense Tracker application on a K3s Kubernetes cluster.

The application is containerized using Docker, deployed on Kubernetes with MySQL as the backend database, and monitored using Prometheus, Grafana, Node Exporter and kube-state-metrics.

Spring Boot Actuator with Micrometer exposes application and JVM metrics which are scraped by Prometheus and visualized through Grafana dashboards.

---

## 📌 Project Overview

This project combines two major DevOps areas:

### Phase 1 — Kubernetes Deployment

- Kubernetes cluster using K3s
- Namespace isolation
- ConfigMap
- Kubernetes Secrets
- MySQL Deployment
- PersistentVolumeClaim
- MySQL ClusterIP Service
- Spring Boot Expense Tracker Deployment
- Resource requests and limits
- Liveness Probe
- Readiness Probe
- NodePort Service
- Pod scaling
- Rolling Updates
- Rollbacks
- Horizontal Pod Autoscaler
- Ingress with Traefik

### Phase 2 — Monitoring & Observability

- Prometheus
- Node Exporter
- kube-state-metrics
- Grafana
- Spring Boot Actuator
- Micrometer Prometheus Registry
- Application metrics
- JVM metrics
- CPU monitoring
- Memory monitoring
- Pod monitoring
- Kubernetes node monitoring
- Grafana dashboards
- Grafana Alerting
- Email notification

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

# Grafana — Application & JVM Monitoring
![Grafana JVM Dashboard](docs/10-grafana-dashboard.png)


# Grafana — Kubernetes Infrastructure Monitoring
![Grafana Kubernetes Dashboard](docs/11-grafana-dashboard.png)
---

# 🔥 Prometheus

Prometheus collects metrics from the Spring Boot application and Kubernetes monitoring components.

![Prometheus Targets](docs/12-Prometheus-Targets.png)
Spring Boot exposes application metrics through:

```text
/actuator/prometheus

---

# 👨‍💻 Author

**Rakesh Sharma**

DevOps / Cloud Engineer
