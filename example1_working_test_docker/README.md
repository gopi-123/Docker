# Docker
Dockerize your Python Application



##  Install Docker from Ubuntu Repository
https://linuxconfig.org/how-to-install-docker-on-ubuntu-18-04-bionic-beaver



First, install Docker in Ubuntu:
$ sudo apt install docker.io 
$ sudo usermod -a -G docker $USER

Step1- Create Dockerfile
Create Dockerfile and Place the attached "Dockerfile" in the same PATH or location of your project folder(reinforceml)
Ex:  hello.py and Dockerfile should be in same folder.


Step2- Build and Run
Commands to build and run Docker image are as follows:
###  1) Build our Docker image (docker-example is an identifier name of our image)
$docker build . -t docker-example

### 2) run the built docker image
$docker run docker-example


Additional notes:
Incase to run dockerfile without cache following are the commands:
# add this below line into your docker file from the point you don't need caching, save it and execute  :
ARG CACHEBUST=1 

Commands to execute:
1) $docker build . -t docker-example --build-arg CACHEBUST=$(date +%s) 
2) $docker run docker-example
