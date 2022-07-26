# Intro

Build a new file docker file: docker build .

## Images and containers

Remove an image: docker image rm -f IMAGE_ID
Build a named file: docker build -t image_name .
Run an image in detached mode: docker run -p 5000:5000 -d --name container_name image_name
List all active containers: docker ps
List all active images: docker image ls
Stop a docker iamge: docker stop container_id

## Interacting with docker container

run interactive linux shell: docker exec -it container_name bash
exit out of interactive linux shell: exit

## Rebuild a container

1. docker rm container_to_replace_name -f

2. rebuild the base image: docker build -t base_image_name .

3. run the new image in detached mode: docker run -p 5000:5000 -d --name container_name image_name

## Using bind mounts

1. remove previous container if it does not use bind mount

2. Run an image in detached mode: docker run -v pathtofolderonlocalmachine:pathtofolderoncontainer -p 5000:5000 -d --name container_name image_name

pwd: windows command prompt: %cd%, windows powershell: ${pwd}
