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


## WEEK 10 EXPLANATION
In Kubernetes, a Secret is used to store sensitive information like usernames and passwords securely.

Instead of writing credentials directly inside configuration files, Kubernetes stores them in a Secret object.

In this setup, the MongoDB container does not read the Secret as a file. Instead, the values inside the Secret are passed to the container as environment variables.

For example:

MONGO_INITDB_ROOT_USERNAME
MONGO_INITDB_ROOT_PASSWORD

These variables are used by MongoDB when the container starts to create the initial admin user.

The line:

valueFrom:
  secretKeyRef:

tells Kubernetes to:

look for a Secret named mongodb-secret
get a specific value (like username or password)
inject it into the container as an environment variable

This way:

sensitive data is not exposed in plain text inside YAML files
credentials are managed securely
applications can still access them when needed
