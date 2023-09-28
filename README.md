# eks-configuration

# Flux Repository for Trivy Operator, Cert-Manager, and Podinfo

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/ArmannGr/eks-configuration/Flux%20Sync%20Workflow)
![GitHub](https://img.shields.io/github/license/ArmannGr/eks-configuration)

This Flux repository is designed to automate the deployment of the Trivy Operator, Cert-Manager, and Podinfo in your Kubernetes cluster. Flux is used to manage the GitOps workflow for continuous delivery and automation of these applications.

## Components Included

### 1. Trivy Operator

![Trivy Logo](https://aquasecurity.github.io/trivy/images/trivy.png)

**Description:** The Trivy Operator is a critical security tool that enhances the security of your Kubernetes workloads by scanning container images for vulnerabilities. It leverages the open-source Trivy scanner to identify security issues in your container images, including Common Vulnerabilities and Exposures (CVEs) and other potential threats. The operator simplifies the process of integrating image scanning into your Kubernetes environment, allowing you to maintain a high level of security without a lot of manual effort.

**Key Features:**

- **Image Scanning**: Trivy Operator automatically scans container images for known vulnerabilities and reports findings.
- **Policy Enforcement**: Define and enforce security policies to ensure images meet your organization's standards.
- **Integration**: Seamlessly integrates with your CI/CD pipeline and Kubernetes cluster to scan images at various stages of deployment.
- **Notifications**: Receive alerts and notifications about vulnerabilities via your preferred communication channels.

### 2. Cert-Manager

![Cert-Manager Logo](https://cert-manager.io/img/logo.svg)

**Description:** Cert-Manager is a Kubernetes native solution for managing SSL/TLS certificates. It simplifies the management of certificates, making it easy to secure your applications. Cert-Manager automates the certificate request and renewal process, ensuring that your services are always protected with up-to-date certificates.

**Key Features:**

- **Automated Certificate Management**: Automatically provisions, renews, and manages SSL/TLS certificates for your services.
- **Integration with Let's Encrypt**: Easily request and renew free certificates from Let's Encrypt.
- **Custom Certificate Resources**: Define certificate requirements using custom resources, simplifying certificate management in your applications.
- **Webhook Support**: Extend Cert-Manager's capabilities through custom webhooks and third-party certificate authorities.

### 3. Podinfo

![Podinfo Logo](https://github.com/stefanprodan/podinfo/raw/master/artwork/podinfo.png)

**Description:** Podinfo is a straightforward, Golang-based web application designed for Kubernetes environments. It serves as a useful example of an application that can be deployed and managed using Kubernetes and GitOps methodologies. Podinfo provides basic information about the Kubernetes pod it runs in, making it an ideal tool for learning and testing purposes.

**Key Features:**

- **Information Display**: Displays details about the Kubernetes pod, including environment variables, namespaces, and more.
- **Health Checks**: Demonstrates Kubernetes readiness and liveness probes for your applications.
- **Customization**: Easily customize and extend the application to suit your needs.

## Prerequisites

Before getting started, make sure you have the following prerequisites:

- [Flux CLI](https://fluxcd.io/docs/installation/) installed locally.
- A Kubernetes cluster properly configured.
- A Git repository where you will store your Flux repository.

## Getting Started

1. **Clone the Flux Repository**:

   ```shell
   git clone <your-flux-repo-url>
   cd <your-flux-repo>
