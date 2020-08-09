# Certified Kubernetes Security Specialist (CKS)
Online resources and study guide that will help preparing for Certified Kubernetes Security Specialist (CKS) exam. Please make pull request if you think there are better resources to be added. This is currently a work in progress. Inspired by awesome CKA study guide by @walidshaari.

## Exam Curriculum
This exam is coming soon in November 2020. CNCF provides us with CKS curriculum that we can follow:
* [CNCF CKS Curriculum](https://github.com/cncf/curriculum/blob/master/CKS_Curriculum_%20v1.19%20Coming%20Soon%20November%202020.pdf)

### 10% - [Cluster Setup]()
1. [Use Network security policies to restrict cluster level access]()
2. [Use CIS benchmark to review the security configuration of Kubernetes components (etcd, kubelet, kubedns, kubeapi)](https://cloud.google.com/kubernetes-engine/docs/concepts/cis-benchmarks)
3. [Properly set up Ingress objects with security control]()
4. [Protect node metadata and endpoints]()
5. [Minimize use of, and access to, GUI elements]()
6. [Verify platform binaries before deploying]()

### 15% - [Cluster Hardening]()
1. [Restrict access to Kubernetes API]()
2. [Use Role Based Access Controls to minimize exposure](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)
3. [Exercise caution in using service accounts e.g. disable defaults, minimize permissions on newly created ones]()
4. [Update Kubernetes frequently]()

### 15% - [System Hardening]()
1. [Minimize host OS footprint (reduce attack surface)]()
2. [Minimize IAM roles]()
3. [Minimize external access to the network]()
4. [Appropriately use kernel hardening tools such as AppArmor, seccomp]()

### 20% - [Minimize Microservice Vulnerabilities]()
1. [Setup appropriate OS level security domains e.g. using PSP, OPA, security contexts]()
   * [PSP (Pod Security Policy)](https://kubernetes.io/docs/concepts/policy/pod-security-policy/)
   * [OPA (Open Policy Agent)]()
   * [Security Contexts](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/)
2. [Manage kubernetes secrets]()
   * [Concept](https://kubernetes.io/docs/concepts/configuration/secret/)
   * [Task](https://kubernetes.io/docs/tasks/inject-data-application/distribute-credentials-secure/)
3. [Use container runtime sandboxes in multi-tenant environments (e.g. gvisor, kata containers)]()
4. [Implement pod to pod encryption by use of mTLS]()

### 20% - [Supply Chain Security]()
1. [Minimize base image footprint]()
2. [Secure your supply chain: whitelist allowed image registries, sign and validate images]()
3. [Use static analysis of user workloads (e.g. kubernetes resources, docker files)]()
4. [Scan images for known vulnerabilities]()

### 20% - [Monitoring, Logging and Runtime Security]()
1. [Perform behavioral analytics of syscall process and file activities at the host and container level to detect malicious activities]()
2. [Detect threats within physical infrastructure, apps, networks, data, users and workloads]()
3. [Detect all phases of attack regardless where it occurs and how it spreads]()
4. [Perform deep analytical investigation and identification of bad actors within environment]()
5. [Ensure immutability of containers at runtime]()
6. [Use Audit Logs to monitor access]()
