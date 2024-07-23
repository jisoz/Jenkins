# Jenkins
docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts

docker ps 
docker run -it ...  /bin/bash
 cd /var/jenkins_home/secrets/
 cat initialAdminPassword 
 