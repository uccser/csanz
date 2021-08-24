# CSANZ Website

This repository stores a copy of the CSANZ website, initally created in 2014.
The existing HTML files are wrapped in a Nginx Docker container for serving from a Docker swarm.

## Development

Build the image and tag it as `csanz`:

```
docker build . -t csanz
```

Run the container locally:

```
docker run --rm -p 8080:8080 csanz
```

View the website in a web browser on port 8080.

## Deployment

The `docker-compose.yml` file contains basic settings for deploying to the UCCSER Docker Swarm.
The stack can be deployed with the following command:

```
docker stack deploy csanz
```
