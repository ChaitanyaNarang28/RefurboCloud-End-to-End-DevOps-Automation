**Note:** This project is a fork of `opentelemetry-demo`. Huge thanks to the OpenTelemetry team and contributors for open-sourcing such an impactful demo project. RefurboCloud is an extended implementation tailored for real-world DevOps use cases in the laptop refurbishing domain.

<!-- markdownlint-disable-next-line -->
# <img src="https://opentelemetry.io/img/logos/opentelemetry-logo-nav.png" alt="OTel logo" width="45"> RefurboCloud: End-to-End DevOps Automation for Laptop Refurbishing

[![Slack](https://img.shields.io/badge/slack-@cncf/otel/demo-brightgreen.svg?logo=slack)](https://cloud-native.slack.com/archives/C03B4CWV4DA)
[![Version](https://img.shields.io/github/v/release/open-telemetry/opentelemetry-demo?color=blueviolet)](https://github.com/open-telemetry/opentelemetry-demo/releases)
[![Commits](https://img.shields.io/github/commits-since/open-telemetry/opentelemetry-demo/latest?color=ff69b4&include_prereleases)](https://github.com/open-telemetry/opentelemetry-demo/graphs/commit-activity)
[![Downloads](https://img.shields.io/docker/pulls/otel/demo)](https://hub.docker.com/r/otel/demo)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg?color=red)](https://github.com/open-telemetry/opentelemetry-demo/blob/main/LICENSE)
[![Integration Tests](https://github.com/open-telemetry/opentelemetry-demo/actions/workflows/run-integration-tests.yml/badge.svg)](https://github.com/open-telemetry/opentelemetry-demo/actions/workflows/run-integration-tests.yml)
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/opentelemetry-demo)](https://artifacthub.io/packages/helm/opentelemetry-helm/opentelemetry-demo)

---

## Welcome to RefurboCloud 🔧📦

RefurboCloud is a comprehensive microservice-based application tailored for **laptop refurbishing businesses**, showcasing **end-to-end DevOps automation** with deep **observability powered by OpenTelemetry**.

### Key Highlights

- **Domain-Focused**: Tracks the lifecycle of refurbished laptops, including diagnostics, repair, testing, listing, and order processing.
- **Observability-First**: Every microservice is instrumented with OpenTelemetry for traces, logs, and metrics.
- **DevOps Integrated**: CI/CD pipelines, monitoring, auto-scaling, and log aggregation are built-in using cloud-native tools.
- **Vendor-Ready**: Plug-and-play compatibility with popular observability platforms and monitoring solutions.

---

## Project Goals

- Demonstrate how OpenTelemetry can be used to monitor and observe every component in a production-grade refurbishing pipeline.
- Provide an example architecture for cloud-native DevOps in retail/repair-tech industries.
- Serve as a base platform for vendors and SREs to test observability tools on realistic workloads.

---

## Quick Start 🚀

You can be up and running with RefurboCloud in just a few steps:

- [Docker Setup](https://opentelemetry.io/docs/demo/docker_deployment/)
- [Kubernetes Setup](https://opentelemetry.io/docs/demo/kubernetes_deployment/)

Each deployment includes:

- Instrumented microservices (Inventory, Diagnostics, Repair, Testing, E-Commerce Portal)
- OpenTelemetry Collector, Prometheus, Grafana
- Logging and tracing pipelines via OTLP

---

## RefurboCloud Architecture

This system includes services such as:

- `inventory-service`: Tracks incoming/outgoing refurbished laptops.
- `diagnostics-service`: Simulates diagnostic checks with telemetry events.
- `repair-service`: Coordinates hardware and software refurbishing.
- `qa-service`: Tests and verifies laptops before listing.
- `frontend`: E-commerce UI for customers.
- `order-service`: Handles purchase and logistics.
- `otel-collector`: Aggregates telemetry data and routes it to compatible backends.

---

## Documentation 📖

Check the [official demo documentation][docs] for component breakdown, integration methods, and observability practices. For specific RefurboCloud modules, refer to the internal `/docs` folder.

---

## Inspired by the OpenTelemetry Astronomy Shop

RefurboCloud is based on the [OpenTelemetry Demo](https://github.com/open-telemetry/opentelemetry-demo), extended and customized for the laptop refurbishment domain. We welcome additional forks or implementations targeting other industries!

---

## Who Can Use RefurboCloud?

| For | How RefurboCloud Helps |
|-----|-------------------------|
| **Developers** | Learn how to instrument services with OpenTelemetry. |
| **SREs** | Practice with real tracing, metrics, and logging data. |
| **DevOps Engineers** | Deploy and automate cloud-native services with telemetry. |
| **Vendors** | Showcase observability solutions using a realistic use case. |

---

## Contributing 🤝

Contributions are welcome! Read the [CONTRIBUTING](CONTRIBUTING.md) guidelines and help make RefurboCloud better.

---

## Maintainers

This project is maintained by [Chaitanya Narang](https://github.com/ChaitanyaNarang28) and is actively seeking collaborators from the cloud and observability community. Reach out via GitHub or Slack!

---

## Credits & Thanks 🎉

We extend our sincere gratitude to the [OpenTelemetry community](https://opentelemetry.io) for their robust demo project, which served as the foundation for RefurboCloud.

[![contributors](https://contributors-img.web.app/image?repo=open-telemetry/opentelemetry-demo)](https://github.com/open-telemetry/opentelemetry-demo/graphs/contributors)

---

[docs]: https://opentelemetry.io/docs/demo/
