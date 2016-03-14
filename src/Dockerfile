FROM    centos:centos6

# Enable Extra Packages for Enterprise Linux (EPEL) for CentOS
RUN     yum install -y epel-release
# Install Node.js and npm
RUN     yum install -y nodejs npm

# Install app dependencies
COPY package.json /src/package.json
RUN cd /src; npm install

# Bundle app source
COPY . /src

EXPOSE  8080
CMD ["node", "/src/index.js"]







# # Set the base image to Ubuntu
# FROM ubuntu:14.04
#
# #FOR DEBUGGING  
# RUN apt-get update -y
# RUN apt-get upgrade -y
#
# RUN apt-get install nodejs -y
# RUN apt-get install nodejs-legacy -y
# RUN apt-get install npm -y
#
# # Install nodemon
# RUN npm install -g nodemon
#
# RUN mkdir -p /usr/src/app
# WORKDIR /usr/src/app
#
# # Install app dependencies
# COPY src/package.json /usr/src/app
# RUN cd /usr/src/app; npm install
#
# # Bundle app source
# COPY src /usr/src/app
#
# EXPOSE  8080
# CMD ["node", "/usr/src/app/index.js"]
#
