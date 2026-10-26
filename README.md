# VM monitoring lab

A local Docker Compose setup to learn how host metrics get collected and displayed. It uses Prometheus, node-exporter and Grafana.

## Start it on your own machine
```bash
docker compose up -d
docker compose ps
```

Grafana: http://localhost:3000 · Prometheus: http://localhost:9090

Default Grafana login may be `admin` / `admin` on first launch. Change it immediately and keep the service restricted to localhost. Container images should be reviewed and updated before use.

## Useful queries
- `up`
- `node_memory_MemAvailable_bytes`
- `node_filesystem_avail_bytes`

`alert_rules.yml` includes an example for thinking about disk pressure. This is a **lab configuration**, not a production monitoring system.

## References
[Prometheus documentation](https://prometheus.io/docs/) · [Grafana documentation](https://grafana.com/docs/)
