# DHRT: Optimize Resource Allocation for Serverless Workloads 🚀

![GitHub release](https://img.shields.io/github/release/ziyankin/dhrt-deadline-and-heterogeneity-aware-resource-tuner.svg) ![GitHub issues](https://img.shields.io/github/issues/ziyankin/dhrt-deadline-and-heterogeneity-aware-resource-tuner.svg) ![GitHub forks](https://img.shields.io/github/forks/ziyankin/dhrt-deadline-and-heterogeneity-aware-resource-tuner.svg) ![GitHub stars](https://img.shields.io/github/stars/ziyankin/dhrt-deadline-and-heterogeneity-aware-resource-tuner.svg)

[![Download Releases](https://img.shields.io/badge/Download%20Releases-Click%20Here-brightgreen)](https://github.com/ziyankin/dhrt-deadline-and-heterogeneity-aware-resource-tuner/releases)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Metrics and Monitoring](#metrics-and-monitoring)
- [Contributing](#contributing)
- [License](#license)

## Overview

DHRT stands for Deadline and Heterogeneity-aware Resource Tuner. This tool optimizes resource allocation for serverless workloads that have strict execution deadlines. It operates in heterogeneous Kubernetes clusters, adjusting resource allocations dynamically based on real-time metrics. By utilizing historical data, DHRT configures and schedules workloads according to their resource needs and specified deadlines.

## Features

- **Dynamic Resource Tuning**: Adjusts resources in real-time based on workload demands.
- **Deadline Awareness**: Ensures that serverless workloads meet their execution deadlines.
- **Heterogeneous Cluster Support**: Works efficiently in diverse Kubernetes environments.
- **Historical Data Utilization**: Leverages past metrics to improve future resource allocation.
- **Integration with Monitoring Tools**: Compatible with Grafana and Prometheus for real-time monitoring.

## Architecture

The architecture of DHRT is designed to facilitate seamless resource management in heterogeneous environments. Below is a simplified diagram illustrating the core components:

![Architecture Diagram](https://example.com/path/to/architecture-diagram.png)

1. **Metrics Collector**: Gathers real-time data from Kubernetes and other sources.
2. **Resource Allocator**: Dynamically adjusts resources based on current metrics.
3. **Scheduler**: Configures workloads based on historical data and execution deadlines.
4. **Monitoring Interface**: Integrates with Grafana and Prometheus for visualization.

## Installation

To install DHRT, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/ziyankin/dhrt-deadline-and-heterogeneity-aware-resource-tuner.git
   cd dhrt-deadline-and-heterogeneity-aware-resource-tuner
   ```

2. Build the project:
   ```bash
   go build
   ```

3. Install any required dependencies:
   ```bash
   go mod tidy
   ```

4. Ensure that you have Kubernetes and the necessary permissions to deploy workloads.

## Usage

After installation, you can start using DHRT. Here’s a simple command to launch the tuner:

```bash
./dhrt --config path/to/config.yaml
```

Make sure to replace `path/to/config.yaml` with your actual configuration file path.

### Example Configuration

Here’s a sample configuration file:

```yaml
apiVersion: v1
kind: Config
metadata:
  name: dhrt-config
spec:
  resourceLimits:
    cpu: "200m"
    memory: "512Mi"
  deadlines:
    - workload: "example-workload"
      deadline: "5m"
```

This configuration sets resource limits and specifies a deadline for a workload.

## Configuration

DHRT allows you to customize various settings. Here are some key configuration options:

- **Resource Limits**: Define CPU and memory limits for workloads.
- **Deadlines**: Set execution deadlines for different workloads.
- **Metrics Sources**: Specify where to collect metrics from (e.g., Prometheus).

### Advanced Configuration

For advanced users, DHRT supports custom metrics and additional tuning parameters. Refer to the official documentation for detailed options.

## Metrics and Monitoring

DHRT integrates seamlessly with Grafana and Prometheus. You can visualize real-time metrics to monitor resource usage and workload performance.

### Setting Up Grafana

1. Install Grafana:
   ```bash
   kubectl apply -f https://raw.githubusercontent.com/grafana/helm-charts/main/charts/grafana/templates/deployment.yaml
   ```

2. Configure data sources to connect to Prometheus.

3. Import DHRT dashboards from the official repository.

## Contributing

Contributions are welcome! If you want to improve DHRT, please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add your message"
   ```
4. Push to your fork:
   ```bash
   git push origin feature/your-feature
   ```
5. Create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

For more information, visit the [Releases section](https://github.com/ziyankin/dhrt-deadline-and-heterogeneity-aware-resource-tuner/releases). 

[![Download Releases](https://img.shields.io/badge/Download%20Releases-Click%20Here-brightgreen)](https://github.com/ziyankin/dhrt-deadline-and-heterogeneity-aware-resource-tuner/releases)