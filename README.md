# Kubernetes Monitoring with Prometheus & Grafana

This project demonstrates how to deploy Prometheus and Grafana to a local Kubernetes cluster (e.g., Minikube) to monitor pod metrics.

## Tools Used

- Kubernetes (Minikube)
- Prometheus
- Grafana
- Node Exporter
- Kube State Metrics (optional)

## Project Structure

```
k8s-monitoring-prometheus-grafana/
├── manifests/
│   ├── prometheus-config.yaml
│   ├── prometheus-deployment.yaml
│   ├── grafana-deployment.yaml
│   └── grafana-service.yaml
```

##  Setup Instructions

### 1. Start Minikube

```bash
minikube start
```

### 2. Deploy Prometheus

```bash
kubectl apply -f manifests/prometheus-config.yaml
kubectl apply -f manifests/prometheus-deployment.yaml
```

### 3. Deploy Grafana

```bash
kubectl apply -f manifests/grafana-deployment.yaml
kubectl apply -f manifests/grafana-service.yaml
```

### 4. Access Grafana

```bash
minikube service grafana-service
```

Login credentials:
- **user**: `admin`
- **pass**: `admin`

Add Prometheus as a data source: `http://prometheus:9090`

---
