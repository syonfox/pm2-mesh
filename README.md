[![npm](https://img.shields.io/npm/v/pm2-metrics.svg)](https://npmjs.com/package/pm2-metrics) 
[![NPM Downloads](https://img.shields.io/npm/dm/pm2-metrics.svg)](https://www.npmjs.com/package/pm2-metrics)
[![NPM](https://nodei.co/npm/pm2-metrics.png?downloads=true)](https://nodei.co/npm/pm2-metrics/)

# PM2 Metrics

#### Easy Install with PM2

```shell
pm2 install pm2-metrics
```

#### Or Clone and run endpoint version as a seperate application

```shell
    $ git clone https://github.com/syonfox/pm2-mesh.git
    $ npm install
    $ pm2 start exporter.js --name pm2-metrics
```

#### Open your browser

```shell
http://<HOST>:9209/metrics
```

#### For Prometheus Config

in `prometheus.yaml`
inside `scrape_configs` add this block:

```yml
- job_name: pm2-metrics
scrape_interval: 10s
scrape_timeout: 10s
metrics_path: /metrics
scheme: http
static_configs:
  - targets:
      - localhost:9209
```

#### Grafana dashboard [#1 (comment)](https://github.com/saikatharryc/pm2-prometheus-exporter/issues/1#issuecomment-499551831)

###### PR(s) & issue(s) are welcome

###### \*change host name from `localhost` on basics where you are hosting

###### Modified & Working Version from [pm2-prometheus-exporter by @burningtree](https://github.com/burningtree/pm2-prometheus-exporter)
