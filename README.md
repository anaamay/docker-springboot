# docker-springboot

Step-1: Check the docker is installed in you machine. run below commands and it will display the installed docker version.
  docker -v
Docker version 19.03.3, build a872fc2f86

Step-2: If docker is inastalled in your mahchine, please  go to the project home directory and run the below commands to 
build a docker image.
sudo docker build -f Dockerfile -t docker-springboot-app .

Step-3: After successfully execution of below comands a docker image will be created.
sudo docker build -f Dockerfile -t docker-springboot-app .

Step-4: Check the image has been created successfully. In case of this example the image will "docker-springboot-app" display
after executing the below command.
sudo docker images 

Step-5: Run the below command to run the docker image.
sudo docker run -p 8080:8080 docker-springboot-app 


Step-6: Here 8080 is the port what is defined in springboot property file. Now check the application will come up on below url:
http://localhost:8080/welcome/docker/hello

--------------------------------------- 

******************Pushing an image in docker repository

Step-1: Run the below command to build an image in the current directory
sudo docker build -t anaamay/docker-springboot-app:latest .

Step-2: Login to the docker account by using your credentials(In case you don't have a docker account kindly create one)
  sudo docker login  -u <username> -p <password>
  
Step-3: Push an image an to docker repositiry
sudo docker push anaamay/docker-springboot-app:latest

Now you will see the image has been placed to your docker repository
Step-4:to check the recently poushed image in your docker repository please check by using below command
sudo docker image ls
REPOSITORY                                      TAG                 IMAGE ID            CREATED             SIZE
anaamay/docker-springboot-app                   latest              3f1449bc3708        15 minutes ago      488MB

-------------Thank You----------------------  
  
