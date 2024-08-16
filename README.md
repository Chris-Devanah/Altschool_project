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

```
mkdir Socks-Shop

cd Socks-Shop

```


3. Git clone this repository and navigate to the terraform folder to have the Terraform configuration files and initiate the Terraform project.

[ Altschool_project](https://github.com/Chris-Devanah/Altschool_project/tree/main)

4. Run the following command to initialize the Terraform project:

```
terraform init
```

5. Run the following command to create an execution plan:

```
terraform plan
```

6. Run the following command to apply the changes:

```
terraform apply --auto-approve
```

--auto-approve can be added to avoid the confirmation prompt

EKS provisioned by terraform.

![2024-08-14-18-21-37](https://github.com/user-attachments/assets/305c4675-68f4-47b4-afc6-256540d74ef2)

![2024-08-14-18-22-11](https://github.com/user-attachments/assets/49d58cd3-df8c-4ecb-a662-5b806bad5e2e)

![2024-08-14-18-25-07](https://github.com/user-attachments/assets/9c24ba58-896d-403d-ad99-988461692849)

![2024-08-14-18-44-25](https://github.com/user-attachments/assets/70e1fb58-c55a-44d0-945a-e57ed89a035f)

![terra init](https://github.com/user-attachments/assets/52e3b819-779d-4216-b889-68aa914fdb6d)

7. Configure the kubectl to connect to the EKS cluster, specify the region and the cluster name.

```
aws eks update-kubeconfig --name Sock_Shop-eks --region us-east-1
```

![2024-08-14-19-00-20](https://github.com/user-attachments/assets/a9e6e351-04b2-4145-9366-be30ef13be72)

8. Apply the deployment manifests in the **kube** folder to our cluster using the following command:

```
  kubectl apply -f kubernetes/deployment.yaml
```
![2024-08-14-19-09-06](https://github.com/user-attachments/assets/a4e86037-bd24-45b3-9ebf-6fcba412afdd)

In the command console of your AWS ensure that the nodes are up and running 

![2024-08-14-19-48-28](https://github.com/user-attachments/assets/663d9804-f11b-49ff-8474-7865d943a34a)

9. Install Ingress and deploy it using the following commands:

```
helm install ingress ingress/ingress-nginx
```
![2024-08-14-19-49-54](https://github.com/user-attachments/assets/17dc803c-b549-4293-9d0d-d921b5dd7583)

Ensure that the load balancer is up and running.

![2024-08-14-19-47-50](https://github.com/user-attachments/assets/fa72c700-c411-4b98-8fe2-300214ef05ec)

10. COnfigure route 53 to deploy the application via front-end, this would be done on the AWS management console.

![route 53 setup 1](https://github.com/user-attachments/assets/911479c8-e766-4313-a0cb-aa7287e4caff)

![53 setup 4](https://github.com/user-attachments/assets/882235ab-0fdc-4297-818c-fd3764fb626a)

After setup, wait a couple of hours depending on your provider for the Domain Name servers to propagate properly and display your application.

![2024-08-15-10-13-11](https://github.com/user-attachments/assets/0d953cda-e19e-4f3c-bce4-ddbca985a1df)

![2024-08-15-10-15-21](https://github.com/user-attachments/assets/879d102f-49c3-46d0-97db-971bf3ad452b)





