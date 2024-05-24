## Contents

- Upgrades for K3s
- H/V scaling 
- Cluster Configuration
- GitLab CI Integration
- Sealed-Secrets master key Rotation
- PostgreSQL Secret management with Vault 

## Automated Upgrades for K3s

K3s cluster upgrades can be managed using the Kubernetes-native Rancher's system-upgrade-controller. This involves using a custom resource definition (CRD), a `plan`, and a controller. The plan specifies upgrade policies and node selection criteria, while the controller executes the upgrades based on these plans.

#### Installation

To automate K3s cluster upgrades:

1. **Install the System Upgrade Controller**:
	
```bash
kubectl apply -f https://github.com/rancher/system-upgrade-controller/releases/latest/download/system-upgrade-controller.yaml
```
    
2. **Deploy the CRD**:
```bash
kubectl apply -f https://github.com/rancher/system-upgrade-controller/releases/latest/download/crd.yaml
```

#### Configuring Plans

Create at least two plans, one for server nodes and another for agent nodes:
```yaml
# Server Node Upgrade Plan
apiVersion: upgrade.cattle.io/v1
kind: Plan
metadata:
  name: server-plan
  namespace: system-upgrade
spec:
  concurrency: 1
  cordon: true
  nodeSelector:
    matchExpressions:
      - key: node-role.kubernetes.io/control-plane
        operator: In
        values:
        - "true"
  serviceAccountName: system-upgrade
  upgrade:
    image: rancher/k3s-upgrade
  version: v1.24.6+k3s1

# Agent Node Upgrade Plan
apiVersion: upgrade.cattle.io/v1
kind: Plan
metadata:
  name: agent-plan
  namespace: system-upgrade
spec:
  concurrency: 1
  cordon: true
  nodeSelector:
    matchExpressions:
      - key: node-role.kubernetes.io/control-plane
        operator: DoesNotExist
  prepare:
    args:
      - prepare
      - server-plan
    image: rancher/k3s-upgrade
  serviceAccountName: system-upgrade
  upgrade:
    image: rancher/k3s-upgrade
  version: v1.24.6+k3s1

```
#### Monitoring Upgrades

To track the progress of an upgrade, use:
```bash
kubectl -n system-upgrade get plans -o yaml kubectl -n system-upgrade get jobs -o yaml`
```
#### Downgrade Prevention

Kubernetes does not support downgrades of control-plane components. The upgrade plans will fail and leave nodes cordoned if an attempt is made to downgrade.

**Example of a Failed Upgrade:**

```bash
kubectl get pods -n system-upgrade kubectl get nodes`
```

**To Recover from a Failed Upgrade:**

- Adjust the plan to target a release equal to or newer than the current cluster version.
- Delete the plan and manually uncordon the nodes.

### Cluster Configuration

Detailed configuration of cluster settings, node configurations, and security measures.

### GitLab CI Integration

Steps to integrate and automate deployments using GitLab CI.

### PostgreSQL Deployment and Secret Rotation

Guidelines for deploying PostgreSQL databases and securely rotating secrets.

### Manual Upgrades

K3s can also be manually upgraded using either the installation script or by directly replacing the binary.

#### Using the Installation Script
```bash
curl -sfL https://get.k3s.io | sh -s -`
```

#### Using the Binary

1. Download the desired version from the [K3s releases page](https://github.com/k3s-io/k3s/releases).
2. Replace the existing binary:

```bash
sudo mv k3s /usr/local/bin/`
```

### Release Channels

K3s releases can be followed through various channels:

- **Stable**: Recommended for production.
- **Latest**: Includes the most recent features.
- **Version-specific channels**: Tracks updates for specific Kubernetes minor versions.

For further details, visit the [K3s documentation](https://docs.k3s.io/upgrades/).

This refactoring aims to make the document more navigable and concise, with clear instructions and organized sections.

## GitLab CI Integration

## ...

## Get Vault access Token 
```bash
kubectl get secrets -n vault vault-unseal-keys -o jsonpath={.data.vault-root} | base64 --decode
```

In psql cluster manifest this option for vault connection is required 
```yaml
enableSuperuserAccess: true
```
##  PostgreSQL Deployment and Secret Rotation

```yaml
app: 
  metadata:
    annotations: 
		vault.hashicorp.com/agent-inject: 'true'  
		vault.hashicorp.com/agent-inject-token: 'true'  
		vault.hashicorp.com/agent-inject-secret-db-creds: "database/creds/db-app"  
		vault.hashicorp.com/agent-inject-template-db-creds: |  
		{{- with secret "database/creds/db-app" -}}  
		postgres://{{ .Data.username }}:{{ .Data.password }}@postgres:5432/appdb?sslmode=disable  
		{{- end }}  
		vault.hashicorp.com/ca-cert: /vault/tls/ca.crt  
		vault.hashicorp.com/role: vault  
		vault.hashicorp.com/tls-secret: vault-tls
```

[Example usage of agent injector](https://developer.hashicorp.com/vault/docs/platform/k8s/injector/examples)
[Annotaions documentation](https://developer.hashicorp.com/vault/docs/platform/k8s/injector/annotations)
## ...


## Sealed-Secrets Key Rotation 

```bash
kubeseal create ns sealed-secrets # If not deployed 

# Setting env 
export PRIVATEKYE="acmetls.key"
export PUBLICKEY="acmetls.crt"
export NAMESPACE="sealed-secrets"
export SECRETNAME="acme-leys"

openssl req -x509 -nodes -newkey rsa:4096 -keyout "$PRIVATEKEY" --out "$PUBLICKKEY" -subj "/CN=sealed-secrets/O=sealed-secret"
```


## Scaling (H/V) k3s cluster 

```bash
sudo k3s agent --server https://myserver:6443 --token ${NODE_TOKEN} #75826f6e52d4fa9e3824773a02fba755
```