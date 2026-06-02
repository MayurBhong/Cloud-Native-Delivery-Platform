# Cloud Native Delivery Platform ☁️

### End-to-End CI/CD Automation for Java Applications on AWS EKS

Cloud Native Delivery Platform (CNDP) is an end to end DevOps solution that automates the build, containerization, and deployment of Java applications on AWS using GitHub, Jenkins, Docker, Kubernetes, and Amazon EKS.

---

## Overview 📖

Cloud Native Delivery Platform is a production-ready DevOps project that automates the complete software delivery lifecycle for Java applications. The platform integrates GitHub, Jenkins, Docker, Kubernetes, and Amazon EKS to enable continuous integration, automated containerization, and seamless deployment on AWS cloud infrastructure.

The project demonstrates modern DevOps practices by creating a fully automated CI/CD pipeline that builds, packages, deploys, and manages applications with minimal manual intervention. It focuses on scalability, reliability, automation, and cloud-native application delivery.

---

## Key Features 🚀

* Automated CI/CD pipeline using Jenkins
* Source code management with GitHub
* Java application build automation using Maven
* Docker containerization
* Container image management with Docker Hub / Amazon ECR
* Kubernetes deployment automation
* Amazon EKS cluster integration
* Automated application updates through SCM polling
* Secure AWS infrastructure using IAM and VPC
* Scalable cloud-native deployment architecture

---

## Motivation 🎯

* Manual deployments are time-consuming and error-prone
* Modern applications require continuous delivery and scalability
* Managing infrastructure and deployments manually reduces productivity
* Organizations need faster and more reliable release cycles

Cloud Native Delivery Platform solves these challenges by:

* Automating the software delivery process
* Reducing deployment errors
* Improving release speed and consistency
* Enabling scalable Kubernetes-based deployments
* Following industry-standard DevOps practices

---

## Architecture 🏗️

Developer → GitHub → Jenkins → Maven → Docker → Container Registry → Amazon EKS → Kubernetes Pods → End Users

<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/55b1a9ab-f290-4683-8ca4-38ce12214700" />

---

## Technologies Used 🛠️

### DevOps Tools

* GitHub
* Jenkins
* Maven
* Docker
* Kubernetes

### AWS Services

* Amazon EC2
* Amazon EKS
* AWS IAM
* AWS VPC
* Public & Private Subnets
* Internet Gateway
* Route Tables

### Container Registry

* Docker Hub
* Amazon ECR

---

## CI/CD Workflow ⚙️

1. Developer pushes code to GitHub
2. Jenkins detects source code changes
3. Maven builds the Java application
4. Docker creates the application image
5. Image is pushed to Docker Hub or Amazon ECR
6. Jenkins deploys the application to Amazon EKS
7. Kubernetes creates and manages Pods
8. Application becomes available to end users

---

## Project Implementation Steps 📌

### Step 1: Create AWS IAM User

* Create a dedicated IAM user
* Enable Programmatic and Console Access
* Assign required permissions
* Configure AWS CLI

### Step 2: Create Custom VPC

* Create a VPC
* Create Public and Private Subnets
* Configure Internet Gateway
* Configure Route Tables

### Step 3: Launch EC2 Instance for Jenkins

* Launch EC2 instance in Public Subnet
* Configure Security Groups
* Connect using SSH
* Install Jenkins and required tools

### Step 4: Install and Configure Jenkins

* Start Jenkins service
* Create admin account
* Access Jenkins dashboard
* Install required plugins

### Step 5: Create IAM Roles for EKS

* Create EKS Cluster Role
* Create EKS Node Group Role
* Attach required AWS policies
* Configure role permissions

### Step 6: Create Amazon EKS Cluster

* Create EKS Cluster
* Select custom VPC
* Configure networking
* Attach cluster role

### Step 7: Create EKS Node Group

* Create Managed Node Group
* Select Node IAM Role
* Configure scaling settings
* Launch worker nodes

### Step 8: Connect Environment to EKS

* Configure kubectl access
* Update kubeconfig
* Verify cluster connectivity
* Validate worker nodes

### Step 9: Create GitHub Repository

* Create public repository
* Upload Java application source code
* Add Kubernetes manifests
* Organize project files

### Step 10: Configure GitHub Credentials in Jenkins

* Generate Personal Access Token
* Add credentials in Jenkins
* Configure repository access
* Test GitHub integration

### Step 11: Create Docker Image

* Create Dockerfile
* Build Docker image
* Validate image creation
* Prepare image for deployment

### Step 12: Configure Container Registry

* Login to Docker Hub
* Tag Docker image
* Push image to registry
* Verify image availability

### Step 13: Create Kubernetes Deployment Files

* Create deployment.yaml
* Create service.yaml
* Define Deployments and Pods
* Configure Services

### Step 14: Create Jenkins Pipeline

* Clone Repository
* Build Application
* Create Docker Image
* Push Image to Docker Hub
* Deploy to Amazon EKS

### Step 15: Deploy Application to EKS

* Deploy application using Kubernetes manifests
* Create Pods and Services in Amazon EKS
* Verify deployment status and running Pods
* Access application through the exposed Service

### Step 16: Enable Continuous Deployment

* Configure Poll SCM in Jenkins
* Monitor GitHub repository changes
* Automatically trigger Jenkins pipeline
* Deploy latest version to Amazon EKS

---

## Real Time Use Case 🏢

A software company manages a Java-based e-commerce application where multiple developers continuously add new features, fix bugs, and release updates.

Using the Cloud Native Delivery Platform, every code change pushed to GitHub automatically triggers the CI/CD pipeline. Jenkins builds the application, creates a Docker image, pushes it to Docker Hub, and deploys the latest version to Amazon EKS.

This automation eliminates manual deployment tasks, accelerates software releases, and ensures that users always have access to the latest version of the application with minimal downtime.

---

## Common Challenges ⚠️

* Incorrect IAM permissions causing access denied errors
* EKS cluster connectivity and authentication issues
* Docker image push failures to Docker Hub
* Jenkins pipeline build and deployment failures
* Kubernetes Pods stuck in Pending or CrashLoopBackOff state
* Service misconfiguration preventing application access
* Resource limitations on EKS worker nodes

---
## Learning Outcomes 📚

* CI/CD Pipeline Implementation
* Docker Containerization
* Kubernetes Administration
* Amazon EKS Deployment
* AWS Infrastructure Management
* Cloud-Native Application Delivery
* DevOps Automation Best Practices

---

## Project Summary 📌

Cloud Native Delivery Platform is an end-to-end DevOps project that automates the build, containerization, and deployment of Java applications on AWS. The platform integrates GitHub, Jenkins, Docker, Kubernetes, and Amazon EKS to create a fully automated CI/CD pipeline.

The project demonstrates modern DevOps practices by automating code integration, application builds, Docker image creation, image management, and Kubernetes deployments. It utilizes AWS services such as IAM, VPC, EC2, and EKS to provide a secure, scalable, and reliable cloud environment.

This implementation enables continuous application delivery with minimal manual intervention while improving deployment consistency, scalability, and availability. It provides hands-on experience in DevOps automation, container orchestration, Kubernetes, and AWS cloud infrastructure.

