# Guacamole with Docker

This repository contains a Docker Compose script that will setup Guacamole with a reverse proxy configured for TLS.

# Setup Steps

## Clone Repository

```
$ git clone https://github.com/iamaleks/Guacamole-With-Docker.git
$ cd cd Guacamole-With-Docker/
```

## Add new TLS certificate (this command will generate a self signed certificate, you can add your own)

```
$ openssl req -new -newkey rsa:2048 -x509 -sha256 -days 365 -nodes -out files/reverseproxy/ssl/server.crt -keyout files/reverseproxy/ssl/server.key
```

## Run Docker Compose Setup

```
$ sudo docker-compose up -d
```

After browse to the IP address of your server or the domain that resolves to it and login using the following credentials:
- username: guacadmin
- pasword: guacadmin
