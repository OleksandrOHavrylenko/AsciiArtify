# Local Kubernetes Matrix
Local Kubernetes Matrix for AsciiArtify project



|                               | Minikube                                 | Kind                                  | K3d                                                   |
|-------------------------------|------------------------------------------|---------------------------------------|-------------------------------------------------------|
| Entry                         | Managing Kubernetes on a single machine tool. Has some limitation in scalability. | Managing Kubernetes on a single machine tool| k3d makes it very easy to create single- and multi-node k3s clusters in docker, e.g. for local development on Kubernetes. Allows you to quickly create and test Kubernetes clusters in Docker containers|
| Characteristics               | Is the Kubernetes community’s OG tool for quickly setting up Kubernetes locally. it simulated multi-node clusters via VMs on your local machine, offering a high-fidelity emulation of real-world scenarios                    | Is a more recent favorite for local Kubernetes deployment, using Docker containers to simulate nodes and focusing purely on Kubernetes standard deployments, with community components requiring manual installation.        | Is a featherweight in local Kubernetes deployment, shares a similar approach to kind but opts for deploying a lightweight k3s instead of standard Kubernetes.                  |
| Advantages and disandvantages | Advantage - Offers a high-fidelity emulation of real-world scenarios, down to the OS and kernel module level. Disadvantage - It’s a resource hog, and if your virtualization environment doesn’t support nested virtualization, you’re out of luck, not to mention it’s slow to start.                   | Advantage - Quick starts and a familiar environment for Docker veterans. Disadvantage - Container simulation lacks OS-level isolation, sharing the host’s kernel, which can complicate OS-specific testing. | Advantage - Quick starts and a familiar environment for Docker veterans. Disadvantage - Container simulation lacks OS-level isolation, sharing the host’s kernel, which can complicate OS-specific testing. The trade-offs include a super-slimmed-down OS (sans glibc), complicating certain OS-level operations. |
| Conclusions                   | For OS-level isolation tests, minikube’s VM Driver is unbeatable           | For everything in between, kind offers a balanced compromise between compatibility and performance.  | If speed and resource efficiency are your top priorities, k3d is your choice. |

K3d is the best solution for AsciiArtify, is speed and resorce efficient, supports Kubernetes clasters in docker containers.

### Deployment Demo for HelloWorld application on k3d.

![Image](./demo.gif)



