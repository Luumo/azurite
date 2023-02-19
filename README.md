# Azure Storage Azurite Docker Compose

This Docker Compose file sets up a container running Azurite, a lightweight server that provides a local emulation of the Azure Blob, Queue, and Table services for development and testing purposes. The container is configured to expose ports 10000, 10001, and 10002 for accessing the different storage services.

## Prerequisites

To use this Docker Compose file, you'll need the following:

- Docker and Docker Compose installed on your system
- Basic familiarity with Docker and Docker Compose

## Usage

To use this Docker Compose file, follow these steps:

1. Download the `docker-compose.yml` file to your local system.

2. Open a terminal window and navigate to the directory where the `docker-compose.yml` file is located.

3. Run the following command to start the container:

```
docker-compose up -d
```


This command will start the container in detached mode and run it in the background. The container will be accessible at the following endpoints:

- Azurite Blob service: `http://localhost:10000`
- Azurite Queue service: `http://localhost:10001`
- Azurite Table service: `http://localhost:10002`

4. To stop the container, run the following command:

```
docker-compose down
```

5. The container is 

## Configuration
This Docker Compose file uses the following configuration:

- The azurite service, which runs the Azurite container.
- The `dev_default` network, which is a bridge network used by the azurite container for communication with other containers.

By default, the `dev_default` network uses the `bridge` driver, which is the default driver in Docker and suitable for most use cases. If you already have a network with the name dev_default and different settings than what is specified in the YAML file, you may need to modify the YAML file to use the existing network.

## Troubleshooting
If you encounter any issues with the container or the YAML file, try the following:

- Check that Docker and Docker Compose are installed and configured correctly on your system.
- Check the Docker logs for the container using the following command:

## Microsoft documentation
https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azurite