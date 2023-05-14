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

---
#### **How to use this project?**

1. Clone this repository.

```shell
git clone https://github.com/alexmbarbosa/jenkins-lab-dev.git
```

#### **Project Structure**

```shell
.
├── docker-compose.yml
├── jenkins
│   └── Dockerfile
└── nginx
    ├── Dockerfile
    └── files
        ├── conf.d
        │   ├── default.conf
        │   └── jenkins.conf
        └── nginx.conf
```

2. In virtualhost file `jenkins.conf`, change the server_name to your preference name:

```conf
server_name jenkins.local;
```

> **Note:** *Make sure you have this hostname in your `/etc/hosts`*.

3. Build/run this docker environment.

```shell
docker-compose up -d --build
```

```shell
docker-compose ps

NAME                IMAGE                                              COMMAND                  SERVICE             CREATED             STATUS              PORTS
jenkins-lab         docker.io/library/jenkins-lab-dev-jenkins:latest   ""                       jenkins             47 seconds ago      Up 46 seconds       8080/tcp, 50000/tcp
nginx-lab           docker.io/library/jenkins-lab-dev-nginx:latest     "nginx -g daemon off;"   nginx               47 seconds ago      Up 46 seconds       80/tcp
```

___

