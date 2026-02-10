# ADR-001: Self-Hosted Prometheus Over Datadog/New Relic

## Status: Accepted | Date: 2026-02-10

## Decision
Self-hosted Prometheus + Grafana over SaaS monitoring (Datadog, New Relic).

## Why
- Datadog costs $15-23/host/month, scales to thousands/month for real infra
- Prometheus + Grafana = free, unlimited metrics
- Full control over data retention, alerting rules, dashboards
- No vendor lock-in on metric format
