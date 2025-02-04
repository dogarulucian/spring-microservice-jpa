1.To download locally temurin jdk image(https://hub.docker.com/r/amd64/eclipse-temurin/tags?name=17) better to get it from tagname
docker pull amd64/eclipse-temurin:17-jdk-ubi9-minimal

2.Run maven jar plugin form IntellijIdea

3.Build the Docker Image
Use the following command to build the Docker image:


docker build -t springboot-microservice .

-t springboot-microservice: Assigns a tag (name) to your image.
. Specifies the current directory where the Dockerfile is located(aka current dir)


4.Run the Docker Container

docker run -p 8090:8090 springboot-microservice

-p 8090:8090: Maps port 8090 of the container to port 8090 on your host machine.
springboot-microservice: The name of the image you created.

5.Run the app : curl -X GET http://localhost:8090/users -v
