# Monitoring Stack (Docker + Prometheus + Grafana)

This project is a full monitoring system deployed on an AWS EC2 Ubuntu instance using Docker Compose.

It demonstrates how to monitor application performance, system metrics, and visualize data using Grafana dashboards.

---

## Architecture

* Nginx (Web Server)
* Pay API (Test Application)
* Prometheus (Metrics Collection)
* Node Exporter (System Metrics)
* Grafana (Visualization)

---

## Tech Stack

* Docker
* Docker Compose
* Prometheus
* Grafana
* Node Exporter
* Nginx
* AWS EC2 (Ubuntu)

---

## Deployment Steps

### 1. Clone project to EC2

```bash
scp -i key.pem -r monitoring-stack ubuntu@54.82.18.197:~/
```
