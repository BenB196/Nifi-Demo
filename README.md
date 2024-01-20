# Nifi-Demo
Demo project showcasing Nifi functionality with various systems.

# Prerequisites

- Docker
- Docker Compose
- git

# Usage

1. Clone this repository
2. Run `docker-compose up -d` in this project's root directory
    - Need to run this command in the project's root directory because we leverage relative paths.
3. Wait for the components to become available
    - Nifi: https://localhost:8443/nifi
      - Username: user
      - Password: password1234
    - Nifi Registry: http://localhost:18080/nifi-registry/
    - Elasticsearch: https://localhost:9200
      - Username: elastic
      - Password: changeme
    - Kibana: http://localhost:5601
      - Same as Elasticsearch
