# Kyverno Demo

Practical Kubernetes policies for security & best practices using Kyverno.

## Quick Start

### 1. Install Kyverno
```bash
kubectl create -f https://github.com/kyverno/kyverno/releases/latest/download/install.yaml
```

### 2. Apply Policies
```bash
kubectl apply -f policies/
```

### 3. Test with Example Workloads

**Bad pod (will be rejected):**
```bash
kubectl apply -f workloads/bad-pod.yaml
```

**Good pod (will be accepted):**
```bash
kubectl apply -f workloads/good-pod.yaml
```

**Production deployment:**
```bash
kubectl apply -f workloads/kubesrv-deployment.yaml
```

## Test Application

This demo uses [kubesrv](https://github.com/bansikah22/kubesrv) - a lightweight C server for testing Kubernetes deployments.

- **Image:** `bansikah/kubesrv:latest`
- **Port:** 8080
- **Purpose:** Minimal test server for policy validation

## Policy Examples

- **Security:** Block privileged containers
- **Resource Management:** Enforce CPU/memory limits
- **Automation:** Auto-inject security contexts

## Learn More

Read the complete guide: [docs/kyverno-practical-guide.md](docs/kyverno-practical-guide.md)
