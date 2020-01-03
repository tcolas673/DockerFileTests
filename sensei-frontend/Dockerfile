#base image
FROM node:13.1.0

#set working directory
RUN mkdir /usr/src/sensei/
WORKDIR /usr/src/sensei/

# add '/usr/src/sensei/node_modules.bin' to $PATH
ENV PATH /usr/src/sensei/node_modules.bin:$PATH

# install and cache app dependencies
COPY package.json /usr/src/sensei/package.json
RUN npm install --silent

# start app
CMD ["npm", "start"]