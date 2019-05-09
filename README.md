# My Docker Cookbook

only to don´t forget

## Mongodb
```docker
docker run --name mongo -p 27017:27017 -d pedrualves/mongodb-mongohacker
```

## Oracledb 

```docker
docker pull deepdiver/docker-oracle-xe-11g
```

```docker
docker run -d -p 49160:22 -p 49161:1521 deepdiver/oracle-xe-11g
```

```docker
docker run -d -p 49161:1521 -p 8080:8080 -e ORACLE_ALLOW_REMOTE=true -e ORACLE_DISABLE_ASYNCH_IO=true -e ORACLE_ENABLE_XDB=true deepdiver/docker-oracle-xe-11g
```

```sql
CREATE USER mcp 
    IDENTIFIED BY mcp 
    DEFAULT TABLESPACE TS_MCPD_01 
    QUOTA 10M ON TS_MCPD_01 
    TEMPORARY TABLESPACE temp
    QUOTA 5M ON system;
```

## RabbitMQ

```docker
docker run -d --name rabbitmq --hostname rabbitmq -p 15672:15672 -p 5672:5672 -p 5671:5671 rabbitmq:3.7.14-management-alpine
```
