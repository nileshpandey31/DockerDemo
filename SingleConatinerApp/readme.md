# Getting Started with Docker

This guide will walk you through the steps to get started with Docker and run a simple Pizza order app using jQuery.

## Installation

If you're using a Windows machine, you can download VirtualBox and start with an Ubuntu virtual machine. Then follow the steps below to install Docker Engine:

1. Install Docker Engine by referring to the official documentation for multiple installation options: [Docker Installation Guide for Ubuntu](https://docs.docker.com/engine/install/ubuntu/)
   
   You can install using the convenience script by running:
   
   curl -fsSL https://get.docker.com -o get-docker.sh
   sudo sh ./get-docker.sh

# Running the Simple jQuery App

## Simple Pizza Order App using jQuery

1. Pull the Nginx image from the Docker Hub registry:

   **docker pull nginx**

2. Build a custom image of our application using the provided Dockerfile:

   **docker build . -t sampleimage**
   _Here, -t flag gives a name to our Docker image._

3. Verify that the image is created by running:

   **docker images**

4. Run a container:

   **docker run --name instance1 -d -p 8080:80 sampleimage**
   _Here, -d means running the instance in the background. We're mapping port 80 of the Docker instance to port 8080 of the host (localhost in this case)._

    list running conatiner
   **docker ps**
    list all conatiner
   **docker ps -a**
   
6. Access the webpage from any browser:
   **https://localhost:8080/**
   
7. You can stop and delete the container using the following commands:
   **docker stop instance1**
   **docker rm instance1**

8. Finally, delete the image using:
   **docker rmi sampleimage**



