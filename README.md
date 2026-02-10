# Observability Stack

> One-command monitoring — Prometheus + Grafana + Loki + Alertmanager. Pre-built dashboards, structured logging, SLA alerting. Deploy in 60 seconds.

[![Prometheus](https://img.shields.io/badge/Prometheus-metrics-orange)]()
[![Grafana](https://img.shields.io/badge/Grafana-dashboards-green)]()
[![Docker](https://img.shields.io/badge/docker--compose-one--command-blue)]()

## Architecture

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│ Application │────▶│ Prometheus  │────▶│  Grafana    │
│  /metrics   │     │  (scrape)   │     │ (dashboards)│
└─────────────┘     └──────┬──────┘     └─────────────┘
                           │
┌─────────────┐     ┌──────▼──────┐     ┌─────────────┐
│ Application │────▶│    Loki     │────▶│  Grafana    │
│  (logs)     │     │  (ingest)   │     │  (explore)  │
└─────────────┘     └─────────────┘     └─────────────┘
                           │
                    ┌──────▼──────┐     ┌─────────────┐
                    │Alertmanager │────▶│ Slack/Email │
                    │  (rules)    │     │  (notify)   │
                    └─────────────┘     └─────────────┘
```

## Pre-Built Dashboards

| Dashboard | Metrics |
|-----------|---------|
| API Overview | Request rate, p50/p95/p99 latency, error rate |
| Infrastructure | CPU, RAM, disk, network I/O |
| LLM Inference | Tokens/sec, model load time, queue depth |
| Business | Active users, queries/day, cost/query |

## Quick Start

```bash
docker-compose up -d    # Prometheus :9090, Grafana :3000, Loki :3100
# Default Grafana login: admin/admin
```

## Revenue

Monitoring setup for clients **R3,000-5,000** + **R1,500/month managed monitoring**. "Your systems, monitored 24/7, alerts to your phone."

---
*MIT License*
