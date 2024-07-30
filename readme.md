# API Gateway

This repository contains the configuration and setup for the API Gateway that routes and manages requests to various microservices in TourHub.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Gateway](#running-the-gateway)
- [Endpoints](#endpoints)
- [Logging and Monitoring](#logging-and-monitoring)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The API Gateway acts as a single entry point for multiple microservices, providing routing, security, and other cross-cutting concerns. This setup uses Express Gateway to manage requests to the Accommodations and Activities services.

## Prerequisites

- Node.js and npm installed
- Express Gateway installed globally

## Installation

1. Clone the repository.
2. Navigate to the project directory.
3. Install the dependencies.

## Configuration

The gateway configuration is defined in the `gateway.config.yml` file. This includes:

- `http` and `admin` ports
- `apiEndpoints` for defining the paths and hosts for various services
- `serviceEndpoints` for mapping services to their respective URLs
- `policies` for managing common middleware functions like CORS, logging, and rate limiting
- `pipelines` for defining the routing and policy application for each service

## Running the Gateway

To start the API Gateway, use the following command:

- Start the gateway usin `npm start`.

Ensure the microservices (Accommodations, Activities, etc.) are running on their respective ports as specified in the `serviceEndpoints` section of the configuration.

## Endpoints

The API Gateway routes requests to the following endpoints:

#### Routes to the Accommodations service

- `/accommodations/*`
- `/amenities/*`
- `/accommodation-types/*`

#### Routes to the Activities service

- `/activity-types/*`
- `/activities/*`

Refer to the `gateway.config.yml` for more detailed endpoint configurations.

## Logging and Monitoring

The API Gateway includes logging policies to capture and log requests. Logs can be viewed in the terminal where the gateway is running. For more advanced monitoring, consider integrating with logging and monitoring tools.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the MIT License.
