# Open Hospital API [![Build Status](https://travis-ci.org/informatici/openhospital-api.svg?branch=master)](https://travis-ci.org/informatici/openhospital-api)

This is the API project of [Open Hospital][openhospital]: it exposes a REST API of the business logic implemented in the [openhospital-core project][core].  

## How to build [WIP]

For the moment, to build this project you should 

 1. fetch and build the `OP-102_master-refactoring-for-api` branch of the [core] project
    
        git clone https://github.com/informatici/openhospital-core.git --branch OP-102_master-refactoring-for-api
        cd openhospital-core
        mvn clean install -DskipTests=true
        
 2. clone and build this project
 
        git clone https://github.com/informatici/openhospital-api
        cd openhospital-api
        mvn clean install -DskipTests=true

 3. set rsc/database.properties
 
        DB can be created with `docker-compose up` from `openhospital-core` or using a dedicated MySQL server

 4. start openhospital-api
 
        java -jar openhospital-api-<version>.jar

Service available on localhost:8080

[openhospital]: https://www.open-hospital.org/
[core]: https://github.com/informatici/openhospital/openhospital-core
