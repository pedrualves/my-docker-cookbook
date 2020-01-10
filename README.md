# My Docker Cookbook

DON'T FORGET

## WSO2

```docker
docker run -it \
-p 9443:9443 \
-p 8243:8243 \
-p 8280:8280 \
wso2/wso2am

Publisher - https://localhost:9443/publisher
Store - https://localhost:9443/store
Admin console - https://localhost:9443/admin
Carbon console - https://localhost:9443/carbon

https://localhost:8243
http://localhost:8280

docker pull wso2/wso2am:2.6.0

docker run -it -p 8280:8280 -p 8243:8243 -p 9443:9443 --name api-manager wso2/wso2am:2.6.0
```

## Mongodb
```docker
docker run --name mongo -p 27017:27017 -d pedrualves/mongodb-mongohacker
```

## Oracledb 

```docker
docker pull deepdiver/docker-oracle-xe-11g
```

```docker
docker run -d -p 49160:22 -p 49161:1521 deepdiver/docker-oracle-xe-11g
```

```docker
docker run -d -p 49161:1521 -p 8080:8080 -e ORACLE_ALLOW_REMOTE=true -e ORACLE_DISABLE_ASYNCH_IO=true -e ORACLE_ENABLE_XDB=true deepdiver/docker-oracle-xe-11g
```
### How to create new user
```sql
CREATE USER user 
    IDENTIFIED BY password 
    DEFAULT TABLESPACE tablespace_name 
    QUOTA 10M ON tablespace_name 
    TEMPORARY TABLESPACE temp
    QUOTA 5M ON system;
```

## RabbitMQ

```docker
docker run -d --name rabbitmq --hostname rabbitmq -p 15672:15672 -p 5672:5672 -p 5671:5671 rabbitmq:3.7.14-management-alpine
```
