# Certified Kubernetes Security Specialist (CKS)
Online resources and study guide that will help preparing for Certified Kubernetes Security Specialist (CKS) exam. Please make pull request if you think there are better resources to be added. This is currently a work in progress. Inspired by awesome CKA study guide by @walidshaari.

## Exam Curriculum
This exam is coming soon in November 2020. CNCF provides us with CKS curriculum that we can follow:
* [CNCF CKS Curriculum](https://github.com/cncf/curriculum/blob/master/CKS_Curriculum_%20v1.19%20Coming%20Soon%20November%202020.pdf)

### 10% - [Cluster Setup]()
1. [Use Network security policies to restrict cluster level access](https://kubernetes.io/docs/concepts/services-networking/network-policies/)
2. [Use CIS benchmark to review the security configuration of Kubernetes components (etcd, kubelet, kubedns, kubeapi)](https://cloud.google.com/kubernetes-engine/docs/concepts/cis-benchmarks)
3. [Properly set up Ingress objects with security control]()
4. [Protect node metadata and endpoints]()
5. [Minimize use of, and access to, GUI elements]()
6. [Verify platform binaries before deploying]()

### 15% - [Cluster Hardening]()
1. [Restrict access to Kubernetes API](https://kubernetes.io/docs/tasks/administer-cluster/securing-a-cluster/)
2. [Use Role Based Access Controls to minimize exposure](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)
3. [Exercise caution in using service accounts e.g. disable defaults, minimize permissions on newly created ones]()
4. [Update Kubernetes frequently]()

### 15% - [System Hardening]()
1. [Minimize host OS footprint (reduce attack surface)]()
2. [Minimize IAM roles]()
   - Youtube: [AWS IAM Role on Kubernetes with kube2iam](https://www.youtube.com/watch?v=OPpz_LUC-2k)
3. [Minimize external access to the network]()
   - [Mitigating Kubernetes attacks](https://www.youtube.com/watch?v=HWv8ZKLCawM)
4. [Appropriately use kernel hardening tools such as AppArmor, seccomp]()
   - [Restrict a Container's Access to Resources with AppArmor](https://kubernetes.io/docs/tutorials/clusters/apparmor/)
   - [Restrict a Container's Syscalls with Seccomp](https://kubernetes.io/docs/tutorials/clusters/seccomp/)

### 20% - [Minimize Microservice Vulnerabilities]()
1. [Setup appropriate OS level security domains e.g. using PSP, OPA, security contexts]()
   * [PSP (Pod Security Policy)](https://kubernetes.io/docs/concepts/policy/pod-security-policy/)
   * OPA (Open Policy Agent)
     * Youtube: [Intro to Open Policy Agent (Kubecon 2019)](https://www.youtube.com/watch?v=Lca5u_ODS5s) - Torin Sandall
     * [Rego Policy Language Reference](https://www.openpolicyagent.org/docs/latest/policy-language/) and [Rego Playground](https://play.openpolicyagent.org/)
     * Youtube: [Intro to Gatekeeper (Kubecon 2019)](https://www.youtube.com/watch?v=Yup1FUc2Qn0) - Rita Zhang & Max Smythe
     * [Gatekeeper tutorial](https://katacoda.com/austinheiman/scenarios/open-policy-agent-gatekeeper) - Katacoda
     * [Kubernetes Authorization via Open Policy Agent](https://itnext.io/kubernetes-authorization-via-open-policy-agent-a9455d9d5ceb)
   * [Security Contexts](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/)
2. [Manage kubernetes secrets]()
   * [Concept](https://kubernetes.io/docs/concepts/configuration/secret/)
   * [Task](https://kubernetes.io/docs/tasks/inject-data-application/distribute-credentials-secure/)
3. [Use container runtime sandboxes in multi-tenant environments (e.g. gvisor, kata containers)]()
   - Youtube: [Sandboxing your containers with gVisor (Cloud Next '18)](https://www.youtube.com/watch?v=kxUZ4lVFuVo)
   - Youtube: [The Enemy Within: Running Untrusted Code with gVisor](https://www.youtube.com/watch?v=1Ib-rfSzDuM)
   - Youtube: [Kata and gVisor: A Quantitative Comparison](https://www.youtube.com/watch?v=WfEA--v5XpA)
4. [Implement pod to pod encryption by use of mTLS]()
   - [Traffic Encryption using mTLS on Istio](https://www.istioworkshop.io/11-security/01-mtls/)
   - [Secure Service Mesh Communication Across Kubernetes Clusters with Consul](https://learn.hashicorp.com/tutorials/consul/kubernetes-mesh-gateways)

### 20% - [Supply Chain Security]()
1. [Minimize base image footprint]()
2. [Secure your supply chain: whitelist allowed image registries, sign and validate images]()
3. [Use static analysis of user workloads (e.g. kubernetes resources, docker files)]()
   - Tools: [Krane](https://github.com/appvia/krane?utm_sq=ggyni5orp7)
4. [Scan images for known vulnerabilities]()
   - Youtube: [Trivy Open Source Scanner for Container Images](https://www.youtube.com/watch?v=XnYxX9uueoQ)
   - Youtube: [Identifying Common Vulnerabilities and Exposures in Containers with Clair](https://www.youtube.com/watch?v=YDCa51BK2q0)

### 20% - [Monitoring, Logging and Runtime Security]()
1. [Perform behavioral analytics of syscall process and file activities at the host and container level to detect malicious activities]()
2. [Detect threats within physical infrastructure, apps, networks, data, users and workloads]()
3. [Detect all phases of attack regardless where it occurs and how it spreads]()
4. [Perform deep analytical investigation and identification of bad actors within environment]()
5. [Ensure immutability of containers at runtime]()
6. [Use Audit Logs to monitor access]()
