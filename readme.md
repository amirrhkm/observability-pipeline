## Observability pipeline

OTelCol -> DataPrepper -> OpenSearch

## Usage

```bash
make up

and

make down
```

## Configuration

- `docker-compose.yaml`: Docker compose file
- `otelcol.yaml`: OTel Collector configuration
  - 4317: gRPC receiver
  - 4318: HTTP receiver
- `dataprepper.yaml`: DataPrepper configuration
  - 21891: metrics receiver
    - index: otlp-metrics
  - 21892: logs receiver
    - index: otlp-logs
- `prometheus.yaml`: Prometheus configuration

