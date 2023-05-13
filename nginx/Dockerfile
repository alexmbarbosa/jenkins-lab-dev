FROM nginx:latest AS nginx-lab
LABEL maintainer='alexmbarbosa'

RUN apt-get update -y && apt-get install -y \
    vim \
    curl \ 
    && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY ./files/nginx.conf /etc/nginx/nginx.conf
COPY ./files/jenkins.conf /etc/nginx/conf.d/jenkins.conf

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]