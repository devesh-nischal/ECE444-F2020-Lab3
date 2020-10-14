# ECE444-F2020-Lab4&5
To run the application through Docker, follow these steps:  
Step 1:  
Make sure docker is installed on your workstation. If it is not, follow the tutorial here: https://docs.docker.com/get-started/  
  
Step 2:  
In the root directory of this repository, run the docker build command: "docker build -t <insert_image_name_here>:latest ."  
Replace <insert_image_name_here> with whatever you want your docker image of this application to be called.  
This command will build a new image with the preferred name. You can check that an image is created by running the "docker image ls" command.  
![Docker_Image](https://github.com/devesh-nischal/ECE444-F2020-Lab3/blob/lab4_Microservice_Experiment/Docker_Image.JPG?raw=true)  
  
Step 3:  
Call the docker run command on your newly built image. After succussfull start up, you can also run the "docker ps -a" command to make sure that the image is running and to determine if its running on the proper port. Refer to the screenshot below to see how to run and check a docker container.  
![Docker_Run_Command](https://github.com/devesh-nischal/ECE444-F2020-Lab3/blob/lab4_Microservice_Experiment/Docker_Run_Command.JPG?raw=true)  
  
If you check the logs of the container (either through the docker desktop application or through the terminal) you should see the flask application start up.  
![Docker_Run_Log](https://github.com/devesh-nischal/ECE444-F2020-Lab3/blob/lab4_Microservice_Experiment/Docker_Run_Log.JPG?raw=true)  
  
Step 4:  
Go to localhost:5000 on your workstation and the application should render.  
![Docker_Webpage](https://github.com/devesh-nischal/ECE444-F2020-Lab3/blob/lab4_Microservice_Experiment/Docker_Webpage.JPG?raw=true)  
  
Alternate Step 2:  
Since there is a docker-compose.yml file also included in the root directory of this repository, you may also run the following command "docker-compose up"  
This commmand will build the the docker image and start the container right after if there are no errors.  
  
There are 3 files associated with Docker in this branch and are all located in the root directory:  
1. Dockerfile: Responsible for telling docker what to install and run in this image  
2. requirements.txt: Text file used by Dockerfile to install all neccessary dependencies to run the application.  
3. docker-compose.yml: This files allows the user to  build and run the application using just one command.  
  
  
  
  
The difference between Docker and Virtual Machines:  
A docker container shared the kernel of the computer it is running on with other containers. It runs natively on Linux and is very lightweight. This makes containers no bigger than normal executable files.  
A virtual machine on the other hand includes a guest operating system with virtual access to the machine's physical resources. This forces virtual machines to have tremendous amounts of overhead as compared to containers.
