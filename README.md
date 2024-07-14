# Log capturing configuration for a Metabase, postgres, nginx setup
Rather than going back and forth between the the separate logs, I wanted to create an aggregator to view all of them in a single place.
As the logs are being generated, it's using Promtail to scrape each of them.
This is simply a baseline environment and no reason other reverse proxies and SQL engines couldn't be used in a similiar configuration.


## Table of Contents
* [Technologies Used](#technologies-used)
* [Screenshots](#screenshots)
* [Configuration](#configuration)
* [Room for Improvement](#room-for-improvement)


## Technologies Used
- Metabase
- Nginx
- Postgres
- Grafana
- Loki
- Promtail


## Screenshots
![alt text](https://github.com/FilmonK/metabase-capture/blob/master/readme_images/grafana1.png?raw=true)
![alt text](https://github.com/FilmonK/metabase-capture/blob/master/readme_images/grafana2.png?raw=true)

## Configuration
Once you've copied the entire folder structure locally, you may have or want to make some adjustments.
Loki folder:
You may have to make permissions adjustments similar to the following depending on existing permissions
  - mkdir -p ./loki/data/index
  - mkdir -p ./loki/data/cache
  - mkdir -p ./loki/data/chunks
  - mkdir -p ./loki/data/wal

  - sudo chown -R $USER:$USER ./loki/data
  - sudo chmod -R 755 ./loki/data

Metabase folder:
- .env folder to specify the environment variables, including your database configuration
- MB_DB_HOST=postgres ← this value must match the service name of the database within the main docker-compose.yml
- Dockerfile has a command to copy the log4j2.xml file, as well as set JAVA environment variables
- log4j2.xml file which can be adjusted to desired level of logging




## Room for Improvement
Room for improvement:

- SQL engine agnostic 

