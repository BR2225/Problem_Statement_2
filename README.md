# Problem_Statement_2
# Title: Kubernetes Security Scan

**Background/Task:**  
Install local K8s cluster (such as Minikube, K3s, Kind, etc) and use a tool such as Kubescape (or any other tool) to scan for findings and send the list of the findings.

## Deliverables:
A JSON file containing the k8s findings.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## ⚙️ What is Minikube?

**Minikube** is a lightweight tool that runs a single-node Kubernetes cluster locally on your machine. It's ideal for:

- Learning Kubernetes
- Testing locally before deploying to production
- Running CI/CD pipelines with Kubernetes clusters

In this project, we used:

- Minikube v1.33.1
- Kubescape v3.0.34
- Docker driver
  
![Screenshot 2025-06-22 100542](https://github.com/user-attachments/assets/fed96a2a-f0c5-4289-a60b-fdabac1640c0)

### ✅ Minikube Cluster Setup

```powershell
minikube start
kubectl get nodes
```
## 🧰 What is Kubescape?

[Kubescape](https://kubescape.io/) is an open-source Kubernetes security platform that scans Kubernetes clusters, YAML manifests, and Helm charts to ensure compliance and security best practices.

### ✅ Key Features:
- Security compliance checks
- Misconfiguration detection
- RBAC analysis
- CI/CD integration
- JSON/HTML report generation
- Integrates with tools like Prometheus, Grafana, Slack

---

## 🎯 Purpose

Kubescape helps DevOps, security teams, and developers:
- Detect misconfigurations and security risks in Kubernetes clusters
- Align with security frameworks (NSA, MITRE, etc.)
- Generate audit/compliance reports
- Enforce policies across CI/CD workflows

---

## 🧪 Supported Security Frameworks

Kubescape supports multiple scanning frameworks:

| Framework     | Description                                                           |
|---------------|-----------------------------------------------------------------------|
| **NSA**       | Based on the NSA-CISA Kubernetes Hardening Guidance                  |
| **MITRE ATT&CK** | Maps Kubernetes risks to known attacker techniques                 |
| **CIS**       | Benchmarks from the Center for Internet Security                     |
| **DevOps Best Practices** | Non-compliance with general Kubernetes deployment best practices |
| **ARMO Best** | A comprehensive, ARMO-recommended security control set               |

---

## 🚀 Project Workflow

### 🔧 1. Start Minikube Cluster

```powershell
minikube start

```
![Screenshot 2025-06-22 100606](https://github.com/user-attachments/assets/bc725f7f-1d69-4c7c-9adc-aa8f8955061e)

## 2. Install Kubescape

```powershell
iwr -useb https://raw.githubusercontent.com/kubescape/kubescape/master/install.ps1 | iex
```
## 3. Verify installation:
```
kubescape version
```
## 4. Run a Security Scan:
```
kubescape scan framework nsa --format json --output results.json
```
### This command:

Uses the NSA framework

Scans the entire Minikube cluster

Outputs results to results.json




