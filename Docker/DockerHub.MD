#What is Docker Hub Registry

Docker Hub is a cloud-based registry service which allows you to link to code repositories, build your images and test them, stores manually pushed images, and links to Docker Cloud so you can deploy images to your hosts. It provides a centralized resource for container image discovery, distribution and change management, user and team collaboration, and workflow automation throughout the development pipeline.
Ref URL : https://docs.docker.com/docker-hub/

    Create a docker hub account in https://hub.docker.com/

    Pull a docker image

    docker pull ubuntu

    pull a docker image with the old version

    docker pull ubuntu:16.04

    create a custom tag to the docker image

    docker tag ubuntu:latest valaxy/ubuntu:demo

    login to your docker hub registry

    docker login
    docker push valaxy/ubuntu:demo

#testing

    Remove all images in docker server

    docker image rm -f <Image_id>

    Pull your custom image from your docker account

    docker pull valaxy/ubuntu:demo

