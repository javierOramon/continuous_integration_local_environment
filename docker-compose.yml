---
version: '3'

services:
 nexus:
    container_name: nexus_ci
    image: javieroramon/nexus_ci:latest
    ports:
    - 8081:8081
 sonarqube:
    container_name: sonar_ci
    image: javieroramon/sonar_ci:latest
    ports:
    - 9000:9000
 jenkins:
    container_name: jenkins_ci
    image: javieroramon/jenkins_ci:latest
    ports:
    - 49001:8080
 gitlab:
    container_name: gitlab_ci
    image: javieroramon/gitlab_ci:latest
    hostname: 172.17.0.1
    restart: always
    volumes:
      - /srv/gitlab/config:/etc/gitlab
      - /srv/gitlab/logs:/var/log/gitlab
      - /srv/gitlab/data:/var/opt/gitlab
    ports:
    - 444:443 
    - 81:80 
    - 23:22 
 gitlab-runner:
    container_name: gitlab-runner_ci
    image: javieroramon/gitlab_runner_ci:latest
    restart: always
    volumes:
     - /srv/gitlab-runner/config:/etc/gitlab-runner 
     - /var/run/docker.sock:/var/run/docker.sock
