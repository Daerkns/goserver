# GoServer

A small **HTTP server written in Go and containerized with Docker**, built as part of the [Boot.dev](https://www.boot.dev) Docker course.

## Features

- Built with Go's standard `net/http` package
- Simple HTTP request routing
- Configurable port through the `PORT` environment variable
- 30-second read and write timeouts
- Dockerized using a lightweight Debian Slim image

## Running Locally

Make sure Go is installed, then run:

```bash
go run .
```

The server listens on the port specified by the `PORT` environment variable.

For example:

```bash
PORT=8991 go run .
```

Then visit:

```text
http://localhost:8991
```

## Running with Docker

Build the Docker image:

```bash
docker build -t goserver .
```

Run the container:

```bash
docker run -p 8991:8991 goserver
```

The container is configured to use port `8991` by default.

## Project Structure

```text
goserver/
├── main.go       # HTTP server and request handling
├── goserver/     # Compiled server binary
├── Dockerfile    # Docker image configuration
├── go.mod        # Go module definition
└── README.md
```

A small project for practicing **Go HTTP servers, Docker images, and containerized applications**.
