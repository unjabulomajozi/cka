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
  - [Components](https://github.com/unjabulomajozi/cka/blob/master/Cluster%20Architecture/Cluster%20Installation%20via%20Kubeadm/Components.md)
  - Setup
- Kubernetes Object
- RBAC
- Highly available Kubernetes Cluster
- Infrastructure provision
- Cluster version upgrade via Kubeadm
- etd backup & restore
## Workloads & Scheduling
- [Deployment, update & rollbacks](https://github.com/unjabulomajozi/cka/blob/master/Workloads%20&amp;%20Scheduling/Deployment,%20update%20&amp;%20rollbacks.md)
- [Configure applications ConfigMaps & Secrets](https://github.com/unjabulomajozi/cka/blob/master/Workloads%20&amp;amp;%20Scheduling/Configure%20applications%20ConfigMaps%20&amp;%20Secrets.md)
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

# Certifications Tips
- Generate Manifest YAML file
  ```
    kubectl run --generator=run-pod/v1 [PDO_NAME] --image=[IMAGE_NAME] --dry-run -o yaml
  ```

# References
Kubernetes. 2020. What Is Kubernetes?. [online] Available at: <https://kubernetes.io/docs/concepts/overview/what-is-kubernetes/> [Accessed 26 October 2020].

Learnk8s. 2020. How Do You Rollback Deployments In Kubernetes?. [online] Available at: <https://learnk8s.io/kubernetes-rollbacks> [Accessed 26 October 2020].

Learnk8s. 2020. Load Balancing And Scaling Long-Lived Connections In Kubernetes. [online] Available at: <https://learnk8s.io/kubernetes-long-lived-connections> [Accessed 26 October 2020].

MSV, J., Omier, E. and Omier, E., 2020. How Does Service Discovery Work In Kubernetes? – The New Stack. [online] The New Stack. Available at: <https://thenewstack.io/how-does-service-discovery-work-in-kubernetes/> [Accessed 26 October 2020].