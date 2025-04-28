# Understanding Observablity

Initial outline

## Setup

```bash
curl -o grafana_dashboard.json https://grafana.com/api/dashboards/1860/revisions/40/download
```

[Node Exporter dashboard](https://grafana.com/grafana/dashboards/1860-node-exporter-full/)

## Start

`./start.sh` and in a browser navigate to <[Grafana](http://localhost:3000/login)>

Credentials are  `admin/admin `
> 🪖 Don't do this in prod

The hostnames are valid inside the docker network. Use localhost.
![Prometheus](prometheus.png)

### promql

```sql
    node_cpu_seconds_total
```

## TODO

node exporter uses environment variable `"uid": "${DS_PROMETHEUS}"`. 
The node exporter dashboard does not read correctly from the prometheus datasource.