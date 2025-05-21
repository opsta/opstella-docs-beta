---
outline: deep
---

# Root Admin (default user: 'Opstella')

**Role Description**

The highest role in the Opstella system. This is the role of the Opstella user, created with the company. Only the Opstella user has this role and access to all permissions in the system.

**Permission on DevOpsTool**

Because Admin (Opstella) is the highest role in the Opstella system, it can use all DevOpstool.

## GitLab

### Manage Repository

* Access and manage all repositories
* Edit repository settings
* Create, edit, and delete branches
* Control and manage tags
* Manage webhooks

### Merge Requests

* Create, edit, and delete merge requests
* Review and accept merge requests
* Use squash and merge options

### Issues

* Create, edit, and delete issues
* Manage issue boards
* Define, edit, and delete labels
* Manage milestones and epics

### CI/CD

* Manage pipelines and jobs
* Edit, delete, and trigger pipelines
* View logs of jobs

### Permissions

* Invite new members to the project
* Change roles of members with lower permissions

### Protected Branches and Tags

* Manage protected branches and protected tags
* Define who can push, merge, and tag in branches and tags that are protected

### Wiki and Snippets

* Create, edit, and delete wiki pages
* Manage project snippets

## Sonarqube

### Browse

* View the project and all related information (e.g., metrics, dashboards, and analysis results)
* View code analysis results but cannot make any edits

### See Source Code

* View source code analyzed by SonarQube
* Use to see context of issues and security hotspots that SonarQube detects in source code

### Administer Issues

* Manage detected issues (e.g., change status, add comments, assign responsibility, and set priority)
* Customize rules and profiles related to issue analysis

### Administer Security Hotspots

* Manage security hotspots (e.g., change status, add comments, assign responsibility, and set priority)
* Customize rules and profiles related to security hotspot analysis

### Administer

* Highest level of project permissions
* Customize project settings (e.g., change project name, set branch defaults, and adjust permissions)
* Manage user permissions in the project
* Customize quality profiles and quality gates

### Execute Analysis

* Analyze source code and submit results to SonarQube
* This permission is required to configure CI/CD pipelines to run automated analysis

## Harbor

### Manage Repositories

* Create, delete, and configure repositories within the project
* Push and pull artifacts (e.g., Docker images, Helm charts) to/from the repository
* View and manage tags within the repository

### Manage Project Members

* Invite new members to the project
* Assign roles to members within the project (but cannot edit admin permissions)

### Manage Permissions

* Manage user access and permissions within the project
* Configure access policies for repositories

### Artifact Management

* Scan artifacts for vulnerabilities and security problems
* View scan results and manage identified issues
* Sign and verify artifact signatures for security

### Replication

* Configure and manage replication rules to replicate artifacts to/from other Harbor instances

## Grafana

View Charts and Data

* View charts and data in the organization but cannot edit or change the data

Create and Edit Private Charts

* Create and edit only personal charts (Private Dashboard) that cannot be shared or accessed by other users

Customize Display

* Customize the display of viewed charts

Set Notifications

* Set notifications only for oneself; cannot set notifications for other users

## Vault

create

* Allows creating new data in Vault

read

* Allows reading existing data in Vault

update

* Allows editing existing data in Vault

delete

* Allows deleting data from Vault

list

* Allows listing data in Vault

## Headlamp

Resources

* pods , pods/log , services , endpoints , secrets , deployments , jobs , cronjobs , configmaps , persistentvolumeclaims , ingresses , daemonsets , events , replicasets , replicationcontrollers , statefulsets
* Retrieve (get) and display information about the resources listed above within the service (namespace) but cannot perform other actions such as create or update

## ArgoCD

* Create, edit, and delete applications
* Synchronize applications manually
* Trigger actions on applications such as sync verification, reset, and abort sync
* View and manage application-related resources such as deployments, services, secrets, configmaps
* View and analyze application metrics such as CPU, memory, network usage

## Kubernetes

Kubernetes Config

kube-non-production-admin-role

* pods : View, edit, create, delete, and manage all pods in the cluster
* pods/log : View logs of any pod in the cluster
* services : View, edit, create, delete, and manage all services in the cluster
* endpoints : View all endpoints in the cluster
* secrets : View, edit, create, delete, and manage all secrets in the cluster
* deployments : View, edit, create, delete, and manage all deployments in the cluster
* jobs : View, edit, create, delete, and manage all jobs in the cluster
* cronjobs : View, edit, create, delete, and manage all cronjobs in the cluster
* configmaps : View, edit, create, delete, and manage all configmaps in the cluster
* persistentvolumeclaims : View, edit, create, delete, and manage all persistentvolumeclaims in the cluster
* ingresses : View, edit, create, delete, and manage all ingresses in the cluster
* daemonsets : View, edit, create, delete, and manage all daemonsets in the cluster
* events : View all events in the cluster
* replicasets : View, edit, create, delete, and manage all replicasets in the cluster
* replicationcontrollers : View all replicationcontrollers in the cluster
* statefulsets : View, edit, create, delete, and manage all statefulsets in the cluster

kube-production-admin-role

* pods : View, edit, create, delete, and manage all pods in the cluster
* pods/log : View logs of any pod in the cluster
* services : View, edit, create, delete, and manage all services in the cluster
* endpoints : View all endpoints in the cluster
* secrets : View, edit, create, delete, and manage all secrets in the cluster
* deployments : View, edit, create, delete, and manage all deployments in the cluster
* jobs : View, edit, create, delete, and manage all jobs in the cluster
* cronjobs : View, edit, create, delete, and manage all cronjobs in the cluster
* configmaps : View, edit, create, delete, and manage all configmaps in the cluster
* persistentvolumeclaims : View, edit, create, delete, and manage all persistentvolumeclaims in the cluster
* ingresses : View, edit, create, delete, and manage all ingresses in the cluster
* daemonsets : View, edit, create, delete, and manage all daemonsets in the cluster
* events : View all events in the cluster
* replicasets : View, edit, create, delete, and manage all replicasets in the cluster
* replicationcontrollers : View all replicationcontrollers in the cluster
* statefulsets : View, edit, create, delete, and manage all statefulsets in the cluster