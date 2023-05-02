# Template of Finall Course Project Report

The repo includes a makefile so you can directly `make` the PDF. 

---

# Structure of the paper

## Contents
- Common patterns of failure cases
  - Liveness
  - Safety
- Describing each failure cases based on common patterns
  - 
- Describing why they happen
  - System design level explanation
    - Reconciliation
    - There is no  like system 
    - Many controllers interact each other
  - Development environment explanation
    - Open source, different contributors implement different part and they are likely to be conflicted each other
  - Challenges
    - Why is it challenging to find failures?
      - The system has a large number of components interacting each other. The search space is enourmously large and impossible to search all of them. The complexity makes it hard to test or verify it since the search space is enormously large. In addition, it is very likely that developer just 
      - The failures are unmasked under a specific combination of interactions between multiple constituents. It does not manifest always and most of time it functions without creating problems. It is particularly hard to reproduce since you need to configure all controllers participating in the failure. Even after successfully reproducing it, it is not clear who is reponsible for it. Multiple entities are involved in the case and unfortunately you cannot blame one since none of them does clearly bad thing.
    - Why is it challenging to fix failures?
      - If you look at each controller separately, individual controller does not imply any buggy or unexpected behavior. However, once it interacts with other parts of the system, they are entangled each other and break down. If controller is tested individually, it will pass all the tests. Undesirable behaviro
      - Most of time, it is hard to argue that they are bugs. What is worse is even if it is agreed by the community that it is a bug, oftentimes there is no clear way to fix it. Again, this is because individual controller is not committing misconduct. It makes it difficult to fix this type of undesirable behaviors.
- Insights from failure study
  - ...

## Structure
1. Introduction
2. Background
   1. Cluster management system
      1. What is Kubernetes
         1. Reconciliation
         2. Controller
            1. Kubelet
            2. Deployment
            3. Scheduler
            4. HPA
            5. Descheduler
            6. Api-server
            7. etcd
3. 
4. Case study (reproduction and anaylsis)
   1. Common patterns of failure cases
   2. Detailed examples
      1. Description
      2. Some plots
   3. Insight
5. Related work
   1. Testing
   2. Chaos engineering
   3. Model checking
   4. Formal verification
   5. Statistical model
   6. Monitoring system
      1. Distributed tracing
         1. Jaegur, Prometheus, ...
      2. What are other monitoring systems?
   7. 
6. Discussion and Future work
   1. Discussion
      1. Scalability
      2. Precise modeling
      3. 
   2. Future work
      1. verifying k8s
7. Conclusion