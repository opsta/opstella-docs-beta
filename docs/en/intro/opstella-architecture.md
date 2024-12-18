---
outline: deep
---

## Opstella Architecture

### <ins><strong>Opstella Components</strong></ins>

![Opstella Architecture!](/images/intro/what-is-opstella/opstella-architecture.svg){data-zoomable}

1.   <strong> UI:</strong> A frontend service, users will access through the Opstella portal on this component.
2.   <strong>Core:</strong> A backend service centralizing information and communication between Opstella’s components.
3.   <strong>Clear Session:</strong> A utility component that clears the user's browser cache upon Single Sign-On (SSO) authentication process.
4.   <strong>Workers:</strong> A set of components that execute tasks to automate all integration components.
5.   <strong>PostgreSQL for Opstella:</strong> A relational database management system (RDBMS) for Opstella Core.
6.   <strong>Redis:</strong> An in-memory data store utilized as a cache for the Opstella Core component.
7.   <strong>Dapr:</strong> A distributed application runtime that orchestrates between each Opstella component.
8.   <strong>RabbitMQ:</strong> A message broker system that enables asynchronous communication to each Opstella component.
9.   <strong>Keycloak:</strong> An identity and access management that provides authentication, authorization, and user management for Opstella.
10.  <strong>PostgreSQL for Keycloak:</strong> A relational database management system (RDBMS) for Keycloak.

### <ins><strong>Supported Integration Components</strong></ins>

#### <strong>DevOps Tools</strong>

1. <strong>GitLab:</strong> A source code version control and CI/CD.
2. <strong>ArgoCD:</strong> A declarative, GitOps continuous delivery tool for Kubernetes applications.
3. <strong>Harbor:</strong> A cloud-native container registry that secures and manages container images.
4. <strong>Headlamp:</strong> A user-friendly web-based GUI for managing Kubernetes clusters.

#### <strong>DevSecOps Tools</strong>

1. <strong>HashiCorp Vault:</strong> Securely manages secrets, credentials, and access to sensitive data.
2. <strong>SonarQube:</strong> Analyzes code quality and security to detect bugs, vulnerabilities, and code smells.
3. <strong>Trivy:</strong> A security vulnerability scanner for container images and file systems. It is designed to identify and assess vulnerabilities in software dependencies, configurations, and operating system packages.
4. <strong>Zed Attack Proxy (ZAP):</strong> A web application security scanner that finds vulnerabilities in web applications.
5. <strong>DefectDojo:</strong> A tool to centralize and manage application security vulnerabilities.

#### <strong> Observability Tools</strong>

1. <strong>Grafana Dashboard:</strong> An interface visually presents real-time metrics, logs, and traces from various data sources.
2. <strong>Grafana Mimir:</strong> A highly scalable and performant backend solution for metrics data.
3. <strong>Grafana Loki:</strong> A log aggregation system that stores and queries logs efficiently.
4. <strong>Grafana Tempo:</strong> A distributed tracing backend for analyzing application performance and dependencies.
5. <strong>Grafana Alloy: </strong>A metrics, logs, and traces push-based collector and exporter

#### <strong> Kubernetes Cluster</strong>

Opstella will manage and deploy applications to the integrated Kubernetes workload cluster. Users can define deploy environments when creating a service with the following

1. <strong>DEV</strong> or <strong>develop</strong> is a development environment for developers
2. <strong>SIT</strong> is a system integration test environment for tester
3. <strong>UAT</strong> is a user acceptance test environment for QA, testers, or beta users
4. <strong>PRE</strong> or <strong>pre-production</strong> is a pre-production environment for compatibility testing before going live
5. <strong>PRD</strong> or <strong>production</strong> is the production environment for going live.

### <ins><strong>Opstella Application Hierarchy</strong></ins>

![Opstella Architecture!](/images/intro/what-is-opstella/application-hierarchy.svg){data-zoomable}

#### Organization 

This is the top layer of the application hierarchy. This is usually your company name. The organization is mandatory and can not change when it is first installed and when the Opstella instance is initialized. You can only have one organization.

#### Platform
This layer under the organization is responsible for integrating with each DevSecOps tool. This can be defined as

<ul style="list-style-type: square;">
            <li>Each of your private or public <strong>clouds.</strong> For example, VMware, AWS, GCP, and Azure.</li>
            <li>Each of your <strong>platforms.</strong> For example, OnPremise and Hybrid consist of VMware for non-production and AWS for workload production.</li>
            <li>Each of your <strong>departments</strong> or business units. For example, Internal, Marketing, and E-Commerce.</li>
            <li>Each of your <strong>projects.</strong> For example, CallCenter, CMS, Support, and Registration.</li>
        </ul>
                
#### Service 
This is the layer under the platform. This can be defined as your applications, projects, or services. The service will determine the <strong>environments</strong>, such as dev and prd, in which you want to deploy microservices or underlying components.

#### Component 
This is the bottom line layer where you deploy the containers. This can be called microservices or batch process. Opstella will create URL endpoints on each environment as defined in the service.