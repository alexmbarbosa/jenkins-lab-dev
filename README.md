# jenkins-lab

Jenkins lab environment

### **What is this project for?**

This project enables spinning up a Jenkins lab for study through the docker containers.

### Requirements

- [Docker installed](https://docs.docker.com/engine/install/)
- [docker-compose](https://docs.docker.com.zh.xy2401.com/v17.12/compose/install/)

#### **What is included here?**

This project has the following resources:

- [Jenkins container](https://www.jenkins.io/doc/book/installing/docker/)
- [NGINX container](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-docker/)

#### **How to use this project?**

1. Clone this repository

```shell
git clone https://github.com/alexmbarbosa/jenkins-lab-dev.git
```

2. Create `.env` copying the `env_template` variables, changing according to your preferences:

- NGINX_HOST="<your_hostname>"
- NGINX_PORT=<your_nginx_port>

```shell
source .env
```

3. Build/run this docker environment

```shell
docker-compose up -d --build
```
