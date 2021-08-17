*Prerequisites*
- Install Docker and download Jenkins & Tomcat images 
- Create the web-data directory (~/CSWebsite specifically in this example) on the local machine
- Place the .war file in it  (make sure to unzip it by a batch command in the Jenkins Job)

Steps

1. cd to docker-composeCS.yml file directory location
2. docker-compose -f docker-composeCS.yml up
3. Check that the containers are up and running: docker ps 
4. To access TomcatSRV interactively: docker exec -it TomcatSRV /bin/bash
5. To access JenkinsSRV interactively: docker exec -it JenkinsSRV /bin/bash
6. Jenkins server is mapped to port 8085: http://localhost:8085/ (UI)
7. CS Web runs on a Tomcat server and mapped to port 8086:  http://localhost:8086/CSWeb/ or http://<IP_add>:8086/CSWeb/ 

Mounted directories:
Directory ~/CSWebsite in the host machine should be mouted to /var/jenkins_home/Website in the Jenkins container
Directory ~/CSWebsite in the host machine should be mouted to /usr/local/tomcat/webapps/CSWeb in the Tomcat container

