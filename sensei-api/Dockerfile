#base image
FROM node:13.1.0

#set working directory
RUN mkdir /usr/src/sensei/api
WORKDIR /usr/src/sensei/api

# add '/usr/src/sensei/node_modules.bin' to $PATH
ENV PATH /usr/src/sensei/api/node_modules.bin:$PATH

# install and cache app dependencies
COPY package*.json /usr/src/sensei/api/
RUN npm install --silent

# start app
EXPOSE 8080
CMD [ "node", "index.js" ]
