# Docker Commands

```bash
# To Pull the image
docker pull ibmcom/mq:latest

# List docker images
docker images

# Docker create volume
docker volume create qmldata

# List Docker volumes 
docker volume ls

# Docker run (creating the container)
docker run --env LICENSE=accept --env MQ_QMGR_NAME=QM1 --volume qmldata:/mnt/mqm --publish 1414:1414 --publish 9443:9443 --detach --env MQ_APP_PASSWORD=Sam12345 ibmcom/mq:latest

# --publish internal-port:to-external-port (9443:9443)
# --detach (means run in the background)

# List Docker running containers
docker ps

# Go into docker container
docker exec -it 6b8 bash
# -it means interactive mode


```