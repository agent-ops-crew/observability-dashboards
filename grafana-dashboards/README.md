# Grafana Dashboards Kustomize Overlay

This directory contains Kustomize configurations for deploying Grafana dashboards in an OpenShift cluster.

## Deployment

1. Navigate to this directory:
   ```bash
   cd grafana-dashboards
   ```

2. (Optional) Update the target namespace in `kustomization.yaml` if needed (default is `user-grafana`)

3. Apply the configuration to your cluster:
   ```bash
   kubectl apply -k .
   ```

## LLM-D Dashboards

By default, the LLM-D dashboards are commented out in the `kustomization.yaml` file. To enable them, uncomment the following lines:

```yaml
# LLM-D Dashboards
- llm-d/inference_gateway.yaml
- llm-d/llm-d.yaml
```

## Included Dashboards

- vLLM Cluster Overview
- vLLM Performance Statistics
- vLLM Query Statistics
- (Optional) LLM-D Inference Gateway
- (Optional) LLM-D Dashboard
