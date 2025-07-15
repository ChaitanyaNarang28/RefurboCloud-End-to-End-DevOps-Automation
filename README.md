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

## 🧩 Microservices Overview

This system is composed of modular microservices that together form a robust, local e-commerce simulation platform for refurbished laptops.
All services were **successfully built and edited on 02-06-2025 for local use**.

### 🛍️ Commerce & User Interaction

* **`frontend`**:
  Main user interface for customers, built as a responsive e-commerce web application.

* **`cart`**:
  Manages shopping cart sessions, item additions/removals, and updates in real-time.

* **`checkout`**:
  Handles the checkout process including validation, order confirmation, and transition to payment.

* **`order-service`**:
  Processes customer orders and manages the flow from order placement to shipment.

* **`payment`**:
  Manages payment transactions, validations, and integrations with simulated gateways.

* **`currency`**:
  Provides currency formatting and conversion logic, supporting global pricing models.

* **`email`**:
  Sends transactional and notification emails like order confirmations and shipment updates.

* **`recommendation`**:
  Suggests relevant refurbished products based on user behavior and historical data.

* **`quote`**:
  Generates dynamic pricing and offers for selected laptop models or configurations.

### 🧾 Business & Operations

* **`accounting`**:
  Tracks financial transactions, invoices, and reporting for business operations.

* **`ad`**:
  Handles advertisement display and tracking within the platform.

* **`product-catalog`**:
  Manages product listings, descriptions, pricing, and categorization.
  ✅ **Final CI/CD check completed – 3 weeks ago**

* **`shipping`**:
  Calculates shipping logistics, timelines, and manages dispatch tracking.

### ⚙️ Infrastructure & Observability

* **`otel-collector`**:
  Collects and exports telemetry data (metrics, logs, traces) to observability tools.

* **`prometheus`**:
  Monitors services and gathers performance metrics across the platform.

* **`grafana`**:
  Visualizes service metrics and dashboards from Prometheus and OpenTelemetry sources.

* **`flagd`** and **`flagd-ui`**:
  Provide feature flag management and a UI to toggle features at runtime.

* **`frontend-proxy`**:
  Acts as a reverse proxy for routing frontend requests to appropriate backend services.

* **`kafka`**:
  Message broker facilitating event-driven communication between services.

* **`load-generator`**:
  Simulates user load and transactions for stress testing and benchmarking.

### 🔒 Risk & Quality Management

* **`fraud-detection`**:
  Detects suspicious transactions and mitigates fraudulent activity.

* **`image-provider`**:
  Serves product images and media resources efficiently across the platform.

---



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
