# Default DevSpace Config Example
>How is the default setup?


### **The Basics**

The default DevSpace config sets up  a basic ubuntu environment with nothing else. There are comments for a config running redis and python to demonstrate to a user the format of the config.
It also allocates the maximum resources a free user is allowed to allocate.


```yaml
# version of configuration format
version: 0.1

# resources that need to be allocated for the env
resources:
  # we only deal in whole CPU cores don't pass milli core syntax
  cpu: 3
  # memory is measured in GB
  mem: 4
  # disk is measured in GB
  disk: 10

# base container that will operate as the OS
base_container: gigodev/gimg:base-ubuntu

# working directory that the source code will be cloned to
working_directory: /home/gigo/codebase/

# environment variables for the env
environment:
  GIGO_WORKSPACE: "true"

# configuration of the vscode editor
vscode:
  # enable/disable vscode editor - default to enabled
  enabled: true
  # extensions that need to be installed in the editor
#  extensions:
#    - ms-python.python

# containers that will be executed within the dev container - in docker compose format
#containers:
#  version: "3.2"
#  services:
#    redis:
#      image: "redis:alpine"
#      command: redis-server --requirepass password
#      ports:
#         - "6379:6379"
#      volumes:
#         - /home/gigo/.gigo/containers/redis-data:/var/lib/redis
#         - /home/gigo/.gigo/containers/redis.conf:/usr/local/etc/redis/redis.conf
#      environment:
#         - REDIS_REPLICATION_MODE=master
#      networks:
#         node_net:
#           ipv4_address: 172.28.1.4
#  networks:
#    node_net:
#      ipam:
#        driver: default
#        config:
#           - subnet: 172.28.0.0/16

# optional shell executions that are performed in order from top to bottom
#exec:
#  - name: Name of command
#   init: false # whether this should only be executed on initialization
#   command: |
#    #!/bin/bash
#    echo "hello world"
```

