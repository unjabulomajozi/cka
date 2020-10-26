# CKA Notes
Certified Kubernetes Administrator Notes

- What is Kubernetes?
  
  > Kubernetes (k8s) is an open-source system for automating deployment, scaling, and management of containerized applications. (What is Kubernetes?, 2020)

  It provides the following:
  - Automated rollouts and rollbacks **incremental application version**
  - Service discovery **pods association with services via labels and selectors**
  - Load balancing **Even traffic distribution**
  - Service topology
  - Secret and configuration management ****
  - Scaling
  - Self-healing **keeps application state constant**
  - Storage orchestration
  - Automatic bin packing

  And it doesn't:
  - Host your source code and build your application
  <!-- TO DO -->

## Cluster Architecture
- Cluster installation via Kubeadm
  - [Components]()
  - Setup
- RBAC
- Highly available Kubernetes Cluster
- Infrastructure provision
- Cluster version upgrade via Kubeadm
- etd backup & restore
## Workloads & Scheduling
- Deployment, update & rollbacks
- Configure applications ConfigMaps & Secrets
- Scale Applications
- Robust self-healing application deployments
- Resources & Pod Scheduling
- Manifest management & common templating tools
## Services & Networking
- Cluster nodes host networking configuration
- Service types (ClusterIP, NodePort, LoadBalancer) and endpoints
- Connectivity between Pods
- Ingress controllers and resources
- CoreDNS configuration and use
- Container network interface plugin
## Storage
- Storage Classes & Persistent Volumes
- Volume mode, access modes & reclaim policies for volumes
- Persistent volume claims primitive
- Applications with persistent storage configuration
## Troubleshooting
- Cluster & node logging
- Application monitoring
- Container stdout & stderr logs
- Application failure troubleshoot
- Cluster component failure troubleshoot
- Networking troubleshoot