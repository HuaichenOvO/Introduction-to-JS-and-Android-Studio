There are numerous types of distributed systems. The most common are as follows:

## Client-server
A client-server architecture is broken down into two primary responsibilities. The client is responsible for the user interface presentation, which then connects over the network to the server. The server is responsible for handling business logic and state management. A client-server architecture can easily degrade into a centralized architecture if the server is not made redundant. A truly distributed client-server setup will have multiple server nodes to distribute client connections. Most modern client-server architectures are clients that connect to an encapsulated distributed system on the server.

__前后端，且多个后端之间可以互相传递信息备份，多个后端服务器共同形成一个大后端给 前端访问__

## Multi-tier
A multi-tier architecture expands on the client-server architecture. The server in a multi-tier architecture is decomposed into further granular nodes, which decouple additional backend server responsibilities like data processing and data management. These additional nodes are used to asynchronously process long-running jobs and free up the remaining backend nodes to focus on responding to client requests, and interfacing with the data store.

__有的服务器负责访问，有的服务器负责储存，将业务逻辑分散__

## Peer-to-peer
In a peer-to-peer distributed system, each node contains the full instance of an application. There is no node separation of presentation and data processing. A node contains the presentation layer and data handling layers. The peer nodes may contain the entire state data of the entire system. 

Peer-to-peer systems have the benefit of extreme redundancy. When a peer-to-peer node is initialized and brought online, it discovers and connects to other peers and synchronizes its local state with the state from the greater system. This feature means the failure of one node on a peer-to-peer system won’t disrupt any of the other nodes. It also means that a peer-to-peer system will persist. 

__全是一摸一样的后端服务器，以此来型形成超级稳定性__


## Service-oriented architecture

Service-oriented architecture (SOA) is a predecessor of microservices. The main difference between SOA and microservices is node scope – the scope of microservice nodes exist at the feature level. In microservices a node encapsulates the business logic to handle a specific feature set, such as payment processing. Microservices contain multiple disparate business logic nodes that interface with independent database nodes. Comparatively, SOA nodes encapsulate an entire application or enterprise division. The service boundary for SOA nodes typically includes an entire database system within the node.

Microservices have emerged as a more popular alternative to SOA due to their benefits. Microservices are more composable, allowing teams to reuse functionality provided by the small service nodes. Microservices are more robust and enable more dynamic vertical and horizontal scaling.

__SOA 更像是将整个业务逻辑copy了，和前面的类似；微服务只是将功能打包了，可复用性更高__