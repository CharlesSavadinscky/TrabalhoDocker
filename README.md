# Docker-NodeAplication
Create an docker container which contains a web application using docker compose to display number of times the server has been visited.

First create the index.js, the javascript file to:
-display the message "Number of visits"' in the web browser 
-to specify the port listening to(8080)
-to specify the client
-to increase the number of visits for every server request


and package .json file to specify the dependencies and scripts  

-Next build the node-app image from the dockerfile.
command: docker build -t adarsha/node-app .


And Run the redis server directly
command: docker run redis

Now to setup the link between two containers, node-app and redis use docker-compose.
Create docker-compose.yml file and declare  version to be used, services used, how to build the image and specify the ort on local machine and the container as well.

Use the followimg command to start the docker-comppose file which sets up everything.
command: docker-compose up

*to rebuild the images listed inside the docker-compose
command: docker-compose up --build

*to close multipple containers from dockerompose
command: docker-compose down
