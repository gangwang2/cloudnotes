---
date: 2018-02-05T00:00:00.000Z
---

# Service Mesh with Linkerd

## Overview

When a request is made to a service through Linkerd, a simplified timeline of events is as follows:

1. Linkerd applies dynamic routing rules to determine which service the requester intended. The service is versioned. The dynamic routing rules can be applied globally or to a slice of the traffic.
2. Having found the correct destination, Linkerd retrieves the corresponding pool of instances from the relevant service discovery endpoint, of which there may be several. 
3. Linkerd chooses the instance most likely to return a fast response based on a variety of factors, including its observed latency for recent requests.
4. Linkerd attempts to send the request to the instance, recording the latency and response type of the result.
5. If the instance is down, unresponsive, or fails to process the request, Linkerd retries the request on another instance if it knows the service is idempotent.
6. If an instance is consistenly returning errors, Linkerd evicts it from the load balancing pool, to be periodly retried later.
7. If the deadline for the requests has elapsed, Linkerd proactilely fails the request rather than adding load with further retries.
8. Linkerd captures every aspect of the above behavior in the form of metrics and distributed tracing, which are emitted to a centralized metrics system.
9. 
## References

[https://linkerd.io/](https://linkerd.io/)

