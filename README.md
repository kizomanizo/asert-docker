# AserT Docker

AserT Docker is a tool designed to simplify the deployment of the AserT system within a Docker environment, specifically tailored for MNRT. This guide will help you get started quickly with deployment and configuration.

## Features

- **Easy Deployment**: Quick setup and management of AserT using Docker.
- **Consistent Environment**: Isolated Docker containers for a predictable AserT environment.
- **Optimized for MNRT**: Tailored configuration for MNRT systems.
- **Flexible**: Configure and extend the container to meet your specific needs.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/) (if needed)

## Installation

1. Clone the repository:

```
mkdir asert && git clone https://github.com/yourusername/asert-docker.git asert
cd asert
```

2. Build the containers using Docker Compose:

```
docker compose build
```

3. Start the services in detached mode:

```
docker compose up -d
```

4. Alternatively, to build and start everything in one command:

```
docker compose up -d --build
```

This setup runs several services:

- asert-api (backend)
- asert-db (Postgres database)
- asert-rabbitmq (messaging)
- asert-pgadmin (PG Admin)

Refer to the provided docker-compose.yml for configuration details.

### Environment Variables

Configure environment variables to customize your setup. Copy the environment file example.env and paste the contents in a new file called `.env` then customize your variables therein.

### Logs and Troubleshooting

View container logs:

```
docker compose logs -f
```

For troubleshooting, check your Docker daemon logs or run the container in interactive mode:

```
docker exec -it asert-<container-name> bash
```

## Contributing

Contributions, bug reports, and feature requests are welcome. Please submit them via the GitHub issues or pull requests.

## License

Licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For support or inquiries, please open an issue on GitHub or contact the repository maintainer.

Happy Dockering!

## Author

Kizito S.M.
