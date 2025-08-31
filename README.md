# 🚀 Auto-Healing Kubernetes Cluster for MERN website with Cost Optimization on AWS
## Project Overview:

 This project demonstrates a production-grade Kubernetes setup on AWS with auto-healing and cost optimization.
 A MERN stack web application is containerized and deployed on AWS EKS. It uses Terraform, Jenkins, SonarQube, Docker, Argocd, Prometheus-Grafana, and AWS Autoscaling to create a cluster that scales dynamically based on workload while minimizing costs. 

## ⚙️ Tech Stack

AWS (EKS, EC2, VPC, IAM, ASG)

Terraform (Infrastructure as Code)

Kubernetes (Cluster, Deployments, HPA, Cluster Autoscaler)

Docker (Containerization)

SonarQube (code Quality Testing)

Jenkins (CI/CD automation)

ArgoCD (GitOps Tool)

Prometheus & Grafana (Monitoring & Alerting)

## 🛠 Features

 Auto-Healing: Failed pods automatically rescheduled, nodes replaced if unhealthy.

 Horizontal Pod Autoscaler (HPA): Scales pods based on CPU/memory usage.

 Cluster Autoscaler (CA): Dynamically provisions/removes worker nodes.

 Cost Optimization: Removes unused nodes to save AWS costs.

 CI/CD Pipeline: Jenkins pipeline deploys the app on every GitHub commit.

 Monitoring & Alerting: Prometheus for metrics, Grafana for visualization.

## 🚀 How It Works

Provision Infrastructure using Terraform (terraform apply).

Deploy Application using Kubernetes manifests.

Enable HPA & CA → pods scale first, then nodes are provisioned if required.

Jenkins CI/CD automatically builds & deploys on new commits.

Monitor Metrics in Grafana, set up alerts from Prometheus.

## Architecture Diagram:
<img width="1536" height="1024" alt="ChatGPT Image Aug 31, 2025, 06_42_48 AM" src="https://github.com/user-attachments/assets/49ae9312-7c15-46e8-9517-3cc5195bd1f4" />


## 📊 Demo Workflow

Deploy initial app → 1 pod running.

Increase load → HPA creates new pods.

If pods exceed node capacity → Cluster Autoscaler provisions new EC2 node.

When load decreases → extra pods and unused nodes are removed to save cost.


# Mern-Ecommerce-website 

<img width = "800" src="https://i.imgur.com/a7YFo86.png"/>  

<img width="800"  alt="Screenshot 2025-08-30 220032" src="https://github.com/user-attachments/assets/7c1737a6-1b82-4a54-8157-e0c0b951ddb5" />


