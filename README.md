# Nginx Reverse Proxy with Multiple Domains

This project sets up a Docker Compose environment with three Nginx containers:
- A reverse proxy (`nginx-proxy`) that routes requests based on domain names.
- Two web servers (`nginx-web1` and `nginx-web2`) serving distinct HTML files.

## Prerequisites

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- Modify your `/etc/hosts` file to simulate the domains:

```plaintext
127.0.0.1   domain1.local
127.0.0.1   domain2.local
```

## Directory Structure

```plaintext
project-directory/
├── docker-compose.yml
├── web1/
│   └── index.html
├── web2/
│   └── index.html
└── proxy/
    └── nginx.conf
```

## Getting Started

Clone the repository and navigate to the project directory.
Ensure the directory structure and files (index.html and nginx.conf) are in place.
Start the services with Docker Compose:

```bash
docker-compose up -d
```
Access the simulated domains in your browser:
  - [http://domain1.local](http://domain1.local) (served by nginx-web1)
  - [http://domain2.local](http://domain2.local) (served by nginx-web2)

## Configuration

Reverse Proxy Configuration: Defined in proxy/nginx.conf.
Web Server HTML Files: Located in web1/index.html and web2/index.html.
