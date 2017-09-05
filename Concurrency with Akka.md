CONCURRENCY WITH ACTORS

- Synchronized blocks in JAVA

ACTORS

- Lightweight object
- Communication via message passing
- No shared state
- Supervision
- Distributed by design


AKKA

- Actor Implementation
- Seamless Remoting
- Java, Scala

MESSAGE

- ASK
- TELL
- Message can be anything
- Mailbox (Bounded, Priority, Unbounded)

Birthday example Crn

* ACTOR REF

- Reference to the actor
- ActorRef can be passed around
- Internal state and methods are hidden
- Unique Address

HIERARCHY

- Hierarchical parent child
- Supervision
- Restart, Resume, Stop children

AKKA CLUSTER
- Cluster Membership
- Load Balancing
- Node Partitioning(Roles)
-

APP CLUSTERING VS HARDWARE LB

- A cluster is a group of resources that are trying to achieve a common objective, and are aware of one another.
- Clustering also involves load balancing
- Clustering shares the state
- Load balancing is more infra than cluster is more app side
- Clustering is harder to setup
- From failure-client perspective, when error occurs LB will lose the request, Cluster can retry on other cluster member
