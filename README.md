# RHOAI Observability Dashboards

This directory contains Kustomize templates for deploying RHOAI (Red Hat OpenShift AI) Observability Dashboards.

## Prerequisites

- Kubernetes cluster with Perses installed
- `kubectl` configured to communicate with your cluster
- `kustomize` (v4.5.0 or later) installed

## Dashboards Included

### LLM-D Dashboards
- **Inference Gateway**: Monitors the LLM inference gateway metrics
- **LLM-D**: Main dashboard for LLM-D service monitoring

### vLLM Dashboards
- **Cluster Overview**: High-level cluster metrics and health
- **Performance Statistics**: Detailed performance metrics for vLLM
- **Query Statistics**: Query-related metrics and analytics

## Deployment

1. Update the `namespace` in `kustomization.yaml` if your Perses instance is in a different namespace than `monitoring`.

2. To deploy all dashboards:
   ```bash
   kubectl apply -k .
   ```

3. To preview the resources that will be created:
   ```bash
   kubectl kustomize .
   ```

## Updating Dashboards

To update the dashboards, modify the respective YAML files in their respective directories and re-apply the kustomization:

```bash
kubectl apply -k .
```

## Removing Dashboards

To remove all deployed dashboards:

```bash
kubectl delete -k .
```
