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

