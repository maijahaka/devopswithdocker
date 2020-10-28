
FROM ubuntu:16.04

RUN apt-get update && apt-get -y install git
RUN git clone https://github.com/docker-hy/backend-example-docker
RUN apt-get -y install curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
WORKDIR /backend-example-docker
RUN npm install
CMD ["npm", "start"]
