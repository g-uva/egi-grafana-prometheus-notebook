#### go-server-grafana-prometheus
Experimentation with Grafana + Prometheus using a quite simple Go server.

#### Steps to run the server
1. Start Prometheus using the configuration
`prometheus --config.file=prometheus.yml`

2. Start Grafana (valid for MacOS)
`brew services start grafana`

3. Start server Go (just to produce metrics)
`go run server.go`

---

#### Tutorial pre-writing (WIP)

- Current state of affairs 2025-03-04
	- [[2025-03-12 GreenDIGIT Meeting Yuri and Adnan]]

	- I am trying to access the external IPs of the services in Kubernetes, but something's wrong
	- [ ] **Publish the plugin:** I have to containerise the notebook as well? Or EGI's notebook and integrate the plugin there, install with by default with PyPi or pip.
	- [Asked prompt](https://chatgpt.com/c/67c6b423-4420-8002-aa65-9b94d6d8db14)
	- [ ] Pooling Prometheus and Grafana for updated metrics feedback

> Github repository 👉 https://github.com/g-uva/egi-grafana-prometheus-notebook
##### Setting Prometheus and Grafana as standalone
Main references:
- [Tutorial on Prometheus webpage](https://prometheus.io/docs/tutorials/visualizing_metrics_using_grafana/)
	1. [Step 01](https://prometheus.io/docs/tutorials/getting_started/): Setting up Prometheus globally and using `yml` file.
	2. [Step 02](https://prometheus.io/docs/tutorials/instrumenting_http_server_in_go/): Setting up Go server with `ping_request_number` service. 
	3. [Step 03](https://prometheus.io/docs/tutorials/visualizing_metrics_using_grafana/): Visualising metrics in Grafana + Grafana installation.
- [ ] Set containerised (Kubernetes) setting with Ansible for everything.

##### Installing Grafana dashboard/panel inside of a React application
- Main references
	- [Share dashboard and panels from Grafana's documentation](https://grafana.com/docs/grafana/latest/dashboards/share-dashboards-panels/)
		- `grafana.ini`: `allow_embeddding=true` — this is because by default 

##### Time-series DB: *for later*

##### Publishing the extension

##### Containerisation with Kubernetes
- [Prometheus server](docker pull prom/prometheus)
- [Grafana server](https://hub.docker.com/r/grafana/grafana)

##### Publishing extension from JupyterLab
- JupyterLab server (development)
	- [ ] Publishing the extension
		- [JupyterLab documentation to write an extension](https://jupyterlab.readthedocs.io/en/stable/extension/extension_tutorial.html#add-an-astronomy-picture-of-the-day-widget

##### Setting environment in Ansible
- I have already investigated the notebooks from the CZ company
- I have tried to set in AWS, but it was a bit tricky. Besides, I did not have enough credits 🥲

