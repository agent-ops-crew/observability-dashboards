# RHOAI Observability Dashboards

This directory contains Kustomize templates for deploying RHOAI (Red Hat OpenShift AI) Observability Dashboards.

## Prerequisites

- Kubernetes cluster with Perses installed
- `kubectl` configured to communicate with your cluster
- `kustomize` (v4.5.0 or later) installed
- `Cluster Observability Operator` (v1.2.1 or later)
- `Perses` Tech Preview Enabled 

## Quickstart

Deploys dashboards to namespace `openshift-cluster-observability-operator`:

```bash
kubectl apply -k .
```

## Dashboards Included

### LLM-D Dashboards
- **Inference Gateway**: Monitors the LLM inference gateway metrics
- **LLM-D**: Main dashboard for LLM-D service monitoring

### vLLM Dashboards
- **Cluster Overview**: High-level cluster metrics and health
- **Performance Statistics**: Detailed performance metrics for vLLM
- **Query Statistics**: Query-related metrics and analytics

### Turn On Perses Tech Preview

Create the following UI Plugin:

```yaml
apiVersion: observability.openshift.io/v1alpha1
kind: UIPlugin
metadata:
  name: monitoring
spec:
  type: Monitoring
  monitoring:
    perses:
      enabled: true
```