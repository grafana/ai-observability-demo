# AI Observability Demo

This repository contains a demo application that showcases AI observability using OpenLIT, OpenAI, and ChromaDB. The application makes API calls to OpenAI and performs vector database operations while being monitored by OpenLIT.

## What This Demo Shows

This demo application demonstrates:

1. Integration with OpenAI's API (GPT-3.5-turbo and GPT-4)
2. Vector database operations using ChromaDB
3. AI observability using OpenLIT
4. Telemetry collection and visualization with Grafana Cloud

## Deployment Options

Choose your preferred deployment method:

1. [Docker Compose](docker/README.md) - For local development and testing
2. [Kubernetes](kubernetes/README.md) - For production deployments

## Prerequisites

- Access to OpenAI API
- Access to Grafana Cloud (for observability)
- Choose your deployment method:
  - For Docker: Docker and Docker Compose
  - For Kubernetes: Kubernetes cluster and kubectl

## Application Details

The demo application performs the following operations in a loop:

1. Makes an OpenAI API call to GPT-3.5-turbo to generate a short story
2. Makes an OpenAI API call to GPT-4 to get information about Grafana
3. Performs vector database operations using ChromaDB:
   - Adds documents to the collection
   - Queries the collection
   - Deletes documents from the collection

The application runs these operations every hour (3600 seconds) and is instrumented with OpenLIT for observability.

## Monitoring

The application sends telemetry data to Grafana Cloud. You can monitor:
- API call latencies
- Token usage
- Vector database operations
- Error rates
- And more...

## Security Notes

- Never commit your actual API keys or secrets to version control
- Always use appropriate security measures for your chosen deployment method
- Regularly rotate your API keys and secrets
- Follow the security best practices in the respective deployment guides

## Contributing

Feel free to submit issues and enhancement requests! 
