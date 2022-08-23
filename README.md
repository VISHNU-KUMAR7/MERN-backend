# MERN-backend
This is demo project for checking the back-end with devops. This is first project which is integrated with devops after completing the theoretical knowledge.

1. Create EC2 instance

2. update the Ec2 
 sudo yum update
 
3. change the hostname:
  sudo vi /etc/hostname
 
4. Create the user for jenkins 
  sudo useradd jenkins
  sudo passwd jenkins

5. Give all permission to <jenkins user>
  sudo visudo
  
6. login as jenkins user
  sudo su jenkins

7. install docker
  sudo yum install docker -y
  
8. check the docker service
  sudo service docker status
 
9. Start the docker service
  sudo service docker start
  
10. check the images in the docker
  sudo docker ps
  (will get permission denied error)
  
11. over come the permission denied error
  usermod -aG docker jenkins ( note:- as a root )

12. Check the images again in jenkins user 
  docker ps  ( permission denied error removed)

13. pull jenkins docker image 
   docker pull jenkins/jenkins

14. Check the jenkins image 
  docker images (note: you can see like this jenkins/jenkins   latest    0a215df0bcfa   6 days ago   463MB)
  
15. Run the image as a container
   docker run -p 8080:8080 --name=jenkins-master jenkins/jenkins  ( note : it will run but u will not able to do anythings in terminal)
   
16. Remove the above container and run again image of jenins
  docker run -p 8080:8080 --name=jenkins-master -d jenkins/jenkins
  
 17. Check the <localhost>:8080 u need unlock key
  docker logs <conatinerId>
  
18. All the steps need for the jenkins...

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
