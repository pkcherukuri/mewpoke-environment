# MEWPOKE-ENVIRONMENT - Docker

Provide a docker environment to run mewpoke and get stats on grafana dashboard

<p align="center">
  <img src="./img/architecture.jpg" alt="logo"/>
</p>

### Pre-requisites

- Install docker and docker-compose

### Included
- Couchbase: deploy cluster listening on port 8091 (login: Administrator / password)
- Mewpoke: deploy instances listening on port 8080, 8081, 8082 
- Prometheus: deploy instance / rules on port 9090
- Grafana: deploy grafana with prometheus datasource, and mewpoke dashboard (login: admin / secret)

### Run
At the top level of the repo run:
```sh
docker-compose up -d grafana
```

then connect to:
http://localhost:3000 and look at "Mewpoke Couchbase" dashboard
<p align="center">
  <img src="./img/mewpoke_grafana_dashboard.png" alt="logo"/>
</p>

