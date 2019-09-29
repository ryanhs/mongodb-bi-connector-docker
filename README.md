# Mongodb BI Connector

this docker image for mongodb-bi-connector.

## Security / Auth

This bi-connector assume that your mongodb server can connect without any authentication (trusted network).
"*Authentication in MongoDB is fairly complex*". Thats the reason to make this bi-connector is simple as possible for now.

## docker-compose example

```
version: "3"
services:
  mongodb:
    image: mongo:bionic
  
  mongodb-bi-connector:
    image: ryanhs/mongodb-bi-connector
    environment:
      MONGO_HOST: mongodb
      MONGO_PORT: 27017  

```
