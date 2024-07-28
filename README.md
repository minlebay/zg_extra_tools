Docker Monitoring Stack

This repository contains a Docker Compose configuration for setting up a monitoring stack using Elasticsearch, Logstash, Kibana, Prometheus, and Grafana. The stack provides a comprehensive solution for log management, monitoring, and visualization.
Components

    Elasticsearch: A search and analytics engine used for storing and searching log data.
    Logstash: A data processing pipeline that ingests, transforms, and sends data to Elasticsearch.
    Kibana: A data visualization tool for exploring and visualizing data stored in Elasticsearch.
    Prometheus: A monitoring system and time series database for collecting metrics and alerts.
    Grafana: A visualization and analytics platform for monitoring data from Prometheus.

Prerequisites

    Docker
    Docker Compose

Getting Started

    Clone the Repository

    bash

git clone https://github.com/your-username/your-repo.git
cd your-repo

Update Configuration Files

    Logstash: Update the Logstash pipeline configuration in ./logstash/pipeline as needed.
    Prometheus: Update the Prometheus configuration in prometheus.yml according to your requirements.

Start the Stack

Run the following command to start the services:

``` shell
    docker-compose up
```
This will start Elasticsearch, Logstash, Kibana, Prometheus, and Grafana.

    Access the Services
        Elasticsearch: http://localhost:9200
        Kibana: http://localhost:5601
        Logstash: Listening on port 5000
        Prometheus: http://localhost:9089
        Grafana: http://localhost:3000

    Default credentials for Grafana:
        Username: admin
        Password: admin

Volumes

    prometheus_data: Stores Prometheus data.
    esdata1: Stores Elasticsearch data.

Networking

All services are connected to a custom network local-net for inter-service communication.
Notes

    Make sure to adapt the configuration files to match your specific use case.
    For more information on each component, refer to their respective documentation:
        Elasticsearch
        Logstash
        Kibana
        Prometheus
        Grafana

License

This project is licensed under the MIT License. See the LICENSE file for details.