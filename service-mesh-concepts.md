# Service Mesh

A service mesh is a dedicated infrastructure layer for making service-to-service communication safe, fast, and reliable. It is responsible for the reliable delivery of requests through the complex topology of services that comprise a modern, cloud native application. If you're building a cloud native application, you need a service mesh.

In the cloud native model, a single application might consist of hundreds of services; each service might have thousands of instances; and each of those instances might be in a constantly-changing state as they are dynamically scheduled by an orchestrator like Kubernetes. In this model, service communication is incredibly complex, it is a pervasive and fundamental part of runtime behavior. Managing it is vital to ensuring end-to-end performance and reliability.

## What does a service mesh actually do?

A service mesh like Linkerd manages this complexity with a wide array of powerful techniques: circuit-breaking, latency-aware load balancing, eventually consistent \(advisory\) service discovery, retires, and deadlines.

## Service Mesh Concepts

While both Istio and Linkerd are service mesh. They can work together. Istio can be the control pane of Linkerd.



| Feature | Description | Istio | Linkerd | Conduit |
| :--- | :--- | :--- | :--- | :--- |
| Overall | One sentence introduction. | A platform to connect, manage and secure microservices. | Feature Rich, many production use cases. | Next-generation ultralight service mesh for Kubernates |
| Site | The official website | [https://istio.io/about/intro.html](https://istio.io/) | https://linkerd.io/ | [https://buoyant.io/products/\#products-Conduit](https://www.gitbook.com/book/gangwang2/cloud-notes/edit#) |
| Traffic Management |  | Intelligent Routing and Load balancing | latency-aware load balancing. Runtime traffic routing |  |
|  |  | Resilience across languages and platforms | Any language, any environment |  |
|  |  | Fleet-wide policy enforcement |  |  |
|  |  | In-depth telemetry and reporting |  |  |
|  |  |  | Fast, high performance |  |
|  |  |  | Integrates with service discovery systems |  |
|  |  |  | Production ready and proven |  |
|  |  |  | Member Project of CNCF |  |
|  |  |  |  |  |



