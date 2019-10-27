# docker_grafana

ref:
https://towardsdatascience.com/get-system-metrics-for-5-min-with-docker-telegraf-influxdb-and-grafana-97cfd957f0ac

https://hub.docker.com/_/telegraf

need to create the network and volumns before running docker compose up

server1$ docker network create monitoring

server1$ docker volume create grafana-volume

server1$ docker volume create influxdb-volume

step 1
server1$ docker network create monitoring
server1$ docker volume create grafana-volume
server1$ docker volume create influxdb-volume

step 2 create telegra database to host the data
docker run --rm \
  -e INFLUXDB_DB=telegraf -e INFLUXDB_ADMIN_ENABLED=true \
  -e INFLUXDB_ADMIN_USER=admin \
  -e INFLUXDB_ADMIN_PASSWORD=supersecretpassword \
  -e INFLUXDB_USER=telegraf -e INFLUXDB_USER_PASSWORD=secretpassword \
  -v influxdb-volume:/var/lib/influxdb \
  influxdb /init-influxdb.sh

step3 run docker compose up


step4 configure grafana datasource




# docker_grafana
