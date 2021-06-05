

1. cd to the directory where docker-composeCS.yml is located
2. docker-compose -f docker-composeCS.yml up
3. Check that the containers are up and running: docker ps 
4. To access TomcatSRV interactively: docker exec -it TomcatSRV /bin/bash
5. To access JenkinsSRV interactively: docker exec -it JenkinsSRV /bin/bash
6. Jenkins server is mapped to port 8085: http://localhost:8085/ (UI)
7. CS Web runs on a Tomcat server and mapped to port 8086:  http://localhost:8086/CSWeb/ or http://172.18.0.1:8086/CSWeb/ 

Mounted directories:
~/CSWebsite in the host machine is mounted to /var/jenkins_home/Website of the Jenkins container
~/CSWebsite in the host machine is mounted to /usr/local/tomcat/webapps/CSWeb of the Tomcat container