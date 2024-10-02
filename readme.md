# DevOps Stack Deployment with Kubernetes

This README provides instructions on how to deploy and manage a DevOps stack using Kubernetes. The stack includes Jenkins, SonarQube, TestLink, Prometheus, and OWASP ZAP.

## Prerequisites

- Ensure you have Docker Desktop installed with Kubernetes enabled.
- Have `kubectl` command-line tool installed and configured to communicate with your Kubernetes cluster.

## File Structure

```plaintext
devops/
│
├── devops-master.yaml                # Master file to deploy all services
│
├── jenkins/
│   ├── jenkins-deployment.yaml       # Deployment configuration for Jenkins
│   ├── jenkins-service.yaml           # Service configuration for Jenkins
│   └── jenkins-pvc.yaml               # Persistent Volume Claim for Jenkins
│
├── sonarqube/
│   ├── sonarqube-deployment.yaml     # Deployment configuration for SonarQube
│   ├── sonarqube-service.yaml         # Service configuration for SonarQube
│   ├── sonarqube-pvc.yaml             # Persistent Volume Claim for SonarQube
│   └── sonarqube-extensions-pvc.yaml  # Extensions PVC for SonarQube
│
├── testlink/
│   ├── testlink-deployment.yaml       # Deployment configuration for TestLink
│   ├── testlink-service.yaml          # Service configuration for TestLink
│   └── testlink-pvc.yaml              # Persistent Volume Claim for TestLink
│
├── prometheus/
│   ├── prometheus-deployment.yaml     # Deployment configuration for Prometheus
│   ├── prometheus-service.yaml        # Service configuration for Prometheus
│   └── prometheus-pvc.yaml            # Persistent Volume Claim for Prometheus
│
└── owasp-zap/
    ├── owasp-zap-deployment.yaml      # Deployment configuration for OWASP ZAP
    └── owasp-zap-service.yaml         # Service configuration for OWASP ZAP
