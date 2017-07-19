
Services

 * Gitlab: port 81
 * Jenkins: port 49001. You should config the environment
 * Sonarqube: port 9000
 * Nexus: port 8081. url 8081/nexus

 Command to up:
 
 docker-compose up
 
 docker-compose up -d (without logs)
 
 If you have problems to up all machines maybe is because you don't have enough RAM, therefore, you should remove the services 
 that you are not going to use.
 
 Review the logs you could have problems with the permissions with the volumes.