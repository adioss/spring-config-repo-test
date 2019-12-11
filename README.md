# Spring config server simple test
* start a server (http://localhost:8888 root/password)
* deliver yaml configuration files located in root folder (naming convention is important)   

# How to use in client
* remote_config.yml accessible with: http://localhost:8888/remote_config/application.yml
* remote_config_other.yml accessible with: http://localhost:8888/remote_config_other/application.yml
* example of config file (to use http://localhost:8888/remote_config/application.yml):
```
spring:
  application:
    name: remote_config
  cloud:
    config:
      uri: http://localhost:8888/
      username: root
      password: password
```

