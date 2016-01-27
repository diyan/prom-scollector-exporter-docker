# prom-scollector-exporter-docker
Server that accepts metrics via the OpenTSDB/Bosun protocol and exports them as Prometheus metrics.

Bosun's scollector is a replacement for OpenTSDB's TCollector and can be used to send metrics to a Bosun, OpenTSDB server and Prometheus scollector exporter. More info at http://bosun.org/scollector/

Prometheus is an open-source service monitoring system and time series database inspired by Google's Borgmon. More info at http://prometheus.io/

# How to use this image

Print help:
```bash
docker run --rm diyan/prom-scollector-exporter --help
```

The most simple usage:
```bash
docker run -d --name=prom_scollector_exporter \
  -p 9107:9107 \
  diyan/prom-scollector-exporter \
  -http=0.0.0.0:9107
```
