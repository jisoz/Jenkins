# Jenkins
docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts

docker ps 
docker run -it ...  /bin/bash
 cd /var/jenkins_home/secrets/
 cat initialAdminPassword 
 

 # to inspect info about where is the mouted folder where data is stored use :
  docker volume inspect jenkins_home


  # manage docker agent 
  docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home  -v /var/run/docker.sock:/var/run/docker.sock -u root  --privileged=true jenkins/jenkins:lts

  => go manage jenkins => clouds =>new cloud    in docker host uri put unix:///var/run/docker.sock => test connection 


# building maven application (java) with jenkins ci/cd  practice :

 go to new item => freestyle project => (name it )

now we will configure the pipeline : 
source code managemenet : git => repo url :https://github.com/anshulc55/Jenkins_Upgradev3.git (maven project from a public repo )

