FROM node:4.2.6
MAINTAINER Sam Hausmann

#install necessary packages
RUN apt-get -y update && apt-get install -y git && apt-get install -y vim && apt-get install -y curl

RUN npm install -g grunt-cli && npm install -g eslint

ENV API_KEY api_key

RUN mkdir /nodejs-dev
COPY runAll.sh /nodejs-dev/runAll.sh
RUN chmod 0755 /nodejs-dev/runAll.sh

#set the working directory
WORKDIR /nodejs-dev

CMD ./runAll.sh
VOLUME ["/source"]
