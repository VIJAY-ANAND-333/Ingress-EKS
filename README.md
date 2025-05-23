# EKS Deployment with Ingress

This project demonstrates how to deploy a containerized application on Amazon EKS (Elastic Kubernetes Service) and expose it externally using Kubernetes Ingress. It includes provisioning EKS infrastructure, deploying workloads, and configuring an ingress controller to manage external access to internal services.

## Features

- Provisioning of EKS cluster using Terraform
- Deployment of a sample Kubernetes application
- Installation and configuration of AWS Alb Ingress Controller
- Ingress resource configuration for routing HTTP(S) traffic
- Optional TLS setup using AWS ACM
- Optional DNS management with Route 53

## Tools and Technologies

- AWS EKS
- Kubernetes
- AWS Alb Ingress Controller
- kubectl
- Terraform
- Docker
- AWS Route 53 and ACM (optional)

## Setup and Usage

1. **Provision EKS Cluster**
   - Use Terraform or AWS CLI to create the EKS cluster.
   - Configure your local machine to connect to the cluster using `aws eks update-kubeconfig`.

2. **Deploy Application**
   - Apply Kubernetes manifests or use Helm charts to deploy your application and associated services.

3. **Install Ingress Controller**
   - Deploy AWS ALB Ingress Controller via Helm.
   - Confirm the creation of a LoadBalancer type service.

4. **Configure Ingress Resource**
   - Define an Ingress resource to route traffic to your application's services.
   - Set up TLS using ACM certificates if required.

5. **Access the Application**
   - Use the DNS name or public IP of the ingress controller to access the application from a browser.

## Prerequisites

- AWS account with appropriate IAM permissions
- AWS CLI configured locally
- kubectl installed and configured
- Helm installed
- Terraform installed (if using infrastructure as code)
- Optional domain name for DNS and TLS configuration

## Goals

- Deploy containerized applications on AWS EKS
- Set up and manage Kubernetes Ingress
- Build a reusable and extensible EKS deployment framework