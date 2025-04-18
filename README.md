# Kubernetes Cluster Setup with k3s

## Project Overview

This documentation outlines our approach to setting up a Kubernetes cluster using k3s in a VM environment. After encountering port blocking issues in GitHub Codespaces and resource sharing limitations in local environments, we've migrated to a VM-based k3s solution for our development and deployment needs.

## Components

Our Kubernetes cluster integrates the following key components:

1. **k3s** - A lightweight Kubernetes distribution optimized for edge and IoT deployments
2. **Jenkins** - CI/CD automation server for building, testing, and deploying applications
3. **Gitea** - Self-hosted Git service for source code management
4. **Supabase** - Open source Firebase alternative with a Postgres database
5. **Atomic CM** - Configuration management for the cluster

## Installation Links

### CI/CD Pipeline
- [Jenkins Deployment]() <!-- Add your Jenkins deployment link -->

### Source Code Management
- [Gitea Configuration]() <!-- Add your Gitea setup link -->

### Database Layer
- [Supabase Integration]() <!-- Add your Supabase integration link -->

### Configuration Management
- [Atomic CM Setup]() <!-- Add your Atomic CM configuration link -->

## Deployment Architecture

Our k3s-based Kubernetes cluster runs on a virtual machine with the following architecture:

```
VM Host
└── k3s Kubernetes Cluster
    ├── Jenkins Deployment
    │   
    ├── Gitea Deployment + Services
    │  
    ├── Supabase Components
    │   
    └── Atomic CM (Cluster-wide)
```

## Known Issues and Solutions

### Port Blocking in Codespaces
We initially attempted deployment in GitHub Codespaces but encountered security restrictions that blocked required ports for communication between services.

### Resource Sharing Limitations
Local environment deployments faced challenges with resource sharing among team members, making collaboration difficult.

### Solution
Migration to a k3s-based VM environment resolved these issues by:
- Providing full control over port configurations
- Enabling centralized access for all team members
- Reducing resource requirements through k3s's lightweight architecture

## Access Information


- Jenkins Web Interface: [Jenkins URL]() (http://157.90.239.132:32001/)
- Gitea repo: [Gitea URL]() http://157.90.239.132:3000/aviat/atomic-crm
- Supabase Dashboard: [Supabase URL]() http://157.90.239.132:31370/project/default/sql/1




