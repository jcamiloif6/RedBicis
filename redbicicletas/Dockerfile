FROM mhart/alpine-node:8
ENV NODE_VERSION 8.9.4
# Create app directory
#RUN apt-get update
RUN mkdir /app
WORKDIR /app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json /app/
RUN npm install
# If you are building your code production
# RUN npm ci --only=production
# Bundle app Source
COPY . /app
# ENV PORT 8080
EXPOSE 1111
ENTRYPOINT [ "npm", "start"]