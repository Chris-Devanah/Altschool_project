# Project Overview: 

A microservices-based architecture application is deployed on Kubernetes and there’s a need to create a clear IaaC (Infrastructure as Code) deployment to be able to deploy the services in a fast manner.
This project will be implemented using Terraform for infrastructure provisioning, Kubernetes for container orchestration, Helm for package management, and Prometheus for monitoring.

## PROJECT REQUIREMENTS:


Socks Shop Application

Terraform

AWS Account

Kubernetes

Helm

Prometheus


## The following tools and technologies will be used in the project:

### Terraform:
Terraform is an open-source infrastructure as a code software tool that provides a consistent CLI workflow to manage hundreds of cloud services. It codifies APIs into declarative configuration files, creating infrastructure as code using a high-level configuration language called HCL (HashiCorp Configuration Language).

### AWS Account:
An AWS account will be required to provision the necessary infrastructure resources, such as VPCs, subnets, security groups, and EKS cluster.

### Kubernetes:
Kubernetes is an open-source container orchestration platform that automates containerized applications' deployment, scaling, and management.

### Helm:
Helm is a package manager for Kubernetes, which provides an easy way to manage software built for Kubernetes.

### Prometheus:
Prometheus is an open-source monitoring and alerting toolkit designed for reliability and scalability. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts based on predetermined conditions.

### Socks Shop Application:
The Socks Shop application is a popular microservices-based e-commerce platform used for this project.


# GETTING STARTED

## Infrastructure Provisioning

1. Using Terraform, we will provision the necessary infrastructure resources on AWS, including VPCs, subnets, security groups, and EKS cluster. This will allow for a clear and reproducible infrastructure setup.
Make sure you have installed Terraform alongside AWS CLI on your local machine. If not, you can download it from the official website.

2. Create a new directory for the Terraform configuration files and navigate to it.

`` mkdir Socks-Shop_Terraform``

`` cd Socks-Shop_Terraform ``

3. Git clone this repository and navigate to the terraform folder to have the Terraform configuration files and initiate the Terraform project.

[ Altschool_project](https://github.com/Chris-Devanah/Altschool_project/tree/main)



