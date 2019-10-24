# docker_grafana

ref:
https://towardsdatascience.com/get-system-metrics-for-5-min-with-docker-telegraf-influxdb-and-grafana-97cfd957f0ac

https://hub.docker.com/_/telegraf

need to create the network and volumns before running docker compose up

server1$ docker network create monitoring
server1$ docker volume create grafana-volume
server1$ docker volume create influxdb-volume

# docker_grafana
