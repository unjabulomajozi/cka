# Deployment, update & rollbacks

## Pods
- Pod
  - What is
  - How to create a pod
    - CLI
    - yaml
      - api
      - kind
      - metadata
        - name
        - labels
      - spec
        - containers
  - Inspection
    - General info
    - Describe
    - Logs
- Container
  - What is?
  - Same containers in one pod?
  - Different containers in one pod?
  - Helper container
    - What is?
    - Why?
    - How main container access helper container
- Relationship between:
  - Worker node and pod
  - Pod and container
  - Pod and docker
- Scaling
  - Replications
    - How
    - Why
- Lifecycle
- Pitfalls
  - What happens when no resources
- Why abstraction over containers
  - Changing the container runtime
- Pods and virtual network (ip address)
  - Solution for Issues with Pod recreation and ip address
    - Service
    - Ingress
## Replica Sets
- Replica
  - What is?
  - Why?
    - **High Availability:** Automatically restart the pod if the pod dies, to keep the current state aligned to desired state of the number of replicas
    - **Load balancing**
    - **Scaling** Can run one or more instances of the pod
  - Relationship with pod
  - Relationship with Load balancing and scaling
- Replication controller
  - What is?
  - Definition
- Replica Set
  - What is?
  - Definition
- Replication Controller vs Replica Set
  - Selector
    - Replica Set can even handle pods not defined on template
      - Then do we need template in the replica set?
        - Yes we do because if those existing pods that you are selecting die, then replica set should know how to creating another
- Can you use replication controller/replica set for one Pod?
  - Yes, because when pod dies it doesn't automatically restart so replication controller will do that for you
- How does it monitor pods
  - By using labels to filter
- Commands
  - Create
    ```
      kubectl create -f [file].yaml
    ```
  - Read
    ```
      kubectl get replicaset
    ```
  - Update
    ```
      kubectl replace -f [file].yaml
    ```
  - Delete **also deletes all underlying PODS**
    ```
      kubectl delete replicaset [name]
    ```
## Deployment
- What is
  - Abstraction over replicaset that adds the following capabilities:
    - Rollbacks
    - Seamless updates
- Definition
- Updates and rollbacks