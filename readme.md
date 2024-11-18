# Monitoring Spring Boot Applications with Prometheus and Grafana, Zipkin

This small demo project contains an example setup of Prometheus and Grafana to monitor Spring Boot applications.

The project contains a default Grafana Prometheus datasource and scrapes the Spring Boot project and Prometheus server 
for monitoring information.

If you want to login to Grafana you can use the `admin / password` combination.

For monitoring Spring Boot applications I highly recommend the [JVM Micrometer dashboard](https://grafana.com/dashboards/4701) created by [Michael Weirauch](https://twitter.com/emwexx).

## Building the project

First build the spring boot application.

```bash
mvn clean package
```

Now when the application has been build we can start running our services by running:

```bash
docker-compose up -d
```

After all services have started successfully, you can navigate to the following urls:

- Spring Boot app - http://localhost:8080/
- Prometheus      - http://localhost:9090/ , http://localhost:9090/targets 
- Grafana         - http://localhost:3000/, 
- Zipkin		  - http://localhost:9411/zipkin/dependency , http://localhost:3000/explore 



 docker-compose -p consul-cluster  -f concsul-docker-compose.yml down
 docker-compose -p consul-cluster  -f consul-docker-compose.yml up -d --remove-orphans



docker-compose -p cloud-observability down
docker-compose -p consul-cluster  -f consul-docker-compose.yml up -d --remove-orphans


