# RHOAI Observability Dashboards

This repository contains Grafana dashboards and Kustomize configurations for monitoring Red Hat OpenShift AI (RHOAI) components, including LLM-D and vLLM services.

## 📋 Overview

This project provides pre-configured Grafana dashboards for monitoring various aspects of RHOAI services. The dashboards are designed to work with Prometheus metrics and are deployed as Kubernetes custom resources using the Grafana Operator.

## 📁 Directory Structure

```
.
├── grafana-dashboards/          # Grafana dashboard configurations
│   ├── dashboards/             # JSON dashboard definitions
│   │   ├── llm-d/             # LLM-D service dashboards
│   │   └── vllm/               # vLLM service dashboards
│   └── kustomization.yaml      # Kustomize configuration
└── README.md                   # This file
```

## 🚀 Prerequisites

- Kubernetes cluster with admin access
- Grafana Operator installed
- Prometheus Operator or similar monitoring stack
- `kubectl` and `kustomize` CLI tools

## 🛠️ Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/agent-ops-crew/observability-dashboards.git
   cd observability-dashboards
   ```

2. Deploy the dashboards using Kustomize:
   ```bash
   kubectl apply -k grafana-dashboards/
   ```

## 🎛️ Dashboards

### LLM-D Dashboards
- **LLM-D Main**: Overview of LLM-D service metrics
- **Inference Gateway**: Metrics for the LLM-D inference gateway

### vLLM Dashboards
- **Cluster Overview**: High-level cluster metrics
- **Performance Statistics**: Detailed performance metrics
- **Query Statistics**: Query performance and analytics

## 🔄 Updating Dashboards

To update the dashboards:

1. Make your changes to the JSON files in the `grafana-dashboards/dashboards/` directory
2. Commit and push your changes
3. Apply the updated configuration:
   ```bash
   kubectl apply -k grafana-dashboards/
   ```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch for your feature
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## 📄 License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

## 📞 Support

For support, please open an issue in the GitHub issue tracker.
