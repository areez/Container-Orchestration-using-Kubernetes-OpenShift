# Guestbook Application Deployment with Kubernetes and RedHat OpenShift

## Introduction

This repository demonstrates my expertise in Kubernetes and RedHat OpenShift by deploying a multi-tier Guestbook web application on IBM Cloud. The project showcases key features such as scaling, version management, and multi-tier architecture using Kubernetes for version 1 (v1) and OpenShift for version 2 (v2).

- **v1**: The Guestbook app is built, deployed, and managed using **Kubernetes** with features like **Horizontal Pod Autoscaling (HPA)**, **Rolling Updates**, and **Rollbacks**.
- **v2**: A multi-tier version is deployed using **RedHat OpenShift** with **ImageStreams**, Redis Master-Slave architecture, and inter-service dependency management.

---

## Objectives / Features

1. **Kubernetes Deployment (v1)**:
   - Build and deploy the Guestbook web app.
   - Implement Horizontal Pod Autoscaling (HPA) for dynamic scaling.
   - Perform Rolling Updates and Rollbacks to ensure seamless upgrades and recovery.
   
2. **RedHat OpenShift Deployment (v2)**:
   - Manage deployment using OpenShift ImageStreams for easy versioning.
   - Deploy a multi-tier architecture with Redis Master-Slave replication.
   - Resolve service dependencies in a multi-tier setup and manage scaling and updates.

---

## Why Kubernetes and OpenShift?

### **Kubernetes**
Kubernetes is a highly popular Container Orchestration tool that automates the deployment, scaling, and operation of application containers. It offers:
- **Scalability**: Automatically scales applications to handle increased traffic or workload.
- **Resilience**: Provides self-healing features like auto-restart of failed containers.
- **Rolling Updates and Rollbacks**: Ensures zero downtime during updates and quick recovery from failures.

### **OpenShift**
OpenShift builds on top of Kubernetes, which is an Enterprise-ready Container Orchestration Platform offering developer-friendly tools for easy app deployment, scaling, and management. Key features include:
- **ImageStreams**: Manage and track image versions for applications.
- **Enterprise Security**: Enhanced security features ideal for production environments.
- **Built-in CI/CD Pipelines**: Simplifies the integration and deployment of applications.

---

## Deployment Overview

### **Version 1: Kubernetes Deployment**

#### Step 1: Create the Dockerfile
Create a `Dockerfile` to define the app's environment and build process. This involves pulling the necessary base images, copying app files, and setting up commands to run the app.

#### Step 2: Define the Deployment YAML
Use a `deployment.yaml` file to define the number of replicas, container image, and configuration for deploying the app in Kubernetes.

#### Step 3: Build and Push the Image to IBM Cloud
After defining the Dockerfile, build the container image and push it to the IBM Cloud Container Registry for deployment.

#### Step 4: Deploy and Scale the Application
Apply the `deployment.yaml` to Kubernetes, which deploys the app and ensures it is running. Set up **Horizontal Pod Autoscaling (HPA)** to handle traffic spikes.

#### Step 5: Rolling Updates and Rollbacks
Perform rolling updates by updating the image tag in the deployment configuration. If the update fails, easily roll back to the previous working version.

---

### **Version 2: OpenShift Deployment**

#### Step 1: Tag the Image and Use OpenShift ImageStreams
Leverage OpenShift’s **ImageStreams** to track and manage different image versions. Tag the latest image and create an OpenShift deployment for the Guestbook app.

#### Step 2: Set Up Redis Master-Slave Architecture
Configure the multi-tier version of the app by setting up Redis as the data storage layer with master and slave nodes. This involves creating separate deployments for the Redis master and slaves.

#### Step 3: Manage Service Dependencies
In the multi-tier setup, Redis services need to be created before deploying the Guestbook app to ensure proper communication between components.

#### Step 4: Deploy and Test Scaling
Deploy the updated Guestbook app in OpenShift, ensuring that Redis services are properly connected. Implement horizontal scaling and monitor the app for performance and resilience.

#### Step 5: Perform Rolling Updates and Test Rollbacks
As with Kubernetes, OpenShift also allows you to perform rolling updates with zero downtime. Test the deployment by scaling, updating, and rolling back changes as necessary.

---

## Conclusion

This project highlights how Kubernetes and OpenShift can be used effectively to manage both simple and complex application deployments. By leveraging key features like Horizontal Pod Autoscaling, Rolling Updates, ImageStreams, and multi-tier architectures, it demonstrates how containerized applications can be deployed and scaled efficiently across cloud environments.
