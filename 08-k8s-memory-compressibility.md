A common challenge for kubernetes user is configuring the memory and cpu footprint for their workload.
The following policies can be found on the web and in the wild:

|                    |   No Opinion  |   Static Allocation  |   Reasonable Bounds |   Robusta  |   Flexible with Guidance  |
|--------------------|---------------|----------------------|---------------------|------------|---------------------------|
|   Cpu requests     |   -           |   n                  |   n                 |   n        |   n                       |
|   Cpu Limits       |   -           |   n                  |   2n                |   -        |   -                       |
|   Memory Requests  |   -           |   m                  |   m                 |   m        |   m                       |
|   Memory Limits    |   -           |   m                  |   2m                |   m        |   -                       |

1. set limits nor requests for memory or cpu
1. set the limit equal to request for both cpu and memory
1. set the limit to n times the request for both cpu and memory, where n is typically 1.5 to 2 
1. [set memory limit=request](https://home.robusta.dev/blog/kubernetes-memory-limit), [never set CPU limits](https://web.archive.org/web/20220805232857/https://home.robusta.dev/blog/stop-using-cpu-limits/)
1. set requests for memory and cpu, but no limits


This post argues for the last approach as the best default policy, because of two reasons:
1. we can show experimentally that memory and cpu are both compressible resources. This means that after a peak in load, the resource will be made available to the pool
1. in practice, the negative business impact of killing a pod is higher than a brief spike in cloud cost burn rate

## Memory Compressibility

A point of contention is the compressibilty of memory. In one of the [leading blogs](https://home.robusta.dev/blog/kubernetes-memory-limit) on the topic, it's explained as follows:

> Because memory is a non-compressible resource. Once you give a pod memory, you can only take it away by killing the pod. 

This echoes the original [kubernetes design docs](https://web.archive.org/web/20220413194743/https://github.com/kubernetes/design-proposals-archive/blob/8da1442ea29adccea40693357d04727127e045ed/node/resource-qos.md#incompressible-resource-guarantees).

In my previous project, we observed a different behavior and [Dan Levin](https://badpacket.in/) created [an experiment](https://github.com/cromulentorg/memallocdemo) to confirm these observations.












myth 1: memory will remain dedicated to a pod once a process in a pod will claim it for a moment 

myth 2: the aks autoscaler does not scale down after a pod is done using a certain amount of memory