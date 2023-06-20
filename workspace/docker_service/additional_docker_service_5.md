# Additional Docker Services
>What To Add To Configs


### **When To Add Additional Docker Services**

The workspace config provides an additional field for optional docker services that are not a part of the base image. This is useful for when a user needs to run any external service such as a database like [TiDB](https://hub.docker.com/r/pingcap/tidb) or data pipeline like [Kafka](https://hub.docker.com/r/bitnami/kafka/).
The `containers` field uses the [*docker-compose*](https://docs.docker.com/compose/compose-file/compose-file-v3/) format so that users may have some familiarity with creating specified containers.

The following is an example of using [Revel](https://revel.github.io/) and [PostgresSQL](https://www.postgresql.org/):
```yaml
containers:
  version: "3.2"
  services:
    postgres:
      image: "postgres:latest"
      networks:
        node_net:
          ipv4_address: 172.28.1.2
      environment:
        POSTGRES_USER: "revel"
        POSTGRES_PASSWORD: "revel"
        POSTGRES_DB: "revel_ecommerce"
  networks:
    node_net:
      ipam:
        driver: default
        config:
          - subnet: 172.28.0.0/16
```

![workspace_config_additional_docker_services.svg](https://raw.githubusercontent.com/Gage-Technologies/gigo-documentation/master/workspace/docker_service/workspace_config_additional_docker_services.svg)

The network section of the block determines what address to run the service on. In the example PostgresSQL is running on  172.28.1.2.  These optional parameters allow for a wide range of different uses and provide users with much more flexibility to run more advanced projects with larger dependencies.