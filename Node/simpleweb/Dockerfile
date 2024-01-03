# # Specify a base image
# FROM alpine

# # Install some depenendencies
# RUN npm install

# # Default command
# CMD ["npm", "start"]

# FROM alpine
FROM node:14-alpine

WORKDIR /usr/app

COPY ./package.json ./

RUN npm install

COPY ./ ./


CMD ["npm","start"]