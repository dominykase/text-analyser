# pull official base image
FROM node:18.14.0-alpine3.16

# set working directory
WORKDIR /var/www/frontend

# add `/app/node_modules/.bin` to $PATH
ENV PATH /var/www/frontend/node_modules/.bin:$PATH

# install app dependencies
COPY ./frontend/package.json ./
COPY ./frontend/package-lock.json ./

RUN npm install
RUN npm install react-scripts@3.4.1 -g

# add app
COPY ./frontend ./var/www/frontend

# start app
CMD ["npm", "start"]