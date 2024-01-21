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
4. Configure the [Parameter Providers](./docs/parameter-providers/setup.md).
5. Configure the [Parameter Contexts](./docs/parameter-contexts/setup.md).
6. Configure the [Registry Clients](./docs/registry-clients/setup.md).
7. Import the [Demo Flows](./docs/import-demo-flows/setup.md).

# Considerations

## Parameters Directory

The [parameters directory](./parameters) in this project is intended to provide an example of being able to "hot-reload" parameter values. In a real scenario, this directory would not be committed to git (or you would at least not commit files with sensitive information).

# TODOs

## More Automated Setup

Some of the setup steps could in theory be automated, but I don't feel like doing that work currently.

- Parameter Providers
  - I'm pretty sure this can be automated, but I can't find an API doc for this part.

# Known Issues

This guide can't be used with `2.0.0-M1` because of [NIFI-12531](https://issues.apache.org/jira/browse/NIFI-12531). You must wait until `2.0.0-M2`, which contains the fix for this issue.
