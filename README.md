🚀 JupyterHub Deployment on Kubernetes Cluster with Docker, Rook Ceph, and Kubeflow
Kubernetes
Docker
JupyterHub
Ceph
Kubeflow

This project demonstrates the deployment of JupyterHub on a Kubernetes cluster integrated with Docker, Rook Ceph for persistent storage, and Kubeflow for machine learning workflows. The infrastructure is designed to be scalable, highly available, and secure, making it ideal for collaborative data science and research environments.

📋 Table of Contents
Project Overview

Technologies Used

Infrastructure Setup

Installation Steps

Deployment Process

Troubleshooting

Conclusion & Future Work

🌟 Project Overview
The goal of this project is to deploy JupyterHub on a Kubernetes cluster to provide an interactive and collaborative computing environment for users. Key features include:

Scalability and high availability.

Persistent storage using Rook Ceph.

Integration with Kubeflow for machine learning workflows.

Secure networking and resource management.

🛠 Technologies Used
Technology	Description
Docker	Containerization platform for packaging applications and dependencies.
Kubernetes	Orchestration system for managing containerized applications.
Rook Ceph	Storage orchestrator providing distributed, resilient, and scalable storage.
Kubeflow	Open-source platform for ML workflows on Kubernetes.
JupyterHub	Multi-user service for Jupyter notebooks, enabling collaboration.
🖥 Infrastructure Setup
Virtual Machines Configuration
Master Node:

Role: Controls the Kubernetes cluster.

Specs: 4 vCPU, 16GB RAM, 200GB Storage (Ubuntu 20.04 LTS).

Worker Nodes (2x):

Role: Execute workloads assigned by the master.

Specs: 4 vCPU, 8GB RAM, 150GB Storage (Ubuntu 20.04 LTS).

Network Configuration
Private VPN for secure communication.

IP Addresses:

Master: 192.168.244.156

Worker 1: 192.168.244.157

Worker 2: 192.168.244.158

Firewall rules to restrict access to essential ports (e.g., 6443 for Kubernetes API).

Storage Partitions
Master:

/: 50GB (OS and applications).

/var/lib/docker: 50GB (Docker storage).

/var/lib/kubelet: 100GB (Kubernetes storage).

Workers:

/: 50GB (OS and applications).

/var/lib/docker: 50GB (Docker storage).

/var/lib/kubelet: 50GB (Kubernetes storage).
