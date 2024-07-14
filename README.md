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
![alt text](https://github.com/FilmonK/leasingm/blob/master/readme_images/grafana1.png?raw=true)
![alt text](https://github.com/FilmonK/leasingm/blob/master/readme_images/grafana2.png?raw=true)


## Room for Improvement
Room for improvement:

- SQL engine agnostic 

