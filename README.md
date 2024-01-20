# Nifi-Demo
Demo project showcasing Nifi functionality with various systems.

# :warning: Warning :warning:

This project is strictly for demonstrative purposes, it should not be used in production (or referenced for a production setup, there are security issues with this setup).

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

# Considerations

## Parameters Directory

The [parameters directory](./parameters) in this project is intended to provide an example of being able to "hot-reload" parameter values. In a real scenario, this directory would not be committed to git (or you would at least not commit files with sensitive information).
