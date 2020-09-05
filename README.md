Sandbox repository to test three musketeers pattern with building docker images within a CI docker.

Building and pushing the image works fine on a local machine.

##Pre-requisites##
Following should be installed in your machine
- Docker
- Docker-compose
- Make

##Steps to build##
- Clone this repository
- Update .env file with your docker-hub credentials
- From the root of the repository
  - ```make build``` to build the app container
  - ```make push```  to push the container to docker-hub
  - ```make clean``` to clean everything including the .env file

##TODO##
  The ```.github/workflows/build-and-publish-actions.yaml``` contains some test Github Actions to build and push the image after each push to master.
  Build works fine though the push does not work as Github secrets token does not seems to be available for the CI container. Time to investigate :-)
