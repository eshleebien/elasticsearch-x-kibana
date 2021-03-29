### Elasticsearch and Kibana demo
This is for Elasticsearch and Kibana for observability training.

#### Requirements
 - docker
 - docker-compose

#### Run Elasticsearch and Kibana
```
$ git clone https://github.com/eshleebien/elasticsearch-x-kibana
$ cd elasticsearch-x-kibana
$ docker-compose up 
```

This creates Elasticsearch and Kibana containers and reachable on http://localhost:9200 and http://localhost:5601.


#### Run sample app, proxy, metricbeat and filebeat
Change the HOST_IP to you machine's IP address in `apps/.env` file

```
$ cd apps
$ docker-compose up
```

This creates an echo app, nginx proxy, Metricbeat and Filebeat. Echo app is reachable via proxy on http://localhost:8080/echoapp (echo).
It also creates a container with siege for load testing
