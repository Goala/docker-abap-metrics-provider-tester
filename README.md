# docker-influxdb-telegraf-grafana-stack-4-sap-netweaver

## influxdb utils

curl -G http://localhost:8086/query?pretty=true --data-urlencode "db=glances" --data-urlencode "q=SHOW DATABASES"
curl -XPOST 'http://localhost:8086/query' --data-urlencode 'q=CREATE DATABASE influxdb'
curl -G http://localhost:8086/query?pretty=true --data-urlencode "db=influxdb" --data-urlencode "q=SHOW MEASUREMENTS"
curl -G 'http://localhost:8086/query' --data-urlencode 'q=select * from influxdb..http'

## telegraf utils

telegraf --config telegraf.conf --test

## based on 
https://github.com/bcremer/docker-telegraf-influx-grafana-stack

https://github.com/nicolargo/docker-influxdb-grafana
