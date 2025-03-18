#### go-server-grafana-prometheus
Experimentation with Grafana + Prometheus using a quite simple Go server.

#### Steps to run the server
1. Start Prometheus using the configuration
`prometheus --config.file=prometheus.yml`

2. Start Grafana (valid for MacOS)
`brew services start grafana`

3. Start server Go (just to produce metrics)
`go run server.go`
