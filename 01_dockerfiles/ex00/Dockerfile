FROM alpine
MAINTAINER sechang <sechang@student.42.us.org>
RUN apk update
RUN apk upgrade
RUN apk add vim
ENTRYPOINT vim

#how to use alpine: https://hub.docker.com/_/alpine
#dockerfile format: https://docs.docker.com/engine/reference/builder/
#ENTRYPOINT: allows you to configure a container that will run as an executable
#base image: An image that has no parent is a base image
#man page apt-get: https://linux.die.net/man/8/apt-get
#update: update the package lists / Used to re-synchronize the package index files
#upgrade: update the packages / Used to install the newest versions of all packages currently installed on the system from the sources enumerated in /etc/apt/sources.list

#docker build: Build an image from a Dockerfile
#docker build -t ex00 .
#the '.' character at the end, which indicates the dockerfile is in the current directory

# How to run it?
# docker run --rm -ti ex00
