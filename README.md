# Infrastructure Monitoring

A server monitoring system using Prometheus and Grafana to track health and performance metrics across a cluster of simulated virtual machines. Metrics are scraped from Node Exporters running on each container and aggregated through a centralized Grafana dashboard, providing real-time insights into CPU, memory, disk, and network usage.

## Stack

- **Prometheus** — time-series database that scrapes and stores metrics
- **Grafana** — visualization and dashboarding
- **Node Exporter** — exposes Linux system metrics (CPU, memory, disk, network)
- **Docker** — containerized deployment simulating a multi-VM environment

## Usage

### Run

```bash
docker compose up -d
```

### Stop

```bash
docker compose down
```

## Project Structure

```
inframonitoring/
├── docker-compose.yml                        # Service definitions
├── prometheus/
│   └── prometheus.yml                        # Scrape targets and intervals
└── grafana/
    └── provisioning/
        ├── datasources/
        │   └── datasource.yml                # Auto-configures Prometheus connection
        └── dashboards/
            └── dashboards.yml                # Dashboard provisioning config
```
